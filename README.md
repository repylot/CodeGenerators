<h1 align="center">RePylot: Fine Tuning GPT-2</h1>
<p align="center"><img src="resources/repylot_logo.png" width="7%"/></p>

This repository contains several GPT2 fine-tuned models retrained using several programming language scripts, so as to serve as an engine for RePylot Code Generator. The code provided allows you to train GPT-2 on a custom dataset to generate text specific to your needs.

<br>

## Python Code Generator

We asked the fine-tuned model to complete `from matplotlib`. We obtained the following result

```python
from matplotlib.animation import pyplot as plt, cvars
import pformat as
```

Meanwhile, the original GPT-2 model itself returned the next sequence

```python
from matplotlib, matplotlib.min.js <~ matplotlib.min.js >) >\n\nNote: Matplot
```
which is not even a Python statement.

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

### How to use

You can easily run one of the given notebooks in the `python` directory to generate your code. There, you must look for the **Model Evaluation** section, and run the chunk containing the following code:

```python
sequence = "for i, element"
generate_text(output_dir, sequence, extra_length=20)
```

where you can modify the `sequence` variable. This will print the model generation, in this case:

```python
for i, element_name in enumerate(value_list)):
  r = random.randrange
```

<br>

## Requirements

Before running the scripts or notebook, please make sure you install the `transformers`' dependency. To do so, feel free to make use of the next command:

```bash
pip install transformers
```

Or simply add the next line at the beginning of your Python script

```python
!pip install transformers
```

Also, you will need to have PyTorch installed, since this is what `transformers`' models are based in. You can install this framework using this [link](https://pytorch.org/get-started/locally/).
