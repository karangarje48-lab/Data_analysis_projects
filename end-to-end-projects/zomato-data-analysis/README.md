import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv('zomato.csv')
df.dropna(inplace=True)

# Top cuisines
top_cuisines = df['cuisines'].value_counts().head(10)
sns.barplot(x=top_cuisines.values, y=top_cuisines.index)
plt.title('Top 10 Cuisines on Zomato')
plt.show()
