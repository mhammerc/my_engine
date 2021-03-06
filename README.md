# My_engine

## Presentation

When I was planning the development, I didn't got able to find a proper name.
So on, I called my engine 'my_engine'.

This is a fully working 3D game engine made from scratch using raycasting. It
have a game loop, textures, map management, animations and a smooth gameplay.
It is also multithreaded. Note this is not a production ready engine.

It was made as a 42 project (school 42 at Paris) named Wolf3D. Making that kind of engine
wasn't asked but I wanted to make things well.

I made [a demo on YouTube](https://youtu.be/oU3RUNNH1Vc):

[![Open YouTube demo](https://raw.githubusercontent.com/mhammerc/my_engine/master/example/resources/splash.png)](https://youtu.be/oU3RUNNH1Vc)

## How to run

Just open a shell and run

    make && make start

On Linux, a few warning will show up. They are not from me but from minilibx
:(

## Under the hood

There is an example game in *example* folder, sources of the engine are located
in *my_engine* folder.

It works on Mac and Linux (as of January 6 2017).

It use the minilibx: a very minimalistic graphic library. It can open a window,
draw pixels and load .xpm files.

## Requirements

On Mac you need XCode.

On Linux you need a few packages. Adapt to your distribution:

    apt update && apt install build-essential libx11-dev libxext-dev libbsd-dev
