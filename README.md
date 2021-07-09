# raylib starter

Just a simple Makefile based project to build games with raylib for HTML and Windows.

## Prerequisites
- a Windows OS
- CMD or Powershell
- make and gcc (mingw provides both)
- a compiled version of libraylib.a for web and libraylib.a for desktop (or use the ones provided in this repo)

## Usage
Create the following architecture:
```
       - include/
         - raylib.h
       - lib/
         - desktop/
						- libraylib.a (compiled from source with PLATFORM_DESKTOP)
					- web/
						- libraylib.a (compiled from source with PLATFORM_WEB)
						- shell.html (copied from source)
       - resources/
         - images, sounds, etc
        main.c
```
Then, in a cmd or powershell terminal:
- `make web=1` to build for HTML
- `make` to build for windows
- `make clean_web` to clean the web build folder
- `make clean_desktop` to clean the desktop build folder