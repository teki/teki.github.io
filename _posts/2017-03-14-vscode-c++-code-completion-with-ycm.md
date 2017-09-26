---
layout: post
title:  "Visual Studio Code C/C++ code completion with YCMD"
date:   2017-03-14
categories: programming
---

## Build YCMD

```
git clone https://github.com/Valloric/ycmd.git
cd ycmd
git submodule update --init --recursive
python build.py --clang-completer
```

## Visual Studio Code config sample

The extension: [https://marketplace.visualstudio.com/items?itemName=RichardHe.you-complete-me]()

Minimal config:
```
    "ycmd.path": "/Users/notsowise/pathto/ycmd",
```

Optional config in case you have multiple python versions:
```
    "ycmd.python": "/usr/bin/python"
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
