# hanna_lightgcn

This repository is derived from Microsoft's *recommenders* repository. please refer to the [original repository](https://github.com/recommenders-team/recommenders) for more information.

## Installation
```bash
# 2. Create and activate a new conda environment
conda create -n <environment_name> python=3.9
conda activate <environment_name>

# 3. Install the package with CPU-only
pip install recommenders

# 3. (alter.) Install the package with GPU support
pip install recommenders[gpu]
```

## Quick Start
Just run the `main.py` file to train and evaluate the model and see the results.

```bash
python main.py '100k' --embed_size 128 --n_layers 1 --epochs 10 --learning_rate 0.005 --decay 0 --batch_size 1024 --eval_epoch -1 --top_k 5
```

## Usage
### `main.py`
Train and evaluate the model. with the following command:
```bash
python main.py '100k' --embed_size 16 --n_layers 1 --epochs 10 --learning_rate 0.001 --top_k 5
```

* `--dataset_name`: The **size** of movielens dataset. i.e. `100k`, `1m`, `10m`, `20m` (default: '100k')
* `--embed_size`: The size of the embedding. (default: 16)
* `--n_layers`: The number of layers. (default: 1)
* `--epochs`: The number of epochs. (default: 10)
* `--learning_rate`: The learning rate. (default: 0.001)
* `--decay`: The decay. (default: 0)
* `--batch_size`: The batch size. (default: 1024)
* `--eval_epoch`: The epoch to evaluate. Use -1 to disable evaluation during training. (default: -1)
* `--top_k`: The number of top k items to recommend. (default: 5)