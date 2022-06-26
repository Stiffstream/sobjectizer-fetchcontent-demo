How to build:

```sh
git clone https://github.com/stiffstream/sobjectizer-fetchcontent-demo
cd sobjectizer-fetchcontent-demo
mkdir cmake_build
cd cmake_build
cmake -DCMAKE_INSTALL_PREFIX=target ..
cmake --build . --config Release --target install
./target/bin/sample.so_5.hello_world
```

**ATTENTION**. SObjectizer will be built as a static library. If it's built as shared library then SObjectizer's shared library won't be copied to the appropriate location during install step. It's unknown why. Any help on this topic will be appriciated.

