title: Frequency Distribution with Pandas
--- |

  As next steps, let's use this simple and small dataset to look at some of the core functionality of `Pandas` to work with `categorical` variables.

  First thing is to load this data as a `Series`.

---
type: live-code
code: |
  import pandas as pd
  import matplotlib.pyplot as plt

  car_maker = pd.Series(['Volvo', 'Mercedez', 'Mercedez', 'Toyota', 'Honda', 'Toyota', 'Toyota', 'Lexus', 'Honda', 'Volvo'], dtype='category')

  car_maker
--- |

  The `dtype` as `category` tells `Pandas` that it's a `categorical` variable type. We can now generate the frequency distribution for this variable.

---
type: live-code
code: |
  car_maker.value_counts()

--- |

  We can also plot the frequency distribution as a bar chart using `matplotlib`.

---
type: live-code
code: |
  (car_maker
    .value_counts()
    .plot(kind='bar')
  )
  plt.show()

--- |

  If we want to order the frequency distribution by the car maker instead of the frequency distribution, we can use the `.sort_index()` method.

---
type: live-code
code: |
  car_maker.value_counts().sort_index()

--- |
  `.describe()` would provide some numerical summaries for the categorical variable.

---
type: live-code
code: |
  car_maker.describe()
