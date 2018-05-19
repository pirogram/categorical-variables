title: Identify Categorical Variables
--- |

  You can't compare `apples` with `oranges` because `fruit` is a categorical variable. Different values of the `fruit` variable are just different. One is neither more nor less from the other.

  The categorical variables are qualitative in nature. They do not signify the _quantity_ of something.

---
type: multiple-choice-question
question: |
  In the following dataset, which variables are categorical?

  | city | max_temp | min_temp |
  | - | - | - |
  | Bengaluru | 35 | 28 |
  | San Francisco | 18 | 11 |
options:
  - text: city
    correct: true
  - text: max_temp
  - text: min_temp

---
type: multiple-choice-question
question: |
  In the following dataset, which variables are categorical?

  | Item Type | City | Sale Price (USD) |
  | - | - | - |
  | 1 | San Francisco | 25 |
  | 1 | Los Angeles | 24 |
  | 2 | San Francisco | 12 |
  | 2 | Los Angeles | 13 |

  Remember, a categorical variable doesn't have to be a string!
options:
  - text: Item Type
    correct: true
  - text: City
    correct: true
  - text: Sale Price (USD)

--- |

  ## Ordered Categoricals

  Some variables look like `quantitative` but are actually `categorical`. Consider the ratings of an item on Amazon.com.

  ![](assets/img/amazon-ratings.png)

  These ratings broadly represent the quantity of satisfaction people had from their purchase. We can say that 5 star rating is more than 4 star rating which is more than 3 star rating. However, can we say that the difference between 5 and 4 star rating is same as 4 and 3 star rating?

  While the amazon rating looks like a `quantitative` variable because it represents a quantity, it is actually a `categorical` variable where the categories are ordered. We can call these kind of variables `ordered categorical` or `ordinal categorical` or just `ordinal`.

  Ordinal number means a number defining a thing's position in a series, such as “first,” “second,” or “third.” Ordinal numbers are used as adjectives, nouns, and pronouns.

  The previous categoricals that we looked at are called `nominal categoricals` or just `nominal` or just `categorical`. Nominal means existing in name only.

  What are other examples of `ordered categoricals` (aka `ordinals`)? Pretty much all variables that represent the quantity of an abstract thing are `ordered categoricals`. How happy are you? How gloomy is the weather? How good is this car?

---
type: multiple-choice-question
question: |
  Consider the following dataset about House Sale. Which variables are `ordered categoricals`?

  | Street | Sqft | Number of Bedrooms | Number of Bathrooms | Condition | Price |
  | - | - | - | - | - | - |
  | Johnson Ave | 1500 | 3 | 2 | like new | 200,000 |
  | Bollinger Rd | 1250 | 2 | 2 | very old | 100,000 |
  | Larry Way | 1600 | 4 | 1 | new | 250,000 |
options:
  - text: Street
  - text: Sqft
  - text: Number of Bedrooms
  - text: Number of Bathrooms
  - text: Condition
    correct: true
  - text: Price
