# OpenGl-In-Mac
Steps to execute OpenGl program in Mac using Xcode

* Install Xcode in AppStore.
* Install HomeBrew by pasting /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)” in your terminal.
* Now paste brew install glew.( If you get permission error then follow this step => sudo chown -R your_username /usr/local/lib/pkgconfig after pressing enter terminal will ask your password, now enter your Mac password to give permission to change. Now paste brew install glew again).
* Now paste brew install glfw.
* Now open Xcode start your new project choose macOS and choose command line tool choose your own project name and destination.
* Now select “Build Phases” above in the toolbar. Then select “link binary with libraries”.
* Now add frame work by pressing + symbol.
    * Add OpenGL frame work.
    * Add Glut framework.
    * Press Add Other then Add files here press cmd+shift+G on keyboard and search for /usr/local/Cellar/glew/2.2.0_1/lib/libGLEW.2.2.0.dylib
    * Press Add Other then Add files here press cmd+shift+G on keyboard and search for /usr/local/Cellar/glfw/3.3.4/lib/libglfw.3.3.dylib
* Now select “Build Settings” above in toolbar. Then search for ‘header search path’ double click and add /usr/local/include
* Now search ‘Other C Flags’ and add “-Wno-deprecated”.
* Now everything is finished just these includes always in your program always  

> #include <stdio.h>
> #include <stdlib.h>

> #if defined(__APPLE__)
> #include <GLUT/glut.h>
> #else
> #include <GL/glut.h>
> #endif

* Now test your program for sample use the code in this link => https://github.com/Ankush-P-Gowda/OpenGl-In-Mac/blob/main/Sample%20Program%20for%20Radient%20Triangle%20(2).txt
