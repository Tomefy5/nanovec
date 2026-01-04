# NanoVec Architecture

NanoVec is designed with a modular architecture to ensure performance, scalability, and ease of use.

## Core Module (`core/`)

The `core` module is the algorithmic heart of NanoVec. It is responsible for:

- **HNSW Implementation**: Manages the multi-layered graph structure for fast vector retrieval.
- **Distance Metrics**: Implements Euclidean, Cosine, and Dot Product distances with SIMD optimizations.
- **Vector Operations**: Basic operations on vector data.

### Key Components

- `HNSWIndex`: The main index structure.
- `VectorNode`: Represents a node in the graph, containing the vector and its neighbors.
- `Metric` Trait: Defines the interface for distance calculations.

## Storage Module (`storage/`)

The `storage` module handles data persistence. It ensures that vectors and the index can be saved to and loaded from disk efficiently.

- **Binary Format**: Uses a custom `.nvec` format for compact storage.
- **Write-Ahead Log (WAL)**: Ensures data integrity during crashes.
- **Page Manager**: (Planned) Efficient memory mapping for large datasets.

## API Module (`api/`)

The `api` module provides a clean facade for developers. It abstracts the complexity of `core` and `storage`.

- **NanoDB**: The primary entry point for users.
- **FFI Bindings**: Exposes NanoVec to other languages like Python and Node.js using `pyo3` or similar tools.

## CLI Module (`cli/`)

The `cli` module provides a command-line interface to interact with NanoVec databases without writing code.

- Create and manage databases.
- Insert vectors from CSV/JSON.
- Perform similarity searches.
