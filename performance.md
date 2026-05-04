#Prior to restructure/constexpr

Sketch uses 832215 bytes (63%) of program storage space. Maximum is 1310720 bytes.
Global variables use 26688 bytes (8%) of dynamic memory, leaving 300992 bytes for local variables. Maximum is 327680 bytes.

write: 32
render: 0
raster: 13
remaining: 2

avg: 47

freeheap: 129324 bytes
max stack: 22848 bytes


#After alphablend restructure

Sketch uses 804979 bytes (61%) of program storage space. Maximum is 1310720 bytes.
Global variables use 26688 bytes (8%) of dynamic memory, leaving 300992 bytes for local variables. Maximum is 327680 bytes.

write: 32
render: 0
raster: 11
remaining: 2

avg: 45

freeheap: 129324 bytes
max stack: 22848 bytes


#After alphablend restructure & usage of existing INLINE_CONSTEXPR macro

Sketch uses 805075 bytes (61%) of program storage space. Maximum is 1310720 bytes.
Global variables use 26688 bytes (8%) of dynamic memory, leaving 300992 bytes for local variables. Maximum is 327680 bytes.

write: 32
render: 0
raster: 11
remaining: 2

avg: 45

freeheap: 129324 bytes
max stack: 22848 bytes


#After alphablend restructure & usage of existing INLINE_CONSTEXPR macro & using templated callbacks for screen access
Framebuffer uses ```LFGX_Sprite``` (rgb332) rather than previous ```texture_t<color8_t>```.
Callbacks include a method for drawing rect directly.
Callbacks are also declared with ```__attribute__((always_inline))```

Sketch uses 748931 bytes (57%) of program storage space. Maximum is 1310720 bytes.
Global variables use 27016 bytes (8%) of dynamic memory, leaving 300664 bytes for local variables. Maximum is 327680 bytes.

write: 31
render: 0
raster: 3
remaining: 2

avg: 37

freeheap: 117392 bytes
max stack: 22848

