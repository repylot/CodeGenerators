<h1 align="center">RePylot: Fine Tuning GPT-2</h1>
<p align="center"><img src="resources/repylot_logo.png" width="7%"/></p>

This repository contains several GPT2 fine-tuned models retrained using several programming language scripts, so as to serve as an engine for RePylot Code Generator. The code provided allows you to train GPT-2 on a custom dataset to generate text specific to your needs.

<br>

## Index
- Python Code Generator
- Java Code Generator
- How to use
- Requirements

<br>

# Python Code Generator

We asked the fine-tuned model to complete `from matplotlib import`. We obtained the following result

```python
from matplotlib import pyplot as plt
from sklearn.metrics import accuracy
```

Meanwhile, the original GPT-2 model itself returned the next sequence

```python
from matplotlib, matplotlib.min.js <~ matplotlib.min.js >) >\n\nNote: Matplot
```
which is not even a Python statement.

<br>

Other examples:

```
Prompt:  for key
```
```python
for key in key.values():
  if self.open_file(filename): # get the OpenPG
```

<br>

```
Prompt:  def inverse_sort(list, number):
```
```python
def inverse_sort(list, number):
  return [list[float] for _ in range(number)]

def inverse_sort(list, number):
  return []
```

<br>

```
Prompt:  if (a ==
```
```python
if (a == a[0]) 
  # check if the queue is empty 
  assert len(a)!=

```

<br>

## Java Code Generator

We asked the fine-tuned model to complete `public class`. We obtained the following result

```java
public class CityTests {
  @Test
  void defaultPropertyPlaceholders() {
    this.contextRunner.run
```

Meanwhile, the original GPT-2 model itself returned the next sequence

```
public class Bool is a constructor function that provides an argument that you can use to define new value types for your classes:\n\nclass Bool'}]
```

<br>

Other examples:

```
Prompt:  import
```
```java
import org.springframework.boot.actuate.endpoint.annotation.Endpoint;
import
```

<br>

```
Prompt:  public static void
```
```java
public static void main(String[] args) {
  String description = "The user name is: %s
```

<br>

```
Prompt:  @Override
```
```java
  @Override
  public String toString() {
    return this.name;
  }
}
 /* * Copyright 2012-
```

<br>

## How to use

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
You can also use the web version by entering into [repylot website](https://repylot.github.com)

https://github.com/user-attachments/assets/838e2b45-ba97-412e-bac9-9ae31021c195

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
