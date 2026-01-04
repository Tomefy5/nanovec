# NanoVec

NanoVec is a lightweight, high-performance vector database implemented in Rust, designed for edge computing and offline-first applications. It implements the HNSW (Hierarchical Navigable Small World) algorithm for efficient similarity search.

## Features

- **Blazing Fast**: Uses HNSW for logarithmic-time similarity search.
- **Memory Efficient**: Designed to handle large datasets even on devices with limited RAM.
- **SIMD Optimized**: Leverages hardware acceleration for distance calculations.
- **Multilingual Support**: Available in English and French.
- **Modular Architecture**: Clean separation between core algorithms, storage, and API.

## Project Structure

- `core/`: The "brain" of NanoVec, containing HNSW logic and vector operations.
- `storage/`: Handles persistence and binary file formats (`.nvec`).
- `api/`: Public interface and bindings (e.g., Python/Node.js).
- `cli/`: Command-line interface for managing and querying databases.

## Getting Started

### Prerequisites

- Rust (Latest stable or 2024 edition)
- Cargo

### Installation

```bash
git clone https://github.com/yourusername/nanovec.git
cd nanovec
cargo build --release
```

### Usage

```bash
# Example command coming soon
./target/release/nanovec-cli --help
```

## Documentation

Exhaustive documentation can be found in the `docs/` directory:
- [Architecture](docs/architecture.md)
- [Getting Started](docs/getting_started.md)

## License

This project is licensed under the terms specified in the LICENSE file.
