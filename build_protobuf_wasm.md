```
git clone --recursive https://github.com/protocolbuffers/protobuf.git
cd protobuf
```

Add this to CMakeLists.txt:

```
SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -s ASSERTIONS=2 --memory-init-file 0 -s ALLOW_MEMORY_GROWTH=1")
set(CMAKE_CXX_STANDARD 17 CACHE STRING "v")
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
```

Build in emscripten:

```
emcmake cmake -B build -Dprotobuf_BUILD_TESTS=OFF
emmake make -C build
emcmake cmake --install build --prefix ../prot
```
