import pandas as pd
import numpy as np

# create a sample DataFrame with NaN values
df = pd.DataFrame({
    'A': [1, 2, np.nan, 4],
    'B': [5, np.nan, 7, 8],
    'C': [9, np.nan, 11, np.nan]
})

# calculate the mean of each column
# fill NaN values with the mean of each column

df.fillna(df.mean(), inplace=True)
print(df)


          A         B     C
0  1.000000  5.000000   9.0
1  2.000000  6.666667  10.0
2  2.333333  7.000000  11.0
3  4.000000  8.000000  10.0
