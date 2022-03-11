```python
import pandas as pd
import numpy as np
a=pd.Series([2,0,78,-9])
a
```




    0     2
    1     0
    2    78
    3    -9
    dtype: int64




```python
s=pd.Series(np.random.randn(5),index=['a','b','c','d','e'])
s
```




    a   -1.068426
    b   -0.270897
    c    1.307677
    d   -0.094185
    e    0.291542
    dtype: float64




```python
a.index
```




    RangeIndex(start=0, stop=4, step=1)




```python
a.values
```




    array([ 2,  0, 78, -9], dtype=int64)




```python
import numpy as np
import pandas as pd

a = pd.Series(np.random.randn(5))
a.index = ['a', 'b', 'c', 'd', 'e']
print(a, a.values, a.index, sep='\n')
a.index = ['one', 'two', 'three', 'four', 'five']
print('\n修改索引后：')
print(a, a.index, sep='\n')
Dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
temp = pd.Series(Dict,dtype=int)
print('\n字典打包为Series：')
print(temp)
```

    a    0.304115
    b   -0.691224
    c   -1.018522
    d   -2.083296
    e   -0.203866
    dtype: float64
    [ 0.30411484 -0.6912238  -1.01852233 -2.08329606 -0.20386642]
    Index(['a', 'b', 'c', 'd', 'e'], dtype='object')
    
    修改索引后：
    one      0.304115
    two     -0.691224
    three   -1.018522
    four    -2.083296
    five    -0.203866
    dtype: float64
    Index(['one', 'two', 'three', 'four', 'five'], dtype='object')
    
    字典打包为Series：
    a    1
    b    2
    c    3
    d    4
    e    5
    dtype: int32
    


```python
temp.describe()
```




    count    5.000000
    mean     3.000000
    std      1.581139
    min      1.000000
    25%      2.000000
    50%      3.000000
    75%      4.000000
    max      5.000000
    dtype: float64




```python
cities={"beijin":55000,"shanghai":60000,"shenzhen":50000,"hangzhou":20000,"guangzhou":None}
apts=pd.Series(cities,name="place")
apts
```




    beijin       55000.0
    shanghai     60000.0
    shenzhen     50000.0
    hangzhou     20000.0
    guangzhou        NaN
    Name: place, dtype: float64




```python
apts[0]
```




    55000.0




```python
apts[1]
```




    60000.0




```python
apts["beijin"]=60000
apts
```




    beijin       60000.0
    shanghai     60000.0
    shenzhen     50000.0
    hangzhou     20000.0
    guangzhou        NaN
    Name: place, dtype: float64




```python
apts[["shanghai","shenzhen"]]
```




    shanghai    60000.0
    shenzhen    50000.0
    Name: place, dtype: float64




```python
apts[[1,4,0]]
```




    shanghai     60000.0
    guangzhou        NaN
    beijin       60000.0
    Name: place, dtype: float64




```python
s1=pd.Series([1,2,3])
s2=pd.Series([4,5,6])
s1
```




    0    1
    1    2
    2    3
    dtype: int64




```python
s2
```




    0    4
    1    5
    2    6
    dtype: int64




```python
dict1={'a':1,'b':2,'c':3}
s3=pd.Series(dict1)
s3
```




    a    1
    b    2
    c    3
    dtype: int64




```python
s1.append(s2,ignore_index=True)
```




    0    1
    1    2
    2    3
    3    4
    4    5
    5    6
    dtype: int64



## 7. 3 .3 Series中的向量化操作与布尔索引


```python
apts*3
```




    beijin       180000.0
    shanghai     180000.0
    shenzhen     150000.0
    hangzhou      60000.0
    guangzhou         NaN
    Name: place, dtype: float64




```python
apts+apts
```




    beijin       120000.0
    shanghai     120000.0
    shenzhen     100000.0
    hangzhou      40000.0
    guangzhou         NaN
    Name: place, dtype: float64




