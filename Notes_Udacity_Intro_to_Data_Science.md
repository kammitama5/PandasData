

```python
import pandas as pd
```


```python
# Data Acquisition
# Accessing an API
# Scraping a web page
# Combine data from different formats

```


```python
# CSV: Comma Separated Values

```


```python
## Representing a CSV as a list of rows

# Option 1: Each row is a list
csv = [['A1', 'A2', 'A3'],
      ['B2', 'B2', 'B3']]
```


```python
csv
```




    [['A1', 'A2', 'A3'], ['B2', 'B2', 'B3']]




```python
# Option 2: Each row is a dictionary
# Works well if your csv has a header
# Keys can be column names, fields can be values

# Overall structure would be a list of dictionaries
```


```python
'''
import unicodecsv

enrollments = [] => create list of enrollments
f - open('enrollments.csv', 'rb') => open the file => b flag changes doc
reader = unicodecsv.DictReader(f) => dict since has header row

for row in reader:
    enrollments.append(row) => iterator used for loop to access each element once
    
    => you can only access iterator once
    
f.close() => close file

enrollments[0] => output 
'''
         
```




    "\nimport unicodecsv\n\nenrollments = []\nf - open('enrollments.csv', 'rb')\nreader = unicodecsv.DictReader(f)\n\nfor row in reader:\n    enrollments.append(row)\n    \nf.close()\n\nenrollments[0]\n"




```python
'''
More succinct version

import unicodecsv

enrollments = []
with open('enrollments.csv', 'rb') as f:
    reader = unicodecsv.DictReader(f)
    
    for row in reader:
        enrollments.append(row)
        
enrolmments[0]


'''
```




    "\nMore succinct version\n\nimport unicodecsv\n\nenrollments = []\nwith open('enrollments.csv', 'rb') as f:\n    reader = unicodecsv.DictReader(f)\n    \n    for row in reader:\n        enrollments.append(row)\n        \nenrolmments[0]\n\n\n"




```python
'''
=> converting iterator to a list


import unicodecsv

with open('enrollments.csv', 'rb') as f:
    reader = unicodecsv.DictReader(f)
    enrollments = list(reader)
        
enrollments[0]
    
'''
```
