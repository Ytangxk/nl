```python
import numpy as np
data1=[6,8.5,9,0]
arr1=np.array(data1)
arr1
```




    array([6. , 8.5, 9. , 0. ])




```python
arr1.dtype
```




    dtype('float64')




```python
import numpy as np

data1 = [6, 8.5, 9, 0]
arr1 = np.array(data1)
print(arr1)
arr1 = arr1.astype(np.int32)
print(arr1)
data2 = [[1, 2, 3, 4], [5, 6, 7, 8]]
arr2 = np.array(data2)
print(arr2)
```

    [6.  8.5 9.  0. ]
    [6 8 9 0]
    [[1 2 3 4]
     [5 6 7 8]]
    


```python
arr3=np.arange(10)
arr3
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
print(arr3)
```

    [0 1 2 3 4 5 6 7 8 9]
    


```python
arr3=arr3+1
print(arr3)
```

    [ 1  2  3  4  5  6  7  8  9 10]
    


```python
print(type(arr3))
```

    <class 'numpy.ndarray'>
    


```python
arr4=range(10)
print(arr4)
```

    range(0, 10)
    


```python
print(type(arr4))
```

    <class 'range'>
    


```python
arr=np.arange(6)
arr=arr.reshape((2,3))
arr
```




    array([[0, 1, 2],
           [3, 4, 5]])




```python
zeros=np.zeros(shape=[3,4],dtype=int)
zeros
```




    array([[0, 0, 0, 0],
           [0, 0, 0, 0],
           [0, 0, 0, 0]])




```python
ones=np.ones(shape=[3,4],dtype=int)
ones
```




    array([[1, 1, 1, 1],
           [1, 1, 1, 1],
           [1, 1, 1, 1]])




```python
array=np.array([[1,2,3.0],[4,5,6]])
array
```




    array([[1., 2., 3.],
           [4., 5., 6.]])




```python
array.dtype
```




    dtype('float64')




```python
b_zeros=np.zeros_like(array,dtype=int)
b_zeros
```




    array([[0, 0, 0],
           [0, 0, 0]])




```python
b_zeros.ndim
```




    2




```python
b_zeros.shape
```




    (2, 3)




```python
b_zeros.shape
```




    (2, 3)




```python
b=np.arange(15)
b
```




    array([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14])




```python
b=b.reshape(3,5)
b
```




    array([[ 0,  1,  2,  3,  4],
           [ 5,  6,  7,  8,  9],
           [10, 11, 12, 13, 14]])




```python
b.ndim
```




    2




```python
b.shape
```




    (3, 5)




```python
b.size
```




    15




```python
a=np.arange(30).reshape(2,3,5)
a
```




    array([[[ 0,  1,  2,  3,  4],
            [ 5,  6,  7,  8,  9],
            [10, 11, 12, 13, 14]],
    
           [[15, 16, 17, 18, 19],
            [20, 21, 22, 23, 24],
            [25, 26, 27, 28, 29]]])




```python
a.shape
```




    (2, 3, 5)




```python
list_1=[1,2,3,4,5,6,7,8,9,10]
list_2=[11,12,13,14,15,16,17,18,19,20]
list_3=[item1 +item2 for item1,item2 in zip(list_1,list_2)]
list_3
```




    [12, 14, 16, 18, 20, 22, 24, 26, 28, 30]




```python
list1_arr=np.array(list_1)
list2_arr=np.array(list_2)
list_sum=list1_arr+list2_arr
print(list_sum)
```

    [12 14 16 18 20 22 24 26 28 30]
    


```python
list_sum
```




    array([12, 14, 16, 18, 20, 22, 24, 26, 28, 30])




```python
a=np.arange(10)
a
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
b=np.linspace(1,10,10)
b
```




    array([ 1.,  2.,  3.,  4.,  5.,  6.,  7.,  8.,  9., 10.])




```python
a+b
```




    array([ 1.,  3.,  5.,  7.,  9., 11., 13., 15., 17., 19.])




```python
a-b
```




    array([-1., -1., -1., -1., -1., -1., -1., -1., -1., -1.])




```python
a*b
```




    array([ 0.,  2.,  6., 12., 20., 30., 42., 56., 72., 90.])




```python
a/b
```




    array([0.        , 0.5       , 0.66666667, 0.75      , 0.8       ,
           0.83333333, 0.85714286, 0.875     , 0.88888889, 0.9       ])




```python
a%b
```




    array([0., 1., 2., 3., 4., 5., 6., 7., 8., 9.])




```python
a**b
```




    array([0.00000000e+00, 1.00000000e+00, 8.00000000e+00, 8.10000000e+01,
           1.02400000e+03, 1.56250000e+04, 2.79936000e+05, 5.76480100e+06,
           1.34217728e+08, 3.48678440e+09])




```python
a**2
```




    array([ 0,  1,  4,  9, 16, 25, 36, 49, 64, 81], dtype=int32)




```python
a=np.array([[1,2],[3,4]])
a
```




    array([[1, 2],
           [3, 4]])




```python
b=np.ones_like(a)
```


```python
b
```




    array([[1, 1],
           [1, 1]])




```python
a+b
```




    array([[2, 3],
           [4, 5]])




```python
c=np.ones(shape=[2,2])
c
```




    array([[1., 1.],
           [1., 1.]])




```python
a+c
```




    array([[2., 3.],
           [4., 5.]])




```python
a*c
```




    array([[1., 2.],
           [3., 4.]])




```python
a*b
```




    array([[1, 2],
           [3, 4]])




```python
np.multiply(a,c)
```




    array([[1., 2.],
           [3., 4.]])




```python
a=np.arange(9).reshape(3,3)
b=np.ones(shape=[3,2])
a
```




    array([[0, 1, 2],
           [3, 4, 5],
           [6, 7, 8]])




```python
b
```




    array([[1., 1.],
           [1., 1.],
           [1., 1.]])




```python
np.dot(a,b)
```




    array([[ 3.,  3.],
           [12., 12.],
           [21., 21.]])




```python
a=np.mat(a)#转化为矩阵
a
```




    matrix([[0, 1, 2],
            [3, 4, 5],
            [6, 7, 8]])




```python
b=np.mat(b)
```


```python
b
```




    matrix([[1., 1.],
            [1., 1.],
            [1., 1.]])




```python
a*b
```




    matrix([[ 3.,  3.],
            [12., 12.],
            [21., 21.]])




```python
a=np.arange(1,10).reshape(3,3)
a
```




    array([[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]])




```python
a=np.mat(a)
a
```




    matrix([[1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]])




```python
a.I
```




    matrix([[ 3.15251974e+15, -6.30503948e+15,  3.15251974e+15],
            [-6.30503948e+15,  1.26100790e+16, -6.30503948e+15],
            [ 3.15251974e+15, -6.30503948e+15,  3.15251974e+15]])




```python
a.T
```




    matrix([[1, 4, 7],
            [2, 5, 8],
            [3, 6, 9]])




```python

```
