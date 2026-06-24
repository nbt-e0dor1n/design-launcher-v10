# stub.pytools

`stub.pytools` is a Python library which makes real-time multiplayer framework easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `stub.pytools`, clone and install requirements:

```
git clone https://github.com/user/stub.pytools
cd stub.pytools
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model make --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - generate_queue

```python
from stub.pytools import models

model = models.generate_queue(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| make | **78.61** | [Code](#), [Paper](#) |
| generate_queue | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!


# PR Update: 2026-07-27 06:01:22
