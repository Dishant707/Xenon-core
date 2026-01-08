# Changelog

All notable changes to this project will be documented in this file.

## [v0.4.0] - 2026-01-08

### Added
- **Manual Parallel K-mer Counting**: Implemented a zero-copy, multi-threaded K-mer counter using `std::thread` and unsafe pointer handling for maximum performance (~2.7x faster than Rayon+File).
- **`KmerCounts` Struct**: A custom PyObject that wraps the Rust HashMap to avoid massive memory allocation when returning millions of K-mers to Python. Supports dict-like access.
- **`translate` Function**: High-performance DNA to Protein translation using the Standard Genetic Code (8.9x faster than Biopython). Supports stop codons and ignores partial trailing codons.
- **`trim_low_quality`**: Phred+33 quality trimming optimization (52x faster).
- **`filter_reads`**: Fast FASTA/FASTQ filtering by minimum sequence length.
- **Benchmarks**: Added comprehensive benchmark scripts (`benchmark_translate.py`, `benchmark_final.py`).

### Changed
- **`gc_content`**: Optimized with static lookup tables (21x faster).
- **`reverse_complement`**: Optimized with static lookup tables (2.2x faster).
- **`process_file`**: Exposed basic genome stats processing.

### Fixed
- Fixed version mismatch between `Cargo.toml` and `pyproject.toml` causing PyPI conflicts.
