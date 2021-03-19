# Python Library Handbook

A comprehensive list of Good Python Libraries™ according to me.

Here we go!

## Bidict

Always-invertible dicts / bijections as a data generic structure. [Github](https://github.com/jab/bidict9) and [Pypi](https://pypi.org/project/bidict/)

## LXML

Powerful XML library.

## Networkx

[Networkx](https://networkx.org/) is a great library for data in graph/network form. 

## NumPy

Needs no explanation.

## Pandas

Tables and stuff.

## Progressbar2

Nice and simple progress bars. Progressbar https://pypi.org/project/progressbar2/)

```
import progressbar
for item in progressbar.progressbar(range(10)):
  pass
```

## Seaborn

Quick and pretty visualizations of data in pandas dataframe format.


```
import seaborn as sns

example_dataframe = pd.read_csv("example_data.csv")

sns.set_theme()
sns.relplot(
    data=example_dataframe,
    x="date", y="quantity_in_question", kind="line",
    facet_kws=dict(sharex=False),
)

plt.show()
```
