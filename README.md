# ibusqt

A Qt client library for the [IBus](https://github.com/ibus/ibus) input
method framework, talking to the IBus daemon over D-Bus with QtDBus.

This is a port of the original ibus-qt 1.3.x by Peng Huang, maintained
by the [makibus](https://github.com/makibus) organization. It builds
with both Qt 5 and Qt 6, and tracks fixes from
[ibus/ibus-qt](https://github.com/ibus/ibus-qt) upstream.

## Building

Requirements:

- CMake >= 3.16
- Qt 5 (>= 5.4) or Qt 6, with the Core, DBus and Xml modules

```
cmake -B build
cmake --build build
cmake --install build
```

## Using

Headers are installed under `include/ibusqt`, and a pkg-config file
is provided:

```
pkg-config --cflags --libs ibusqt
```

Include the umbrella header after adding the ibusqt include directory:

```cpp
#include <qibus.h>
```

The API lives in the `IBus` namespace, e.g. `IBus::Bus`,
`IBus::InputContext`, `IBus::Engine` and `IBus::Config`.

## License

GPL-2.0-only, matching upstream ibus-qt (see [COPYING](COPYING)).
The keysym table in `qibuskeysyms.h` originates from ibus under
LGPL-2.0+ and is relicensed under GPLv2 per section 3 of the LGPL.

