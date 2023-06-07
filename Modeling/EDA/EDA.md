[참고](https://dacon.io/competitions/open/235671/codeshare/2006)

### Sentence 수 시각화 
```python
original_sent_counts = []
for i in range(len(df['content'])):
    original_sent_counts.append(len(df['content'][i].split('.')))
    
fig, axs = plt.subplots(1, 2, figsize=(16, 6), gridspec_kw=dict(width_ratios=[4, 3]))
sns.histplot(original_sent_counts, binwidth=1, ax=axs[0])
sns.boxplot(original_sent_counts, ax=axs[1])
```

### Word 수 시각화 
```python
original_word_counts = []
for i in range(len(df['content'])):
    original_word_counts.append(len(df['content'][i].split(' ')))
    
fig, axs = plt.subplots(1, 2, figsize=(16, 6), gridspec_kw=dict(width_ratios=[4, 3]))
sns.histplot(original_sent_counts, binwidth=1, ax=axs[0])
sns.boxplot(original_sent_counts, ax=axs[1])
```