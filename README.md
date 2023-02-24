# dflogger

When you feel like any existing experiment tracker tools are overpowered, then dflogger is what you're looking for

## Installation

```bash
pip install dflogger
```

## Usage

Logging experiment parameters and metrics

```python
from dflogger.logger import Logger

dflogger = Logger()

params = {
    "learning_rate": 0.01,
    "epochs": 100
}

metric = {
    "train_acc": 0.6,
    "val_acc": 0.58,
    "train_loss": 0.1,
    "val_loss": 0.15
}

dflogger.log("run_name", params, metric)
```

Getting best score based on a metric

```python
dflogger.best_score("val_acc")
```

Getting best params based on a metric

```python
dflogger.best_params("val_acc")
```

Getting the dataframe log

```python
dflogger.get_df()
```

Saving dataframe

```python
dflogger.to_csv()
```
