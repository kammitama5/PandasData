

```python
import pandas as pd
```


```python
df = pd.read_csv('cars.csv')
df.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>YEAR</th>
      <th>Make</th>
      <th>Model</th>
      <th>Size</th>
      <th>(kW)</th>
      <th>Unnamed: 5</th>
      <th>TYPE</th>
      <th>CITY (kWh/100 km)</th>
      <th>HWY (kWh/100 km)</th>
      <th>COMB (kWh/100 km)</th>
      <th>CITY (Le/100 km)</th>
      <th>HWY (Le/100 km)</th>
      <th>COMB (Le/100 km)</th>
      <th>(g/km)</th>
      <th>RATING</th>
      <th>(km)</th>
      <th>TIME (h)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2012</td>
      <td>MITSUBISHI</td>
      <td>i-MiEV</td>
      <td>SUBCOMPACT</td>
      <td>49</td>
      <td>A1</td>
      <td>B</td>
      <td>16.9</td>
      <td>21.4</td>
      <td>18.7</td>
      <td>1.9</td>
      <td>2.4</td>
      <td>2.1</td>
      <td>0</td>
      <td>n/a</td>
      <td>100</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2012</td>
      <td>NISSAN</td>
      <td>LEAF</td>
      <td>MID-SIZE</td>
      <td>80</td>
      <td>A1</td>
      <td>B</td>
      <td>19.3</td>
      <td>23.0</td>
      <td>21.1</td>
      <td>2.2</td>
      <td>2.6</td>
      <td>2.4</td>
      <td>0</td>
      <td>n/a</td>
      <td>117</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2013</td>
      <td>FORD</td>
      <td>FOCUS ELECTRIC</td>
      <td>COMPACT</td>
      <td>107</td>
      <td>A1</td>
      <td>B</td>
      <td>19.0</td>
      <td>21.1</td>
      <td>20.0</td>
      <td>2.1</td>
      <td>2.4</td>
      <td>2.2</td>
      <td>0</td>
      <td>n/a</td>
      <td>122</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013</td>
      <td>MITSUBISHI</td>
      <td>i-MiEV</td>
      <td>SUBCOMPACT</td>
      <td>49</td>
      <td>A1</td>
      <td>B</td>
      <td>16.9</td>
      <td>21.4</td>
      <td>18.7</td>
      <td>1.9</td>
      <td>2.4</td>
      <td>2.1</td>
      <td>0</td>
      <td>n/a</td>
      <td>100</td>
      <td>7</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2013</td>
      <td>NISSAN</td>
      <td>LEAF</td>
      <td>MID-SIZE</td>
      <td>80</td>
      <td>A1</td>
      <td>B</td>
      <td>19.3</td>
      <td>23.0</td>
      <td>21.1</td>
      <td>2.2</td>
      <td>2.6</td>
      <td>2.4</td>
      <td>0</td>
      <td>n/a</td>
      <td>117</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>




```python
import numpy as np
df.pivot_table(values='(kW)', index='YEAR', columns='Make', aggfunc=np.mean)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>Make</th>
      <th>BMW</th>
      <th>CHEVROLET</th>
      <th>FORD</th>
      <th>KIA</th>
      <th>MITSUBISHI</th>
      <th>NISSAN</th>
      <th>SMART</th>
      <th>TESLA</th>
    </tr>
    <tr>
      <th>YEAR</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2012</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>107.0</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>280.000000</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>NaN</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>268.333333</td>
    </tr>
    <tr>
      <th>2015</th>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>320.666667</td>
    </tr>
    <tr>
      <th>2016</th>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>409.700000</td>
    </tr>
  </tbody>
</table>
</div>




```python
#print(pd.pivot_table(Bikes, index=['Manufacturer','Bike Type']))
```


```python
df.pivot_table(values='(kW)', index='YEAR', columns='Make',aggfunc=[np.mean,np.min], margins=True)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="9" halign="left">mean</th>
      <th colspan="9" halign="left">amin</th>
    </tr>
    <tr>
      <th>Make</th>
      <th>BMW</th>
      <th>CHEVROLET</th>
      <th>FORD</th>
      <th>KIA</th>
      <th>MITSUBISHI</th>
      <th>NISSAN</th>
      <th>SMART</th>
      <th>TESLA</th>
      <th>All</th>
      <th>BMW</th>
      <th>CHEVROLET</th>
      <th>FORD</th>
      <th>KIA</th>
      <th>MITSUBISHI</th>
      <th>NISSAN</th>
      <th>SMART</th>
      <th>TESLA</th>
      <th>All</th>
    </tr>
    <tr>
      <th>YEAR</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2012</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>64.500000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>49.0</td>
    </tr>
    <tr>
      <th>2013</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>107.0</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>280.000000</td>
      <td>158.444444</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>107.0</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>270.0</td>
      <td>35.0</td>
    </tr>
    <tr>
      <th>2014</th>
      <td>NaN</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>268.333333</td>
      <td>135.000000</td>
      <td>NaN</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>NaN</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>225.0</td>
      <td>35.0</td>
    </tr>
    <tr>
      <th>2015</th>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>320.666667</td>
      <td>181.428571</td>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>280.0</td>
      <td>35.0</td>
    </tr>
    <tr>
      <th>2016</th>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>409.700000</td>
      <td>252.263158</td>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>283.0</td>
      <td>35.0</td>
    </tr>
    <tr>
      <th>All</th>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>345.478261</td>
      <td>190.622642</td>
      <td>125.0</td>
      <td>104.0</td>
      <td>107.0</td>
      <td>81.0</td>
      <td>49.0</td>
      <td>80.0</td>
      <td>35.0</td>
      <td>225.0</td>
      <td>35.0</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
