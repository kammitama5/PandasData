

```python
# ratio => 
# units are equally spaced
# mathematical operations of +-/* are all valid

```


```python
# Interval =>
# units are equally spaced, but there is no true zero
```


```python
# Ordinal scale
# the order of the units is important, but not evenly spaced
# Letter grades such as A+, A are a good example
```


```python
#Nominal Scale
# categories of data, but the categories have no order with respect to one another
# eg. teams of a sport
```


```python
import pandas as pd
df = pd.DataFrame(['A+', 'A', 'A-', 'B+', 'B', 'B-', 'C+', 'C','C-', 'D+','D'],
                 index=['excellent','excellent','excellent','good','good','good','ok','ok','ok','poor','poor'])
df.rename(columns={0:'Grades'}, inplace=True)
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Grades</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>excellent</th>
      <td>A+</td>
    </tr>
    <tr>
      <th>excellent</th>
      <td>A</td>
    </tr>
    <tr>
      <th>excellent</th>
      <td>A-</td>
    </tr>
    <tr>
      <th>good</th>
      <td>B+</td>
    </tr>
    <tr>
      <th>good</th>
      <td>B</td>
    </tr>
    <tr>
      <th>good</th>
      <td>B-</td>
    </tr>
    <tr>
      <th>ok</th>
      <td>C+</td>
    </tr>
    <tr>
      <th>ok</th>
      <td>C</td>
    </tr>
    <tr>
      <th>ok</th>
      <td>C-</td>
    </tr>
    <tr>
      <th>poor</th>
      <td>D+</td>
    </tr>
    <tr>
      <th>poor</th>
      <td>D</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['Grades'].astype('category').head()
```




    excellent    A+
    excellent     A
    excellent    A-
    good         B+
    good          B
    Name: Grades, dtype: category
    Categories (11, object): [A, A+, A-, B, ..., C+, C-, D, D+]




```python
grades = df['Grades'].astype('category', 
                            categories = ['D','D+','C-','C','C+','B-','B','B+','A-','A','A+'],
                            ordered=True)
grades.head()
```




    excellent    A+
    excellent     A
    excellent    A-
    good         B+
    good          B
    Name: Grades, dtype: category
    Categories (11, object): [D < D+ < C- < C ... B+ < A- < A < A+]




```python
grades > 'C'
```




    excellent     True
    excellent     True
    excellent     True
    good          True
    good          True
    good          True
    ok            True
    ok           False
    ok           False
    poor         False
    poor         False
    Name: Grades, dtype: bool




```python
# s = pd.Series(['Low','Low','High','Medium','Low','High','Low'])
# s.astype('category', categories=['Low', 'Medium','High'], ordered=True)
```


```python
import numpy as np
df = pd.read_csv('census.csv')
df = df[df['SUMLEV'] == 50]
df = df.set_index('STNAME').groupby(level=0)['CENSUS2010POP'].agg({'avg':np.average})
pd.cut(df['avg'], 10)
```




    STNAME
    Alabama                  (11706.0871, 75333.413]
    Alaska                   (11706.0871, 75333.413]
    Arizona                 (390320.176, 453317.529]
    Arkansas                 (11706.0871, 75333.413]
    California              (579312.234, 642309.586]
    Colorado                 (75333.413, 138330.766]
    Connecticut             (390320.176, 453317.529]
    Delaware                (264325.471, 327322.823]
    District of Columbia    (579312.234, 642309.586]
    Florida                 (264325.471, 327322.823]
    Georgia                  (11706.0871, 75333.413]
    Hawaii                  (264325.471, 327322.823]
    Idaho                    (11706.0871, 75333.413]
    Illinois                 (75333.413, 138330.766]
    Indiana                  (11706.0871, 75333.413]
    Iowa                     (11706.0871, 75333.413]
    Kansas                   (11706.0871, 75333.413]
    Kentucky                 (11706.0871, 75333.413]
    Louisiana                (11706.0871, 75333.413]
    Maine                    (75333.413, 138330.766]
    Maryland                (201328.118, 264325.471]
    Massachusetts           (453317.529, 516314.881]
    Michigan                 (75333.413, 138330.766]
    Minnesota                (11706.0871, 75333.413]
    Mississippi              (11706.0871, 75333.413]
    Missouri                 (11706.0871, 75333.413]
    Montana                  (11706.0871, 75333.413]
    Nebraska                 (11706.0871, 75333.413]
    Nevada                  (138330.766, 201328.118]
    New Hampshire            (75333.413, 138330.766]
    New Jersey              (390320.176, 453317.529]
    New Mexico               (11706.0871, 75333.413]
    New York                (264325.471, 327322.823]
    North Carolina           (75333.413, 138330.766]
    North Dakota             (11706.0871, 75333.413]
    Ohio                     (75333.413, 138330.766]
    Oklahoma                 (11706.0871, 75333.413]
    Oregon                   (75333.413, 138330.766]
    Pennsylvania            (138330.766, 201328.118]
    Rhode Island            (201328.118, 264325.471]
    South Carolina           (75333.413, 138330.766]
    South Dakota             (11706.0871, 75333.413]
    Tennessee                (11706.0871, 75333.413]
    Texas                    (75333.413, 138330.766]
    Utah                     (75333.413, 138330.766]
    Vermont                  (11706.0871, 75333.413]
    Virginia                 (11706.0871, 75333.413]
    Washington              (138330.766, 201328.118]
    West Virginia            (11706.0871, 75333.413]
    Wisconsin                (75333.413, 138330.766]
    Wyoming                  (11706.0871, 75333.413]
    Name: avg, dtype: category
    Categories (10, object): [(11706.0871, 75333.413] < (75333.413, 138330.766] < (138330.766, 201328.118] < (201328.118, 264325.471] ... (390320.176, 453317.529] < (453317.529, 516314.881] < (516314.881, 579312.234] < (579312.234, 642309.586]]




```python
# s = pd.Series([168,180, 174, 190, 170, 185, 179, 181, 175, 169, 182, 177, 180, 171  ])
# pd.cut(s, 3)
# You can also add labels for the sizes [Small < Medium < Large].
# pd.cut(s, 3, labels = ['Small', 'Medium', 'Large'])
```
