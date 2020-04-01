# wasm-contract
Wasm contract contain example of smart contract which are written in rust and compile to wasm.


## Tutorial Prerequisites
There is a list of all tools and dependencies required for this tutorial.

### Rust
[rustup](https://github.com/rust-lang-nursery/rustup.rs#installation) is the easiest way to install Rust toolchains. Rust nightly toolchain is required since our contracts require some unstable features:

```bash
rustup install nightly-2018-11-12
```

Also, we need to install `wasm32-unknown-unknown` to compile contracts to Wasm:

```bash
rustup target add wasm32-unknown-unknown
```

### wasm-build
`wasm-build` takes the raw `.wasm` file produced by Rust compiler and packs it to the form of valid contract.

```
cargo install pwasm-utils-cli --bin wasm-build
```

## Build Prerequisites
This project contains 3 example of wasm contract written using rust

```
* Getset string value
* Erc20Token
* Calaculator
```

Please refer for code structure in

```
cd erc20token/src/lib.rs
```

Build the wasm contract

```
cd erc20token/
```

```
./build.sh
```

> Above command create the folder name called `target` which contains all the dependecy with the `.wasm` contract with `.json` interface.

### For deploy the code
Follow the [wasm-node deploy guide](https://github.com/maxonrow/wasm-node). You'll need Durian VM  for wasm contract deployment.
