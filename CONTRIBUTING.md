# Contributing to Xenon-Core

We welcome contributions! Please follow these steps to set up your development environment.

## 1. Environment Setup

### Install Rust
You need the Rust compiler and Cargo.
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### Install Maturin
We use `maturin` to build the Python extension.
```bash
pip install maturin
```

## 2. Running Tests
Run the standard Rust test suite:
```bash
cargo test
```

## 3. Coding Standards
- **Indentation**: Use 4 spaces.
- **Linting**: Please run `clippy` before submitting:
  ```bash
  cargo clippy
  ```
- **Formatting**: Use `cargo fmt` to ensure standard formatting.
