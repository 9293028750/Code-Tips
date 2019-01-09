import Mapplotlib.pyplot as plt

#############
plt.subplots
#############

fig, axes = plt.subplots(5, sharey=True, figsize=(5, 10))
axes[0].plot(df_2010['date'],df_2010['pm2.5'])
axes[1].plot(df_2011['date'],df_2011['pm2.5'])
axes[2].plot(df_2012['date'],df_2012['pm2.5'])
axes[3].plot(df_2013['date'],df_2013['pm2.5'])
axes[4].plot(df_2014['date'],df_2014['pm2.5'])
for ax in axes:
    ax.set_xlabel('data')
    ax.set_ylabel('pm2.5')


fig, ax = plt.subplots()
_ = df['Survived'].value_counts().plot.bar(ax=ax)
_ = ax.set_xticklabels(['died', 'survived'])