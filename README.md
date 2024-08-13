<h1 align="center">GPT-2 Python Fine-Tuning</h1>

This repository contains several GPT2 fine tuned models retrained using several programming languages scripts, so as to serve as an engine to RePylot Code Generator. The code provided allows you to train GPT-2 on a custom dataset to generate text specific to your needs.

<br>

## Python Code Generator

Whithin 5 single epochs, we asked the fine tuned model to complete `from matplotlib`. We obtained the following result

```python
from matplotlib.animation import pyplot as plt, cvars
import pformat as
```

Meanwhile, the original GPT-2 model itself return the next sequence

```python
from matplotlib, matplotlib.min.js <~ matplotlib.min.js >) >\n\nNote: Matplot
```
which is not even a python statement.

<br>

Furthermore, we asked RePylot to complete the sequence `for key`, and returned the next result

```python
for key in zip(*generate_pair(n, n - key + 1, i), j
```

On the other hand, GPT-2 returned

```
for keyframes and transitions between keyframes), and a series of options to allow for different
```

Not even a programming language.

<br>

## Requirements

Before running the scripts or the notebook, ensure you have the transformers dependency installed. To do so, feel free to make use of the next command:

```bash
pip install transformers
```

Or simply add the next line at the beginning of your python script

```python
!pip install transformers
```
