<p align="center">
  <img src="assets/logo.png" alt="NanoVec Logo" width="200">
</p>

<h1 align="center">NanoVec</h1>

<p align="center">
  <strong>A lightweight, blazing-fast vector database for Edge Computing & Offline-first applications.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Rust-2024-orange?logo=rust" alt="Rust Version">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome">
  <img src="https://img.shields.io/badge/Status-Beta-yellow" alt="Status">
</p>

---

## 🚀 Why NanoVec?

NanoVec is designed for developers who need high-performance similarity search without the overhead of heavy cloud-based solutions. Built in **Rust**, it offers:

- ⚡ **Low Latency**: HNSW algorithm for logarithmic-time search.
- 📉 **Tiny Footprint**: Optimized for devices with limited memory (Edge/Mobile).
- 🛠️ **Zero-Copy Friendly**: Efficient serialization for fast I/O.
- 🧪 **SIMD Powered**: Leveraging hardware acceleration for vector math.

## 🏗️ Architecture

NanoVec follows a strict modular design to allow flexibility and high performance.

| Module | Responsibility | Key Features |
| :--- | :--- | :--- |
| **`core`** | Algorithmic Heart | HNSW implementation, SIMD metrics. |
| **`storage`** | Persistence | Custom `.nvec` format, WAL, mmap support. |
| **`api`** | Integration | Facade for developers, FFI (Python/Node). |
| **`cli`** | Management | Command-line tools for DB management. |

## 🛠️ Installation

```bash
# Clone the repository
git clone https://github.com/Tomefy5/nanovec.git

# Navigate to the directory
cd nanovec

# Build for release
cargo build --release
```

## 📋 Quick Start

```rust
use nanovec::api::NanoDB;

fn main() {
    // Create or load a database
    let db = NanoDB::new("my_data.nvec");

    // Insert a vector with metadata
    db.insert(vec![0.12, 0.45, 0.78], "user_node_1");

    // Perform a similarity search (Top-K)
    let results = db.query(vec![0.10, 0.40, 0.70], 5);

    println!("Top match: {:?}", results[0]);
}
```

## 📖 Documentation

Dive deeper into NanoVec's internals:

- [Architecture Overview](docs/architecture.md)
- [Full Getting Started Guide](docs/getting_started.md)
- [French Version (README.fr.md)](README.fr.md)

## 🤝 Contributing

We love contributions! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) to get started.

## ⚖️ License

Distributed under the **MIT License**. See `LICENSE` for more information.

---
<p align="center">Built with 🦀 by the NanoVec community.</p>
