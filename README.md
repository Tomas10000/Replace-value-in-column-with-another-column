#Replace-value-in-column-with-another-column


#data frame 1

d1 = {'Name':pd.Series(['Dam','Manu','Owen','Max','Liam','William']),'Phone1':pd.Series([755233315,522245315,561237894,743625792,123451239,321659841]),'Phone2':pd.Series([755238815,522214315,561234494,333625792,123451212,321656641])}

df1 = pd.DataFrame(d1)

df1

#data frame 1

df2 = {'Exclude':pd.Series([123451239,333625792])}

df2 = pd.DataFrame(df2)

df2


import numpy as np

df1["Phone1_s"] = list(map(lambda x: "X" if x else "A", np.in1d(df1.Phone1, df2.Exclude)))

df1["Phone2_s"] = list(map(lambda x: "X" if x else "A", np.in1d(df1.Phone2, df2.Exclude)))

df1
