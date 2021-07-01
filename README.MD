Sanity check for my custom `#[unsafe_fp_math]` attribute in Rust

```sh
cargo +unsafe_fp_math rustc --release -- --emit=llvm-ir
filecheck --input-file target/release/deps/fastmath_llvm_filecheck-{alphanums}.ll src/lib.rs
```