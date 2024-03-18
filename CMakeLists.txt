cmake_minimum_required(VERSION 3.10)

# Set the project name
project(KVStoreProject)

# Specify the C standard
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)

# Include directories
include_directories("${PROJECT_SOURCE_DIR}/include")

# Add storage engine
SET(STORAGE_LIST
  src/storage/array/array.c
  src/storage/btree/btree.c
  src/storage/dhash/dhash.c
  src/storage/hash/hash.c
  src/storage/rbtree/rbtree.c
  src/storage/skiplist/skiplist.c
)

# file(GLOB_RECURSE SRC_LIST ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)

# Add server executable
add_executable(server src/network/main.c src/protocol/kvstore.c ${STORAGE_LIST})

# Add client executable
add_executable(client src/client/tb_kvstore.c)
