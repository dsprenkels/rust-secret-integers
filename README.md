# Rust secret integers

This simple crate provides integer wrappers that guarantee that they are being used in a constant-time fashion. Hence, division and direct comparison are disallowed. Using Rust's type system, this crate will help the compiler check systematically whether your cryptographic code is constant-time relative to secret inputs.

To use the crate, just import everything (`use secret_integers::*;`) and replace your integer types with uppercase versions of their names (e.g. `u8` -> `U8`).

## Examples

Two examples show how to use the crate : [Dalek](https://github.com/denismerigoux/rust-secret-integers/tree/master/examples/dalek.rs)
and [Chacha20](https://github.com/denismerigoux/rust-secret-integers/tree/master/examples/chacha20.rs).
To build theses examples, use

    cargo build --example dalek
    cargo build --example chacha20
