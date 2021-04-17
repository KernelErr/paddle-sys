# paddle-sys

[![PaddlePaddle version](https://img.shields.io/badge/PaddlePaddle-release%2F2.0-blue)](https://github.com/PaddlePaddle/Paddle)

Rust bindings for the Paddle Inference, the core inference engine for [PaddlePaddle].

This library is intended to provide a low-level wrapper for functions, datatypes, and others in the Paddle Inference C language API. You may use it in applications that need to interact with Paddle Inference directly in Rust.

## Bindings

We use the [bindgen] tool to generate wrappers over the Paddle Inference C language header file and the [libloading] tool to load the pre-compiled library. So before you run your application, please ensure you have a pre-compiled library with the correct version and set the environment variables to let the linker could find it. An example of Linux is shown below.

```
export LD_LIBRARY_PATH=/path/to/paddle_lib:$LD_LIBRARY_PATH
```

## External Information

The usage for this library is mostly like the stuff you do with Paddle Inference in C language. But it's in Rust, meaning that you would use some unsafe features and manage pointers and malloced memories. I sincerely hope that if there are developers who stand out to develop a safe wrapper based on this library. Let's make PaddlePaddle more prosperous!

Demos are available on [paddle-sys-demo]. Any advice is welcomed.

## License

paddle-sys is provided under the <a href="LICENSE-APACHE">Apache License, Version 2.0</a> or <a href="LICENSE-MIT">MIT license</a>.

[PaddlePaddle]: https://github.com/PaddlePaddle/Paddle
[bindgen]: https://github.com/rust-lang/rust-bindgen
[libloading]: https://github.com/nagisa/rust_libloading
[paddle-sys-demo]: https://github.com/KernelErr/paddle-sys-demo