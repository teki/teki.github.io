---
layout: post
title:  "Visual Studio Code C/C++ code completion with YCMD"
date:   2017-03-14
categories: programming
---

## Clang 4 support

Linking will fail with the error: `install_name_tool: no LC_RPATH load command with path: @executable_path/../lib`
This is not needed anymore, so this should fix it:
```
diff --git a/cpp/ycm/CMakeLists.txt b/cpp/ycm/CMakeLists.txt
index 2074c58e..82c7abdd 100644
--- a/cpp/ycm/CMakeLists.txt
+++ b/cpp/ycm/CMakeLists.txt
@@ -367,7 +367,7 @@ if( LIBCLANG_TARGET )
       COMMAND ${CMAKE_COMMAND} -E copy "${LIBCLANG_TARGET}" "$<TARGET_FILE_DIR:${PROJECT_NAME}>"
     )

-    if( APPLE )
+    if( 0 )
       # In OS X El Capitan, Apple introduced System Integrity Protection.
       # Amongst other things, this introduces features to the dynamic loader
       # (dyld) which cause it to "sanitise" (and complain about) embedded
```

## Build

```
curl -O http://releases.llvm.org/4.0.0/clang+llvm-4.0.0-x86_64-apple-darwin.tar.xz
tar xvf clang+llvm-4.0.0-x86_64-apple-darwin.tar.xz
git clone https://github.com/Valloric/ycmd.git
cd ycmd
git submodule update --init --recursive
# patch cpp/ycm/CMakeLists.txt
EXTRA_CMAKE_ARGS="-DPATH_TO_LLVM_ROOT=${PWD}/../clang+llvm-4.0.0-x86_64-apple-darwin" python build.py --clang-completer
```

## Visual Studio Code config sample

The extension: [https://marketplace.visualstudio.com/items?itemName=RichardHe.you-complete-me]()

Minimal config:
```
    "ycmd.path": "/Users/notsowise/pathto/ycmd",
```

## Generate completion database

Pass `-DCMAKE_EXPORT_COMPILE_COMMANDS=ON` to cmake on invocation. You might have to copy the compile_commands.json into the source tree.

Something like this:
```
mkdir build
cd build
cmake -G Ninja -DCMAKE_EXPORT_COMPILE_COMMANDS=ON ../src
cp compile_commands.json ../src
cd ../src
code .
```
