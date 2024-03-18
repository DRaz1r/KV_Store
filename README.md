## 构建项目
创建一个新的构建目录并进入它：
``mkdir build && cd build``

从CMake配置生成Makefile：
``cmake ..``

使用生成的Makefile构建项目：
``make``

build目录下生成两个可执行文件：server和client

```
ProjectRoot/
  ├── src/
  │   ├── client/
  │   │   └── tb_kvstore.c
  │   ├── protocol/
  │   │   ├── kvstore.h
  │   │   └── kvstore.c
  │   ├── network/
  │   │   └── main.c
  │   └── storage/
  │       ├── array/
  │       │   ├── array.c
  │       │   └── array.h
  │       ├── btree/
  │       │   ├── btree.c
  │       │   └── btree.h
  │       ├── dhash/
  │       │   ├── dhash.c
  │       │   └── dhash.h
  │       ├── hash/
  │       │   ├── hash.c
  │       │   └── hash.h
  │       ├── rbtree/
  │       │   ├── rbtree.c
  │       │   └── rbtree.h
  │       └── skiplist/
  │           ├── skiplist.c
  │           └── skiplist.h
  ├── include/
  │   
  └── CMakeLists.txt

```