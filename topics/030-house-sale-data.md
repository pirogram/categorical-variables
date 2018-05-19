title: House Sale Data
--- |

  In this example, we'll work with [House Sale Data](https://www.kaggle.com/harlfoxem/housesalesprediction/data) from King County. If you wish, you can download the [csv file](assets/data/kc_house_data.csv) to work offline.

  First, load the data.

---
type: live-code
code: |
  import pandas as pd

  df = pd.read_csv('assets/data/kc_house_data.csv')

--- |

  In this dataset, there are three categorical variables: `zipcode`, `condition` and `grade`. Let's look at frequency distribution of `condition` variable and find out whether it is a `nominal` or `ordinal` variable.

---
type: live-code
code: |
  df['condition'].value_counts().sort_index()

--- |

  `condition` seems to be an `ordinal` variable with 5 possible values. It's difficult to say based on the dataset whether condition `1` is better or `5` is better. Let's make the assumption that `5` represents best and `1` represents worst.

---
type: categorization-question
question: |
  Can you assess the type of `zipcode` and `grade` variables? Look at their possible values and choose the right variable type for them.
code: |
  # you can write code here.

mappings:
  zipcode: Nominal Categorical
  grade: Ordinal Categorical

--- |

  The current `dtype` for `zipcode`, `condition` and `grade` is `int`. We can verify it here:

---
type: live-code
code: |
  df[ ['zipcode', 'condition', 'grade'] ].dtypes

--- |

  A good practice would be to update our data frame so that it has the correct `dtype` for these variables.

---
type: live-code
code: |
  from pandas.api.types import CategoricalDtype

  df['zipcode'] = df['zipcode'].astype('category')
  df['condition'] = df['condition'].astype(CategoricalDtype(ordered=True))
  df['grade'] = df['grade'].astype(CategoricalDtype(ordered=True))

  df[ ['zipcode', 'condition', 'grade'] ].dtypes

--- |
  Let's solve some problems now.

---
type: fill-in-the-blank-question
question: |
  Look at the frequency distribution of `condition` variable and answer the following questions.
code: |
  # you can write code here.

blanks:
  - label: What's the number of unique conditions?
    answer: 5
  - label: Which condition has maximum frequency?
    answer: 3
  - label: How many houses have condition 5?
    answer: 1701

---
type: fill-in-the-blank-question
question: |
  Look at the frequency distribution of `zipcode` variable and answer the following questions.
code: |
  # you can write code here.

blanks:
  - label: What's the number of unique zipcodes?
    answer: 70
  - label: Which zipcode has maximum house sale data?
    answer: 98103
