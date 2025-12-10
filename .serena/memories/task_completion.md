# What to do when finishing tasks
- No automated tests or linters are configured. If you modify training/inference code, run a quick smoke check with the relevant entrypoint (e.g., `python train.py --num_epochs 1 --batch_size 1`) to ensure it still runs.
- If touching visualization/generation scripts, run a minimal invocation (e.g., `python visualize.py --num_of_data 1`) to verify plotting paths exist.
- Check that required data directories (`data/train`, `data/validation`, `data/test`) and cache files exist or can be regenerated; run `bash make_directories.sh` if new environment lacks log/model/plot/result folders.
- Review outputs/logs in `log/`, `model/`, `plot/`, `result/` for errors; ensure checkpoints/configs are saved in expected subfolders.
- Document any new CLI flags or defaults in README or comments when you add them.