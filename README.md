# MiniGrep

A simple **Rust** command-line text search tool inspired by the classic Unix `grep` utility.  
MiniGrep reads a file, searches for a given pattern, and prints lines that contain that pattern. :contentReference[oaicite:0]{index=0}

---

## 🧠 About

MiniGrep is a learning project to understand how to:

- Accept and parse command-line arguments in Rust  
- Read and process file contents  
- Perform text search (case-sensitive and optionally case-insensitive)  
- Structure a Rust project with `main.rs` and library code (`lib.rs`)  
- Write basic unit tests for core logic :contentReference[oaicite:1]{index=1}

---

## 🚀 Features

✔️ Search for a substring in a text file  
✔️ Supports case-insensitive search (via environment variable)  
✔️ Modular design separating CLI parsing and search logic  
✔️ Unit tests for core search functionality :contentReference[oaicite:2]{index=2}

---

## 🛠️ Getting Started

### Prerequisites

Make sure you have the Rust toolchain installed:

```sh
rustup toolchain install stable
rustup default stable
````

---

### 📦 Build & Run

Clone the repo:

```sh
git clone https://github.com/PranavGaur7/MiniGrep.git
cd MiniGrep
```

Build in debug mode:

```sh
cargo build
```

Or build optimized release:

```sh
cargo build --release
```

---

## 📄 Usage

Run the program with:

```sh
cargo run -- <query> <file_path>
```

**Example:**

```sh
cargo run -- Rust poem.txt
```

This searches for the word `Rust` in `poem.txt`. ([Docs.rs][1])

---

### 🔍 Case-Insensitive Search

To perform a case-insensitive search, set the environment variable first:

**Linux / macOS:**

```sh
export IGNORE_CASE=1
cargo run -- rust poem.txt
```

**Windows (PowerShell):**

```ps
$env:IGNORE_CASE=1
cargo run -- rust poem.txt
```

---

## 🧪 Running Tests

Run the built-in unit tests:

```sh
cargo test
```

This tests both case-sensitive and case-insensitive search logic. ([Docs.rs][1])

---

## 📦 Project Structure

```
MiniGrep/
├── Cargo.toml
├── src/
│   ├── main.rs          # CLI and entry point
│   └── lib.rs           # Search and config logic
├── poem.txt             # Example input file
└── README.md
```
