How to build:

```sh
git clone https://github.com/stiffstream/sobjectizer-fetchcontent-demo
cd sobjectizer-fetchcontent-demo
mkdir cmake_build
cd cmake_build
cmake -DCMAKE_INSTALL_PREFIX=target ..
cmake --build . --config Release --target install
```

The result of the build process will be stored in `target/bin` subdirectory of `cmake_build`. To run the resulting application:

On Windows it's just:

```sh
target\bin\sample.so_5.hello_world.exe
target\bin\sample.so_5.hello_world_s.exe
```

On Linux the `sample.so_5.hello_world_s` can be simple invoked because of static linking to SO-5 library:

```sh
./target/bin/sample.so_5.hello_world_s
```

but for `sample.so_5.hello_world` an addition action is recuired becase SO-5 shared library is in `target/lib`. It means that `LD_LIBRARY_PATH` has to be modified:

```sh
LD_LIBRARY_PATH=$LD_LIBRARY_PATH:./target/bin \
  ./target/bin/sample.so_5.hello_world
```
