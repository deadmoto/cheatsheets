# Seaborn

`import seaborn as sns`

## Plots

### Histogram

`sns.distplot(df['foo'], bins=16, label='foo')`

### Scatter plot

`sns.regplot(x="Wingspan", y="Height", data=df)`

### Linear plot

`sns.lmplot(x="Wingspan", y="CWDistance", data=df, hue="Gender")`

### Bins

```
bins = np.linspace(df.age.min(), df.age.max(), 10)
g = sns.FacetGrid(df, col="Gender", hue="loan_status", palette="Set1")
g.map(plt.hist, 'Gender', bins=bins, ec="k")
```

### Boxplot

```
plt.figure(figsize=(12, 4))
a = sns.boxplot(db.DMDMARTLx, db.RIDAGEYR)
```

### Heatmap

```python
corr = df.corr()
sns.heatmap(corr, xticklabels=corr.columns, yticklabels=corr.columns)
```

### Violin plot

```
plt.figure(figsize=(12, 4))
a = sns.violinplot(da.DMDMARTLx, da.RIDAGEYR)
```

## Plot parameters

### Plot size

`sns.regplot(x='x', y='y', data=df, aspect=48/16)`
