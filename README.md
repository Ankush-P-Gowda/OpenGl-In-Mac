# OpenGl-In-Mac
Steps to execute OpenGl program in Mac using Xcode

1.Install Xcode in AppStore.
2.Install HomeBrew by pasting /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)” in your terminal.
3.Now paste brew install glew.( If you get permission error then follow this step => sudo chown -R your_username /usr/local/lib/pkgconfig after pressing enter terminal will ask your password, now enter your Mac password to give permission to change. Now paste brew install glew again).
4.Now paste brew install glfw.
5.Now open Xcode start your new project choose macOS and choose command line tool choose your own project name and destination.
6.Now select “Build Phases” above in the toolbar. Then select “link binary with libraries”.
7.Now add frame work by pressing + symbol.
(a).Add OpenGL frame work.
(b).Add Glut framework.
(c)Press Add Other then Add files here press cmd+shift+G on keyboard and search for /usr/local/Cellar/glew/2.2.0_1/lib/libGLEW.2.2.0.dylib
(d)Press Add Other then Add files here press cmd+shift+G on keyboard and search for /usr/local/Cellar/glfw/3.3.4/lib/libglfw.3.3.dylib
8.Now select “Build Settings” above in toolbar. Then search for ‘header search path’ double click and add /usr/local/include
9.Now search ‘Other C Flags’ and add “-Wno-deprecated”.
10.Now everything is finished just these includes always in your program always  

#include <stdio.h>
#include <stdlib.h>

#if defined(__APPLE__)
#include <GLUT/glut.h>
#else
#include <GL/glut.h>
#endif

11.Now test your program for sample use the code in this link => 
