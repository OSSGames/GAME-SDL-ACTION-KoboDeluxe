# KoboDeluxe

Kobo Deluxe is an enhanced version of Akira Higuchi's classic scrolling shooter XKobo — 50 action-packed levels of arcade mayhem with smooth animation, sound effects, and multiple skill levels.

Original game by Akira Higuchi. Kobo Deluxe port by David Olofson. This repository contains the **ArcaOS / OS/2 port** built with GCC 9.2 and SDL2.

For the full game description, controls reference, and command-line options see [README](README).  
For OS/2-specific build and installation instructions see [Kobo_os2.txt](Kobo_os2.txt).

---

## ArcaOS / OS/2 Port Status

| Feature         | Status                        |
|-----------------|-------------------------------|
| Windowed mode   | Working                       |
| Fullscreen mode | Not supported                 |
| Sound           | Working (requires SDL2_mixer) |
| Keyboard        | Working                       |
| Joystick        | Untested                      |

---

## Requirements

- ArcaOS 5.x (or OS/2 Warp 4 with kLIBC)
- SDL2, SDL2\_image, SDL2\_mixer DLLs on the `LIBPATH` (available via `yum`)

---

## Building

Requires GCC 9.2 (kLIBC), SDL2 dev packages, and GNU make. Run from the source root on ArcaOS:

```
compile-kobodl.cmd
```

Output: `kobodl.exe`

Source layout:

```
src\            top-level game sources
src\graphics\   graphics engine
src\sound\      sound engine
src\eel\        scripting engine
data\gfx\       PNG graphics assets
data\sfx\       AGW sound assets
```

---

## Running

The game must be launched from its own directory so that `data\` is reachable:

```
cd C:\Games\KoboDeluxe
kobodl.exe
```

Settings are written to `kobodl.cfg` and high scores to `KoboPlayer`, both in the game directory.

---

## Controls

| Key                | Action                  |
|--------------------|-------------------------|
| Arrow keys         | Move ship               |
| Shift / Ctrl       | Fire                    |
| Numpad 1 / 3 / 7 / 9 | Single-key diagonals |
| Escape             | Menu / Pause            |

---

## License

GNU General Public License — see [COPYING](COPYING).

Copyright (c) 1995–1996 Akira Higuchi  
Copyright (C) 1997 Masanao Izumo  
Copyright (C) 1999–2007 David Olofson

## Links
- https://github.com/OS2World/GAME-SDL-ACTION-Kobo_Deluxe
