# Numerai Machine Learning Tournament

This repository contains a historical Numerai Tournament modeling pipeline. The shell launchers were written for a particular workstation and Docker image. A fresh checkout does not include all of the dataset files and model configurations those launchers reference.

> **Review the Docker scripts before running them.** The five launchers listed below issue `docker rm $(docker ps -a -q)`, which can remove stopped containers from other projects.

- [`02_cron_run_infer.sh`](02_cron_run_infer.sh)
- [`02_run_docker_bash.sh`](02_run_docker_bash.sh)
- [`02_run_infer.sh`](02_run_infer.sh)
- [`03_ranking.sh`](03_ranking.sh)
- [`04_housekeep.sh`](04_housekeep.sh)

## What’s included

- `ds_utils/` contains training, tuning, validation, ensembling, and neutralization code for scikit-learn compatible models such as LightGBM, XGBoost, and CatBoost.
- `numerai_utils/` contains Numerai API helpers.
- `script/` contains data, research, and inference entry points, including the historical weekly inference workflow.

The original project recorded historical leaderboard results for [`ct_balance`](https://numer.ai/ct_balance). See the [Numerai documentation](https://docs.numer.ai/) for current Tournament instructions.

## License

The repository is licensed under [Apache License 2.0](LICENSE).
