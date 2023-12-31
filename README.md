# LoadMe
This is a helper to load data generated by [MeasureMe](https://github.com/spxtr/measureme)

# Installation
Modified from MeasureMe.

Installing python projects can be a real pain. Here is how I personally set up lab computers to use measureme, but other ways can work fine. I do not like to use tools such as Conda or pipenv, because I find them to be a real headache.

1. On Windows computers I typically use GitHub Desktop for git.
2. I install the latest Python 3 from python.org, system wide. I make sure that I can run Python from the command line. On Windows this sometimes means running py or py3 or python3. I feel like it changes every time I do it, so just try them all and see what sticks. Later versions of Windows will annoyingly pop up some app store if you don't use the right incantation. Ignore that nonsense.
3. Next, make sure pip exists with python -m ensurepip. Again, pip might have some odd path like pip3.
4. Download and install loadme. Git clone, then pip install -e.
5. Test loadme by following the basic usage section below!

# Basic usage

Start by importing sweep_load

```python
import sweep_load
```

To quickly check the metadata of a measurement file, we can load it in by specifying the path to the file and the sweep id:

```python
metadata = sweep_load.load_meta('/path/to/data/directory', 1)
```

The simplest way to load in data is to use ```load```

```python
data = sweep_load.load('/path/to/data/directory', 1)
```

which returns and ndarray. If we want to load the data in a slightly fancier way we can use ```pload1d``` or ```pload2d```, which returns dictionaries where the keys are given by the metadata. 

```python
data = sweep_load.pload2d('/path/to/data/directory', 1)
```

To quickly check all the fields in the data file (without using ```load_meta```):

```python
print(data.keys())
```
