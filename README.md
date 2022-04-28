# Python Library Handbook

A comprehensive list of Good Python Libraries™ according to me.

Here we go!

## Argparse

Add easy-to-use args to your app like this

```python
import argparse
parser = argparse.ArgumentParser()
parser.add_argument("--no", type=int, default=12)
parser.add_argument("--pi", type=float, default=3.14)
args = parser.parse_args()
```

This is standard but a nice-to-have clipboard so that you don't need to learn all this by heart.

Use the following line to print out the docstring at the start of the file when you run ```python script.py --help```

```python
parser = argparse.ArgumentParser(description=__doc__)
```

## Bidict

Always-invertible dicts / bijections as a data generic structure. [Github](https://github.com/jab/bidict9) and [Pypi](https://pypi.org/project/bidict/)

```python
from bidict import bidict
element_by_symbol = bidict({'H': 'hydrogen'})

# Works like a normal dict
hydrogen = element_by_symbol['H']

# Also to the inverse direction
H = element_by_symbol.inverse['hydrogen']
```

## LXML

Powerful XML library.

## Networkx

[Networkx](https://networkx.org/) is a great library for data in graph/network form. 

```python
g = nx.Graph()
g.add_edge("dog", "cat")

print(g)
print(g.edges)
print(g.nodes)
```

## NumPy

Needs no explanation.

## Pandas

Tables and stuff.

## Polars

Tables and stuff, with a Rust backend. Feels more idiomatic and functional than Pandas.

```py
import polars as pl

df = pl.read_csv("data.csv")

# Drop rows where name is null
df = df.drop_nulls("name")

# Fill 'number' nulls with 
df = df.select([
  "name",
  pl.col("number").fill_null(-123),
  ])

# Save to file
df.to_csv("polars.csv")
```

## Progressbar2

Nice and simple progress bars. Progressbar https://pypi.org/project/progressbar2/)

```py
import progressbar
for item in progressbar.progressbar(range(10)):
  pass
```

## Seaborn

Quick and pretty visualizations of data in pandas dataframe format.


```py
import seaborn as sns
from matplotlib import pyplot as plt

example_dataframe = pd.read_csv("example_data.csv")

sns.set_theme()
sns.relplot(
    data=example_dataframe,
    x="date", y="quantity_in_question", kind="line",
    facet_kws=dict(sharex=False),
)

plt.show()
```
