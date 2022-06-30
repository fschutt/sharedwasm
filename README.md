# sharedwasm

Example test-case to build a WASM32-WASI library:

```sh
# Build (install rustup target first)
cargo +nightly build -Zbuild-std --release --target wasm32-wasi
# Unpack .rlib into object file
ar -x ./target/wasm32-wasi/release/libsharedwasm.rlib
# Install wasm disassembly tools
sudo apt install wabt
wasm-objdump -d ./sharedwasm-58cd299b3f128130.sharedwasm.2a7776b6-cgu.0.rcgu.o
```
