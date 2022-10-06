# PyVGDL 2.0

A reimplementation on steroids
of the original
[py-vgdl](https://github.com/schaul/py-vgdl/)
by Tom Schaul.

Under heavy and active development,
just check the latest timestamps in the git history.


## What is it?

VGDL stands for
Video Game Description Language.
PyVGDL is an easily scriptable video game engine written in Python,
ideal for artificial intelligence research.

Given a [game description](examples/continuousphysics/platformer.txt),
it allows you to turn something like
```
w              w
w              w
w              w
w              w
w   HwwwwHwwwwww
w   H ww H     w
wA  H ww H  G  w
wwwwwwwwwwwwwwww
```
… into a human or AI-playable game:

![level play](examples/continuousphysics/left_to_right_play.png)

PyVGDL interfaces with [Gymnasium][gym-repo] (formerly OpenAI Gym). Support for
[PettingZoo][pettingzoo-repo] is planned.

[gym-repo]: https://github.com/farama-foundation/gymnasium
[pettingzoo-repo]: https://github.com/farama-foundation/pettingzoo

## Installation
The easiest way to install VGDL as a library with all its dependencies is to run
```bash
pip install vgdl
```

You can use a local installation in the usual way.
```bash
git clone https://github.com/jmuchovej/vgdl
pip install -e vgdl
```

### Dependencies
You'll need Python >= 3.6.
This is so we can have nice things.


## How do I use it?

PyVGDL is excellent for designing your own problem environments that still 
share some standard characteristics. It supports grid phyics and continuous
phyics.

You probably want to use one of several standard interfaces:
- [OpenAI Gym interface](vgdl/interfaces/gymnasium)

Read ahead to figure out how best to get started with either.

## Getting Started

Example code is included that relies on VGDL's Gym interface
to demonstrate the engine through human game play.
Give it a go:
```bash
# Any of the games in vgdl/games will work
python -m vgdl.util.humanplay.play_vgdl vgdl/games/aliens_lvl0.txt
```
Definitely check out
[all the other examples](examples/README.md)
demonstrating human play (with recording and replay),
reinforcement learning, planning,
and of course writing your own games to do any number of these things.


## How does it relate to other frameworks

- A more full-fledged VGDL implementation is written and maintained
for the [General Video Game AI Competition](http://www.gvgai.net/),
so look there for more features and expressability.
It features a server-client model written in Java,
tailored for the competition,
whereas this repository
aims to be a complete yet lightweight
Python implementation
for AI research.

## TODO
- While manual testing has been done by multiple parties,
  we are in desperate need of unit and scenario tests.
- Some more basic ontology functionality is welcome.
- Could use another PEP check.
