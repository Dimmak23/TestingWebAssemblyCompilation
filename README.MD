# How can I compile C/C++ codebase into WebAssembly?

Main entry point of the project could be converted into _.js and _.html by these 4 steps:

1. Get Emscripten software development kit by running script: get_emsdk.bat;
   Emscripten compiler will be used as default compiler later;

2. Configure project with necessary generator (Ninja) and toolchain file by running script: cmake_config_toolchain.bat;

3. Build executable by running simple script: cmake_build.bat;

4. Finally you can show \*.html in browser by running it with emrun: emrun_executable.bat;

![plot](./documentation/images/example.gif)
