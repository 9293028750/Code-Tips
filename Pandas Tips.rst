import pandas as pd

#############
load data
#############

df=pd.read_csv(url, names=names)

#############
pd.DataFrame
#############

bc_df = pd.DataFrame(
    dict(
        zip(bcdata['feature_names'], list(bcdata.data.T))
    )

#############
clean data
#############

df = df.dropna()

################################
convert categorical to numberic
################################

df['cbwd'] = pd.get_dummies(df['cbwd'])

############
to_datetime
############

df['date'] = pd.to_datetime(df[['year','month','day','hour']])
df_2010 = df[df['year'] == 2010]
df_2011 = df[df['year'] == 2011]
df_2012 = df[df['year'] == 2012]
df_2013 = df[df['year'] == 2013]
df_2014 = df[df['year'] == 2014]


############
value_counts
############
df['Survived'].value_counts()

############
df.groupby()
############
subset[['Sex','Survived','PassengerId']].groupby(['Sex','Survived']).count()

############
series.str.contains("")
############
subset['Sex'].str.contains('female'))
subset['Sex'].str.match('female'))