# XRGB TO PACKED RGB
Elias Malloy

The pixels of an image may be stored in a number of different ways. Today I will look at a few implementations of converting between an XRGB encoding of 24-bit color, to packed 24-bit RGB. XRGB is useful for referencing and manipulating pixels because each pixel is aligned to a four-byte memory address. XRGB pixels can be read and written in four byte blocks because of their alignment. The unused X is a major waste of space, especially in a rendered image. It's valuable to have an efficient way to convert between the two encodings so that you can take advantage of the strengths of each encoding at different stages of processing. We’ll first take a look at two similar c implementations of XRGB to RGB, the conversion I’m focusing on.

![C implementation](figures/Cimpl.png)


