# Contributing to NanoVec

Thank you for your interest in contributing to NanoVec! We welcome all contributions, from bug reports to new features.

## How to Contribute

### Reporting Bugs
- Use the [Bug Report template](.github/ISSUE_TEMPLATE/bug_report.md).
- Provide a clear description of the issue and steps to reproduce.

### Suggesting Features
- Use the [Feature Request template](.github/ISSUE_TEMPLATE/feature_request.md).
- Describe the use case and why the feature would be beneficial.

### Pull Requests
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/my-new-feature`).
3. Make your changes.
4. Ensure the code follows the project's standards (run `cargo fmt` and `cargo clippy`).
5. Run tests (`cargo test`).
6. Commit your changes (`git commit -m 'feat: add some feature'`).
7. Push to the branch (`git push origin feature/my-new-feature`).
8. Open a Pull Request.

## Development Setup

1. Install Rust: `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`
2. Clone the repo: `git clone https://github.com/Tomefy5/nanovec.git`
3. Build the project: `cargo build`

## Coding Standards

- **Formatting**: Always run `cargo fmt` before committing.
- **Linting**: No new clippy warnings should be introduced.
- **Testing**: Add tests for any new functionality.

## Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.
