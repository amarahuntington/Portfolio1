```python
subjects = ['spid10_2014_06_17_17_44', 'spid12_2014_06_20_15_11']
```


```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```


```python
in_file = (subjects[0]+ "/"+ subjects[0]+ '_data.txt')

# The print command below will help you confirm you have the string right, 
# before you try to use it to read the data file
print(in_file)
```

    spid10_2014_06_17_17_44/spid10_2014_06_17_17_44_data.txt



```python
df= pd.read_csv(in_file)
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id\tyear\tmonth\tday\thour\tminute\tmapping\tmessageViewingTime\tblock\ttrialNum\ttargetLocation\ttarget\tflankers\trt\tresponse\terror\tanticipation\tfeedbackResponse\ttargetOnError</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>spid10\t2014\t06\t17\t17\t44\t0\t4.395697256\t...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>spid10\t2014\t06\t17\t17\t44\t0\t4.395697256\t...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>spid10\t2014\t06\t17\t17\t44\t0\t4.395697256\t...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>spid10\t2014\t06\t17\t17\t44\t0\t4.395697256\t...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>spid10\t2014\t06\t17\t17\t44\t0\t4.395697256\t...</td>
    </tr>
  </tbody>
</table>
</div>




```python
df= pd.read_csv(in_file, sep='\t')
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id</th>
      <th>year</th>
      <th>month</th>
      <th>day</th>
      <th>hour</th>
      <th>minute</th>
      <th>mapping</th>
      <th>messageViewingTime</th>
      <th>block</th>
      <th>trialNum</th>
      <th>targetLocation</th>
      <th>target</th>
      <th>flankers</th>
      <th>rt</th>
      <th>response</th>
      <th>error</th>
      <th>anticipation</th>
      <th>feedbackResponse</th>
      <th>targetOnError</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>spid10</td>
      <td>2014</td>
      <td>6</td>
      <td>17</td>
      <td>17</td>
      <td>44</td>
      <td>0</td>
      <td>4.395697</td>
      <td>practice</td>
      <td>1</td>
      <td>right</td>
      <td>white</td>
      <td>congruent</td>
      <td>0.723172</td>
      <td>white</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>0.069474</td>
    </tr>
    <tr>
      <th>1</th>
      <td>spid10</td>
      <td>2014</td>
      <td>6</td>
      <td>17</td>
      <td>17</td>
      <td>44</td>
      <td>0</td>
      <td>4.395697</td>
      <td>practice</td>
      <td>1</td>
      <td>right</td>
      <td>white</td>
      <td>congruent</td>
      <td>0.723172</td>
      <td>white</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>0.069474</td>
    </tr>
    <tr>
      <th>2</th>
      <td>spid10</td>
      <td>2014</td>
      <td>6</td>
      <td>17</td>
      <td>17</td>
      <td>44</td>
      <td>0</td>
      <td>4.395697</td>
      <td>practice</td>
      <td>1</td>
      <td>right</td>
      <td>white</td>
      <td>congruent</td>
      <td>0.723172</td>
      <td>white</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>0.069474</td>
    </tr>
    <tr>
      <th>3</th>
      <td>spid10</td>
      <td>2014</td>
      <td>6</td>
      <td>17</td>
      <td>17</td>
      <td>44</td>
      <td>0</td>
      <td>4.395697</td>
      <td>practice</td>
      <td>2</td>
      <td>right</td>
      <td>white</td>
      <td>incongruent</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>False</td>
      <td>True</td>
      <td>0.066798</td>
    </tr>
    <tr>
      <th>4</th>
      <td>spid10</td>
      <td>2014</td>
      <td>6</td>
      <td>17</td>
      <td>17</td>
      <td>44</td>
      <td>0</td>
      <td>4.395697</td>
      <td>practice</td>
      <td>2</td>
      <td>right</td>
      <td>white</td>
      <td>incongruent</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>False</td>
      <td>True</td>
      <td>0.066798</td>
    </tr>
  </tbody>
</table>
</div>


