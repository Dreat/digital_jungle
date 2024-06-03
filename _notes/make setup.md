<status>Status: 🌿 </status>

Because I'm a weirdo, I decided to go with terminal only development. That means no `easy mode` of going with VSCode and pressing `build` to make it work. 

But it turns out (at least for start) it's not as difficult to do:

### Step one - Install Raylib

I'm on MacOS, so I just typed `brew install raylib`. You can easily get it on official website as well - https://www.raylib.com

### Step two - Prepare build

I went with a very simple Makefile, that I prepared during the course and was using for all projects there

```bash
.Phony: format

files := main.cpp

build: $(files)
	clang++ -o game $(files) -Wall -std=c++14 -g -O0 -I. -I/opt/homebrew/include -L. -L/opt/homebrew/lib -lraylib -framework OpenGL

format:
	clang-format -i *.cpp
	clang-format -i *.h

```

(You will need clang-format to use `format` target).

Now, when I type `make`, my code is compiled and I can type `./game` to mess around.
When I type `make format` my code get's formatted.

For a brief explanation what's happening here:

- This is a Makefile, which `tldr` "helps building software"
- `.Phony:` is used to say "hey, run it always"
- `files := main.cpp` is where you define files for your c++ project
- `clang++ ...` is the compiling step
	- output `game` executable, so it's possible to run `./game` and mess around
	- show warnings, use c++14, all that jazz
	- include all files from current directory as well as `/opt/homebrew/include`
	- link all libs from current directory as well as `opt/homebrew/lib`
		- (if brew was not used to install raylib, obviously the paths will change)
	- `I want raylib`
	- `use OpenGl`
- and `format` -> with `make format` I get formatted code, `clang-format` is needed, obviously 


### Step three - render something

With following `main.cpp`

```cpp
#include "raylib.h"

int main() {
  const int windowWidth = 300;
  const int windowHeight = 300;
  InitWindow(windowWidth, windowHeight, "Hello Raylib");

  unsigned char red = 0;
  unsigned char green = 117;
  unsigned char blue = 44;
  Color color = {};

  SetTargetFPS(60);
  while (!WindowShouldClose()) {
    red = (red + 1) % 128;
    green = (green + 2) % 128 + 128;
    blue = (blue + 3) % 128;
    color = {red, green, blue, 255};
    BeginDrawing();
    ClearBackground(WHITE);
    DrawCircle(windowWidth / 2, windowWidth / 2, 50, color);

    EndDrawing();
  }
  CloseWindow();
  return 0;
}

```

Code is not pretty, but will get the job done.
So; what's happening here?

1. Creating window. Width, height and title.
2. Then, I decided to be a bit fancy and (had to look into Raylib cheatsheet) created manually a color that I will manipulate.
	- Yes, those are unsigned chars, probably not most convenient way of doing that
	- `Color color = {};` seems like pretty recent addition - simple, but default initialisation is something I really enjoy
4. `SetTargetFPS(60)` set's the maximum FPS the game will run.
5. `while` loop with check if `esc` was pressed or `close window` button was pressed. Pretty handy, thou for game I would have not just kill everything on simple `esc` press.
6. Do wonky color manipulation.
7. `BeginDrawing()` and `EndDrawing()` are required, to easily show what goes into a frame.
8. `ClearBackground(WHITE);`
	- `WHITE` is Raylib's built in `Color` that we can use.
	- this method is used to prevent screen flickering
9. Draw our circle in the middle of the screen. Left right edge is {0,0} and it increases down and right. We give it `color`, so it is `animated`.
10. Once we're out of the loop, close window and be on own's merry way.

That should give a solid headstart for some simple experimentation with Raylib - if you know how to code it should be fun exploring how this can be extended.