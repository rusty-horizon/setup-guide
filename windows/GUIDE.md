# Windows setup

## Step by step

devkitPro is just supported on 64bit Windows, so this guide too.

1. [Setup of Rust](#setup-of-rust)
2. [Setup of MinGW](#setup-of-mingw)

### Setup of Rust

- Download rustup-init installer from [Rust website](http://win.rustup.rs).

- On the same directory, execute `rustup-init.exe --default-host x86_64-pc-windows-gnu --default-toolchain nightly-2019-01-19-x86_64-pc-windows-gnu`, and hit 1. Wait until it installs.

- Now, run `rustup component add rust-src`.

- We also need to install xargo, a cross-platform compiling cargo wrapper, so run `cargo install xargo`.

- If any of the commands above failed, make sure that the path `C:\<user>\.cargo\bin` is added to PATH in environment variables, and retry again.

### Setup of MinGW

- Now we have to install MinGW. In case you don't have it already installed, install it from [here](https://sourceforge.net/projects/mingw-w64/).

- Having it installed, create a new environment variable named `CC` with the path to GCC compiler, which usually is `<mingw>\bin\gcc.exe`.