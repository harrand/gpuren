# psygpu
## Overview
psygpu is a 3d graphics rendering library that keeps things relatively low level.

- only vulkan on windows is supported. linux support is a wibnif but i wont be getting around to it anytime soon.
- you must have vulkan 1.3 ready drivers installed.
- depends on [psystdlib](https://github.com/harrand/psystdlib), so you must also do `add_build_file("path/to/stdlib.psy", "default");` in your project's build region (before or after psygpu, doesnt matter)
- all memory allocations are done through the [arena api](https://github.com/harrand/psystdlib/blob/master/src/arena.psy). this means you have complete control over memory allocation.

there is a tradeoff between performance and api simplicity that graphics libraries must take. in terms of that tradeoff, psygpu leans towards performance - think of another SDL GPU rather than another Raylib
