To build and run natively:

```
mkdir build && cd build
cmake ..
make
./HelloCMake
```

To build with Emscripten:

1. Install Emscripen compiling tools
2. Set EMSCRIPTEN environment variable to the Emscripten root directory path.
3. Run the following commands:

```
mkdir build && cd build
cmake -DCMAKE_TOOLCHAIN_FILE=../cmake/Emscripten.cmake ..
make
```

Then open build/HelloCMake.html in a browser
