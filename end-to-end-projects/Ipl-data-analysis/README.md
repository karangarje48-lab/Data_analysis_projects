import pandas as pd
import matplotlib.pyplot as plt

matches = pd.read_csv('matches.csv')

# Most wins by team
team_wins = matches['winner'].value_counts().head(8)
team_wins.plot(kind='bar', color='orange', figsize=(10,5))
plt.title('IPL Team Win Count')
plt.xlabel('Team')
plt.ylabel('Wins')
plt.show()
