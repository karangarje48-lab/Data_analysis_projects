import pandas as pd
import plotly.express as px

df = pd.read_csv('covid_data.csv')
df['date'] = pd.to_datetime(df['date'])

fig = px.choropleth(df, locations='iso_code',
                    color='total_cases',
                    hover_name='location',
                    animation_frame='date',
                    title='Global Covid-19 Cases Over Time')
fig.show()
