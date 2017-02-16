# gltf

This library is intended to load [glTF assets](https://www.khronos.org/gltf), a file format designed for the efficient transmission of 3D models. It is in its early stages of development, hence it is not fully-featured and future releases are not guaranteed to be backward compatible. It requires rustc version 1.15 or above to compile.

[![Build Status](https://travis-ci.org/Alteous/gltf.svg?branch=master)](https://travis-ci.org/Alteous/gltf)
[![Crates.io](https://img.shields.io/crates/v/gltf.svg)](https://crates.io/crates/gltf)

[Documentation](https://docs.rs/gltf)

### Usage

Add `gltf` to the dependencies section of `Cargo.toml`:

```toml
[dependencies]
gltf = "0.2"
```

Import the crate in your library or executable:

```rust
extern crate gltf;

use gltf::Gltf;
```

Load a glTF file:

```rust
fn main() {
    let gltf = Gltf::new("Foo.gltf").unwrap();
}
```

### Future Goals

 - [x] Ability to be compilied with the latest stable toolchain (1.15)
 - [ ] Full conformance to the [specification](https://github.com/KhronosGroup/glTF/blob/master/specification/1.0/README.md)
 - [ ] Replace untyped `GLenum` identifiers with equivalent type-safe constants
