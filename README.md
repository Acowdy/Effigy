# Effigy Desktop Theme

Copyright 2026 Adam Cowdy

Effigy is licensed under the GNU GPL Version 2.

## Build and install

Build and install locally:

```sh
meson setup --prefix=$HOME/.local builddir
cd builddir
ninja
ninja install
```

Build and install system wide:

```sh
meson setup --prefix=/usr builddir
cd builddir
ninja
ninja install
```
