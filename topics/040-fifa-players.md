title: FIFA Players
--- |
  We'll continue with the theme of working with categorical variables in the context of a real dataset. The dataset for this exercise is for [FIFA Players](https://www.kaggle.com/artimous/complete-fifa-2017-player-dataset-global/data). You can download the data from [this location](assets/data/fifa-players.csv) for offline use.

  First, let's load the dataset. We'll look at two categorical variables in this dataset: `Nationality` & `Club`.

---
type: live-code
code: |
  import pandas as pd
  import matplotlib.pyplot as plt

  df = pd.read_csv('assets/data/fifa-players.csv')
  df[ ['Nationality', 'Club'] ]

---
type: coding-question
question: Write the code to convert `Nationality` and `Club` columns to `CategoricalDtype`.
code: |
  from pandas.api.types import CategoricalDtype

  # your code goes here.

tests: |
  assert isinstance( df['Nationality'].dtype, CategoricalDtype)
  assert isinstance( df['Club'].dtype, CategoricalDtype)
solution: |
  from pandas.api.types import CategoricalDtype

  df['Nationality'] = df['Nationality'].astype('category')
  df['Club'] = df['Club'].astype('category')

---
type: fill-in-the-blank-question
question: Answer the following questions for the variable `Club` and `Nationality`.
code: |
  # You can write code here.

blanks:
  - label: How many unique values are present for `Club`?
    answer: 634
  - label: How many unique values are present for `Nationality`?
    answer: 160
  - label: Which country are the maximum players from?
    answer: England
  - label: How many players from Argentina?
    answer: 1097
