import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv('airbnb_listings.csv')
df['price'] = df['price'].str.replace('$','').str.replace(',','').astype(float)

sns.boxplot(x='room_type', y='price', data=df[df['price']<500])
plt.title('Price Distribution by Room Type')
plt.show()
