# ibusqt

A Qt client library for the [IBus](https://github.com/ibus/ibus) input
method framework, talking to the IBus daemon over D-Bus with QtDBus.

This is a port of the original ibus-qt 1.3.x by Peng Huang, maintained
as a standalone library. It builds with both Qt 5 and Qt 6.

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
