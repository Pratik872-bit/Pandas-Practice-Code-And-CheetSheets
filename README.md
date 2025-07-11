# Pandas-Practice-Code-And-CheetSheets
PANDAS CHEAT SHEET
----------------------
1. Import Pandas
import pandas as pd

2. Create DataFrame
pd.DataFrame(data)

3. Read/Write Files
pd.read_csv("file.csv")
df.to_csv("file.csv", index=False)
pd.read_excel("file.xlsx")
df.to_excel("file.xlsx", index=False)
pd.read_json("file.json")
df.to_json("file.json", orient="records")

4. DataFrame Info
df.head(), df.tail()
df.info(), df.describe()
df.shape, df.columns, df.dtypes

5. Selecting Data
df['col'], df[['col1', 'col2']]
df.loc[row_index, col_name]
df.iloc[row_index, col_index]

6. Filtering Rows
df[df['Age'] > 25]
df[(df['Gender'] == 'Male') & (df['Score'] > 80)]

7. Sorting & Ranking
df.sort_values('Score', ascending=False)
df.sort_index()

8. Handling Missing Values
df.isnull(), df.notnull()
df.dropna(), df.fillna(value)

9. Aggregation & Grouping
df.sum(), df.mean(), df.count(), df.max()
df.groupby('Gender')['Score'].mean()

10. Merging & Joining
pd.merge(df1, df2, on='key')
df1.join(df2, on='index')

11. Concatenation
pd.concat([df1, df2], axis=0)

12. Pivot Tables & Crosstab
df.pivot_table(values='val', index='col1', columns='col2')
pd.crosstab(df['col1'], df['col2'])

13. Apply & Lambda
df['new'] = df['col'].apply(lambda x: x * 2)

14. Encoding
from sklearn.preprocessing import LabelEncoder, OneHotEncoder

15. Exporting
df.to_csv(), df.to_excel(), df.to_json()

16. Reset/Set Index
df.reset_index(), df.set_index('col')

17. Drop Columns/Rows
df.drop('col', axis=1)
df.drop(index=2)

18. Value Counts & Unique
df['col'].value_counts()
df['col'].unique()

19. Replace & Map
df['col'].replace({old: new})
df['col'].map({'A': 1, 'B': 2})

20. Rename Columns
df.rename(columns={'old': 'new'})