```python
apts>apts.median()
```




    beijin        True
    shanghai      True
    shenzhen     False
    hangzhou     False
    guangzhou    False
    Name: place, dtype: bool




```python
apts[apts>apts.median()]
```




    beijin      60000.0
    shanghai    60000.0
    Name: place, dtype: float64




```python
import numpy as np
s=pd.Series(np.random.randn(5),index=['a','b','c','d','e'])
s
```




    a    0.233737
    b    1.291211
    c    0.622220
    d    0.420777
    e   -0.501841
    dtype: float64




```python
a=np.square(s)
a
```




    a    0.054633
    b    1.667225
    c    0.387157
    d    0.177053
    e    0.251844
    dtype: float64




```python
b=np.abs(s)
b
```




    a    0.233737
    b    1.291211
    c    0.622220
    d    0.420777
    e    0.501841
    dtype: float64




```python
b[1:3]
```




    b    1.291211
    c    0.622220
    dtype: float64




```python
b['b':'d']
```




    b    1.291211
    c    0.622220
    d    0.420777
    dtype: float64




```python
apts.isnull()
```




    beijin       False
    shanghai     False
    shenzhen     False
    hangzhou     False
    guangzhou     True
    Name: place, dtype: bool




```python
apts.notnull()
```




    beijin        True
    shanghai      True
    shenzhen      True
    hangzhou      True
    guangzhou    False
    Name: place, dtype: bool




```python
apts[apts.isnull() == True]
```




    guangzhou   NaN
    Name: place, dtype: float64




```python
apts.name='price'
apts.index.name='地点'
apts
```




    地点
    beijin       60000.0
    shanghai     60000.0
    shenzhen     50000.0
    hangzhou     20000.0
    guangzhou        NaN
    Name: price, dtype: float64



# 7.4 DataFrame 类型数据


```python
df=pd.DataFrame({'sentences':['txk','fight']})
df
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
      <th>sentences</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>txk</td>
    </tr>
    <tr>
      <th>1</th>
      <td>fight</td>
    </tr>
  </tbody>
</table>
</div>




```python
data=pd.DataFrame({'one':[1,2,3],'two':[4,5,6],'three':[7,8,9]})
data
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
      <th>one</th>
      <th>two</th>
      <th>three</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>4</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>5</td>
      <td>8</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>6</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
data1=np.random.randint(1,10,9).reshape(3,3)
data1
```




    array([[1, 4, 8],
           [8, 4, 6],
           [4, 1, 8]])




```python
df1=pd.DataFrame(data1)
df1
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
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>4</td>
      <td>8</td>
    </tr>
    <tr>
      <th>1</th>
      <td>8</td>
      <td>4</td>
      <td>6</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4</td>
      <td>1</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2=pd.DataFrame(data1,columns=['one','two','three'],index=['a','b','c'])
df2
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
      <th>one</th>
      <th>two</th>
      <th>three</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>1</td>
      <td>4</td>
      <td>8</td>
    </tr>
    <tr>
      <th>b</th>
      <td>8</td>
      <td>4</td>
      <td>6</td>
    </tr>
    <tr>
      <th>c</th>
      <td>4</td>
      <td>1</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.T
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
      <th>a</th>
      <th>b</th>
      <th>c</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>one</th>
      <td>1</td>
      <td>8</td>
      <td>4</td>
    </tr>
    <tr>
      <th>two</th>
      <td>4</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>three</th>
      <td>8</td>
      <td>6</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.columns
```




    Index(['one', 'two', 'three'], dtype='object')




```python
df2['two']
```




    a    4
    b    4
    c    1
    Name: two, dtype: int32




```python
df2.three
```




    a    8
    b    6
    c    8
    Name: three, dtype: int32




```python
df2[['one','two']]
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
      <th>one</th>
      <th>two</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>b</th>
      <td>8</td>
      <td>4</td>
    </tr>
    <tr>
      <th>c</th>
      <td>4</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
