import seaborn as sns

########
heatmap
########
plt.figure(figsize=(9,9))
sns.heatmap(mat.T, annot=True, fmt=".3f", linewidths=.5, square = True, cmap = 'Blues_r',
            xticklabels=digits.target_names,
            yticklabels=digits.target_names)
plt.xlabel('actual label')
plt.ylabel('predicted label');


all_sample_title = 'Accuracy Score: {0}'.format(score)
plt.title(all_sample_title, size = 15);


########
pairplot
######## 
sns.set(style="ticks")
sns.pairplot(pdata)


########
scatterplot
########
sns.scatterplot(x='principal component 1', y='principal component 2', hue='target', data=principalDf)