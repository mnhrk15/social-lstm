# Style and conventions
- Python scripts with argparse-driven `main()` entrypoints; training/inference invoked via `if __name__ == '__main__': main()` patterns.
- Functions/methods use snake_case; classes CamelCase. No type hints; minimal docstrings/comments.
- Four-space indentation; relies on torch Variables/tensors directly (no typing/static checks).
- Configuration passed via argparse; arguments often forwarded as `args` objects into model/DataLoader.
- File paths built with `os.path.join`; optional `--drive` flag prefixes paths with `drive/semester_project/social_lstm_final/`.
- Persistence uses `pickle` for configs/checkpoints and `.cpkl` cache files; logs/plots/checkpoints stored under `log/`, `plot/`, `model/`, `result/` created by `make_directories.sh` or lazily in scripts.
- No linting/formatting/test tooling configured; follow existing imperative/NumPy/PyTorch style when extending code.