# GLcompute
[![Documentation](https://godoc.org/github.com/adraenwan/glcompute?status.svg)](https://godoc.org/github.com/adraenwan/glcompute)

GLcompute (aka glc) is a Go library  for GPGPU using OpenGL ES 3.1 compute shaders as the backend.

* `glc/` contains the actual library
* `demo/` contains a short example to get started with glc

`glc/buffer.go` is the most tricky part ; it uses `unsafe` and `reflect` to interface Go's safe slices with OpenGL's unsafe `mmap`-based GPU memory access.

The rest is basically wrappers for OpenGL objects/functions written with the help of [go-gl](https://github.com/go-gl/gl/tree/master/v4.3-core/gl), plus some helper functions.
