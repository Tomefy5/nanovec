# Getting Started with NanoVec

Welcome to NanoVec! This guide will help you set up your development environment and start building with NanoVec.

## Prerequisites

Ensure you have the following installed:
- **Rust Compiler**: Version 1.80+ or the 2024 edition.
- **Cargo**: Rust's package manager.

## Building the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/nanovec.git
   cd nanovec
   ```

2. Build the project:
   ```bash
   cargo build --release
   ```

## Using the CLI

Run the CLI help to see available commands:
```bash
./target/release/nanovec-cli --help
```

## Basic Code Example

Here is how you can use NanoVec in your Rust project:

```rust
use nanovec::api::NanoDB;

fn main() {
    let db = NanoDB::new("my_database.nvec");
    
    let vector = vec![0.1, 0.2, 0.3];
    db.insert(vector, "Some metadata".to_string());
    
    let query_vector = vec![0.1, 0.2, 0.29];
    let results = db.query(query_vector, 5);
    
    for result in results {
        println!("Found match: {:?}", result);
    }
}
```

## Running Tests

To ensure everything is working correctly:
```bash
cargo test
```

## Documentation

For more details, check out:
- [Architecture](architecture.md)
- [README (English)](../README.md)
- [README (French)](../README.fr.md)
