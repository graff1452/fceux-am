# fceux-am

Personal backup fork of [NJU-ProjectN/fceux-am](https://github.com/NJU-ProjectN/fceux-am)
(branch `ics2021`) — an NES emulator (FCEUX) ported to run on top of AM.

Unmodified from upstream. Kept here purely so it's available on any machine without
depending on the upstream repo staying reachable.

This repo is meant to be cloned **inside** an `ysyx-workbench/` checkout (see
[OSOC](https://github.com/graff1452/OSOC)), since it builds against AM via `$AM_HOME`.

## Setup

```bash
git clone git@github.com:graff1452/fceux-am.git
```

## ROM files are NOT included

`nes/rom/` is gitignored, deliberately — ROM files are copyrighted game content and
should never be committed to a public repo (that's how upstream ships it too). To run
a game, place a legally-obtained `.nes` file at:

```
fceux-am/nes/rom/<name>.nes
```

## Running

```bash
make ARCH=native run mainargs=<name>
```
(where `<name>` matches the ROM filename without `.nes`, e.g. `mainargs=mario` for
`nes/rom/mario.nes`)

## Controls

| Key | Action |
|---|---|
| W/S/A/D | D-pad (Up/Down/Left/Right) |
| J | A button |
| K | B button |
| U | Select |
| I | Start |
| Q | Quit |
