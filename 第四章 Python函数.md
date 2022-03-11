# 4.1Python中的函数

## 4.1.1函数的定义


```python
def area(width,height):
    return width*height
w=4
h=5
print("area =",area(w,h))
```

    area = 20
    

## 4.1.2 函数返回多个值


```python
def return_mul_val():
    my_str="Hello Python"
    num=20
    return my_str,num#返回my_str，num两个值，实际返回的是一个元组
str_,x=return_mul_val()
print(str_,x)
```

    Hello Python 20
    

## 4.1.3 函数文档的构建


```python
help(str)
```

    Help on class str in module builtins:
    
    class str(object)
     |  str(object='') -> str
     |  str(bytes_or_buffer[, encoding[, errors]]) -> str
     |  
     |  Create a new string object from the given object. If encoding or
     |  errors is specified, then the object must expose a data buffer
     |  that will be decoded using the given encoding and error handler.
     |  Otherwise, returns the result of object.__str__() (if defined)
     |  or repr(object).
     |  encoding defaults to sys.getdefaultencoding().
     |  errors defaults to 'strict'.
     |  
     |  Methods defined here:
     |  
     |  __add__(self, value, /)
     |      Return self+value.
     |  
     |  __contains__(self, key, /)
     |      Return key in self.
     |  
     |  __eq__(self, value, /)
     |      Return self==value.
     |  
     |  __format__(self, format_spec, /)
     |      Return a formatted version of the string as described by format_spec.
     |  
     |  __ge__(self, value, /)
     |      Return self>=value.
     |  
     |  __getattribute__(self, name, /)
     |      Return getattr(self, name).
     |  
     |  __getitem__(self, key, /)
     |      Return self[key].
     |  
     |  __getnewargs__(...)
     |  
     |  __gt__(self, value, /)
     |      Return self>value.
     |  
     |  __hash__(self, /)
     |      Return hash(self).
     |  
     |  __iter__(self, /)
     |      Implement iter(self).
     |  
     |  __le__(self, value, /)
     |      Return self<=value.
     |  
     |  __len__(self, /)
     |      Return len(self).
     |  
     |  __lt__(self, value, /)
     |      Return self<value.
     |  
     |  __mod__(self, value, /)
     |      Return self%value.
     |  
     |  __mul__(self, value, /)
     |      Return self*value.
     |  
     |  __ne__(self, value, /)
     |      Return self!=value.
     |  
     |  __repr__(self, /)
     |      Return repr(self).
     |  
     |  __rmod__(self, value, /)
     |      Return value%self.
     |  
     |  __rmul__(self, value, /)
     |      Return value*self.
     |  
     |  __sizeof__(self, /)
     |      Return the size of the string in memory, in bytes.
     |  
     |  __str__(self, /)
     |      Return str(self).
     |  
     |  capitalize(self, /)
     |      Return a capitalized version of the string.
     |      
     |      More specifically, make the first character have upper case and the rest lower
     |      case.
     |  
     |  casefold(self, /)
     |      Return a version of the string suitable for caseless comparisons.
     |  
     |  center(self, width, fillchar=' ', /)
     |      Return a centered string of length width.
     |      
     |      Padding is done using the specified fill character (default is a space).
     |  
     |  count(...)
     |      S.count(sub[, start[, end]]) -> int
     |      
     |      Return the number of non-overlapping occurrences of substring sub in
     |      string S[start:end].  Optional arguments start and end are
     |      interpreted as in slice notation.
     |  
     |  encode(self, /, encoding='utf-8', errors='strict')
     |      Encode the string using the codec registered for encoding.
     |      
     |      encoding
     |        The encoding in which to encode the string.
     |      errors
     |        The error handling scheme to use for encoding errors.
     |        The default is 'strict' meaning that encoding errors raise a
     |        UnicodeEncodeError.  Other possible values are 'ignore', 'replace' and
     |        'xmlcharrefreplace' as well as any other name registered with
     |        codecs.register_error that can handle UnicodeEncodeErrors.
     |  
     |  endswith(...)
     |      S.endswith(suffix[, start[, end]]) -> bool
     |      
     |      Return True if S ends with the specified suffix, False otherwise.
     |      With optional start, test S beginning at that position.
     |      With optional end, stop comparing S at that position.
     |      suffix can also be a tuple of strings to try.
     |  
     |  expandtabs(self, /, tabsize=8)
     |      Return a copy where all tab characters are expanded using spaces.
     |      
     |      If tabsize is not given, a tab size of 8 characters is assumed.
     |  
     |  find(...)
     |      S.find(sub[, start[, end]]) -> int
     |      
     |      Return the lowest index in S where substring sub is found,
     |      such that sub is contained within S[start:end].  Optional
     |      arguments start and end are interpreted as in slice notation.
     |      
     |      Return -1 on failure.
     |  
     |  format(...)
     |      S.format(*args, **kwargs) -> str
     |      
     |      Return a formatted version of S, using substitutions from args and kwargs.
     |      The substitutions are identified by braces ('{' and '}').
     |  
     |  format_map(...)
     |      S.format_map(mapping) -> str
     |      
     |      Return a formatted version of S, using substitutions from mapping.
     |      The substitutions are identified by braces ('{' and '}').
     |  
     |  index(...)
     |      S.index(sub[, start[, end]]) -> int
     |      
     |      Return the lowest index in S where substring sub is found,
     |      such that sub is contained within S[start:end].  Optional
     |      arguments start and end are interpreted as in slice notation.
     |      
     |      Raises ValueError when the substring is not found.
     |  
     |  isalnum(self, /)
     |      Return True if the string is an alpha-numeric string, False otherwise.
     |      
     |      A string is alpha-numeric if all characters in the string are alpha-numeric and
     |      there is at least one character in the string.
     |  
     |  isalpha(self, /)
     |      Return True if the string is an alphabetic string, False otherwise.
     |      
     |      A string is alphabetic if all characters in the string are alphabetic and there
     |      is at least one character in the string.
     |  
     |  isascii(self, /)
     |      Return True if all characters in the string are ASCII, False otherwise.
     |      
     |      ASCII characters have code points in the range U+0000-U+007F.
     |      Empty string is ASCII too.
     |  
     |  isdecimal(self, /)
     |      Return True if the string is a decimal string, False otherwise.
     |      
     |      A string is a decimal string if all characters in the string are decimal and
     |      there is at least one character in the string.
     |  
     |  isdigit(self, /)
     |      Return True if the string is a digit string, False otherwise.
     |      
     |      A string is a digit string if all characters in the string are digits and there
     |      is at least one character in the string.
     |  
     |  isidentifier(self, /)
     |      Return True if the string is a valid Python identifier, False otherwise.
     |      
     |      Call keyword.iskeyword(s) to test whether string s is a reserved identifier,
     |      such as "def" or "class".
     |  
     |  islower(self, /)
     |      Return True if the string is a lowercase string, False otherwise.
     |      
     |      A string is lowercase if all cased characters in the string are lowercase and
     |      there is at least one cased character in the string.
     |  
     |  isnumeric(self, /)
     |      Return True if the string is a numeric string, False otherwise.
     |      
     |      A string is numeric if all characters in the string are numeric and there is at
     |      least one character in the string.
     |  
     |  isprintable(self, /)
     |      Return True if the string is printable, False otherwise.
     |      
     |      A string is printable if all of its characters are considered printable in
     |      repr() or if it is empty.
     |  
     |  isspace(self, /)
     |      Return True if the string is a whitespace string, False otherwise.
     |      
     |      A string is whitespace if all characters in the string are whitespace and there
     |      is at least one character in the string.
     |  
     |  istitle(self, /)
     |      Return True if the string is a title-cased string, False otherwise.
     |      
     |      In a title-cased string, upper- and title-case characters may only
     |      follow uncased characters and lowercase characters only cased ones.
     |  
     |  isupper(self, /)
     |      Return True if the string is an uppercase string, False otherwise.
     |      
     |      A string is uppercase if all cased characters in the string are uppercase and
     |      there is at least one cased character in the string.
     |  
     |  join(self, iterable, /)
     |      Concatenate any number of strings.
     |      
     |      The string whose method is called is inserted in between each given string.
     |      The result is returned as a new string.
     |      
     |      Example: '.'.join(['ab', 'pq', 'rs']) -> 'ab.pq.rs'
     |  
     |  ljust(self, width, fillchar=' ', /)
     |      Return a left-justified string of length width.
     |      
     |      Padding is done using the specified fill character (default is a space).
     |  
     |  lower(self, /)
     |      Return a copy of the string converted to lowercase.
     |  
     |  lstrip(self, chars=None, /)
     |      Return a copy of the string with leading whitespace removed.
     |      
     |      If chars is given and not None, remove characters in chars instead.
     |  
     |  partition(self, sep, /)
     |      Partition the string into three parts using the given separator.
     |      
     |      This will search for the separator in the string.  If the separator is found,
     |      returns a 3-tuple containing the part before the separator, the separator
     |      itself, and the part after it.
     |      
     |      If the separator is not found, returns a 3-tuple containing the original string
     |      and two empty strings.
     |  
     |  removeprefix(self, prefix, /)
     |      Return a str with the given prefix string removed if present.
     |      
     |      If the string starts with the prefix string, return string[len(prefix):].
     |      Otherwise, return a copy of the original string.
     |  
     |  removesuffix(self, suffix, /)
     |      Return a str with the given suffix string removed if present.
     |      
     |      If the string ends with the suffix string and that suffix is not empty,
     |      return string[:-len(suffix)]. Otherwise, return a copy of the original
     |      string.
     |  
     |  replace(self, old, new, count=-1, /)
     |      Return a copy with all occurrences of substring old replaced by new.
     |      
     |        count
     |          Maximum number of occurrences to replace.
     |          -1 (the default value) means replace all occurrences.
     |      
     |      If the optional argument count is given, only the first count occurrences are
     |      replaced.
     |  
     |  rfind(...)
     |      S.rfind(sub[, start[, end]]) -> int
     |      
     |      Return the highest index in S where substring sub is found,
     |      such that sub is contained within S[start:end].  Optional
     |      arguments start and end are interpreted as in slice notation.
     |      
     |      Return -1 on failure.
     |  
     |  rindex(...)
     |      S.rindex(sub[, start[, end]]) -> int
     |      
     |      Return the highest index in S where substring sub is found,
     |      such that sub is contained within S[start:end].  Optional
     |      arguments start and end are interpreted as in slice notation.
     |      
     |      Raises ValueError when the substring is not found.
     |  
     |  rjust(self, width, fillchar=' ', /)
     |      Return a right-justified string of length width.
     |      
     |      Padding is done using the specified fill character (default is a space).
     |  
     |  rpartition(self, sep, /)
     |      Partition the string into three parts using the given separator.
     |      
     |      This will search for the separator in the string, starting at the end. If
     |      the separator is found, returns a 3-tuple containing the part before the
     |      separator, the separator itself, and the part after it.
     |      
     |      If the separator is not found, returns a 3-tuple containing two empty strings
     |      and the original string.
     |  
     |  rsplit(self, /, sep=None, maxsplit=-1)
     |      Return a list of the words in the string, using sep as the delimiter string.
     |      
     |        sep
     |          The delimiter according which to split the string.
     |          None (the default value) means split according to any whitespace,
     |          and discard empty strings from the result.
     |        maxsplit
     |          Maximum number of splits to do.
     |          -1 (the default value) means no limit.
     |      
     |      Splits are done starting at the end of the string and working to the front.
     |  
     |  rstrip(self, chars=None, /)
     |      Return a copy of the string with trailing whitespace removed.
     |      
     |      If chars is given and not None, remove characters in chars instead.
     |  
     |  split(self, /, sep=None, maxsplit=-1)
     |      Return a list of the words in the string, using sep as the delimiter string.
     |      
     |      sep
     |        The delimiter according which to split the string.
     |        None (the default value) means split according to any whitespace,
     |        and discard empty strings from the result.
     |      maxsplit
     |        Maximum number of splits to do.
     |        -1 (the default value) means no limit.
     |  
     |  splitlines(self, /, keepends=False)
     |      Return a list of the lines in the string, breaking at line boundaries.
     |      
     |      Line breaks are not included in the resulting list unless keepends is given and
     |      true.
     |  
     |  startswith(...)
     |      S.startswith(prefix[, start[, end]]) -> bool
     |      
     |      Return True if S starts with the specified prefix, False otherwise.
     |      With optional start, test S beginning at that position.
     |      With optional end, stop comparing S at that position.
     |      prefix can also be a tuple of strings to try.
     |  
     |  strip(self, chars=None, /)
     |      Return a copy of the string with leading and trailing whitespace removed.
     |      
     |      If chars is given and not None, remove characters in chars instead.
     |  
     |  swapcase(self, /)
     |      Convert uppercase characters to lowercase and lowercase characters to uppercase.
     |  
     |  title(self, /)
     |      Return a version of the string where each word is titlecased.
     |      
     |      More specifically, words start with uppercased characters and all remaining
     |      cased characters have lower case.
     |  
     |  translate(self, table, /)
     |      Replace each character in the string using the given translation table.
     |      
     |        table
     |          Translation table, which must be a mapping of Unicode ordinals to
     |          Unicode ordinals, strings, or None.
     |      
     |      The table must implement lookup/indexing via __getitem__, for instance a
     |      dictionary or list.  If this operation raises LookupError, the character is
     |      left untouched.  Characters mapped to None are deleted.
     |  
     |  upper(self, /)
     |      Return a copy of the string converted to uppercase.
     |  
     |  zfill(self, width, /)
     |      Pad a numeric string with zeros on the left, to fill a field of the given width.
     |      
     |      The string is never truncated.
     |  
     |  ----------------------------------------------------------------------
     |  Static methods defined here:
     |  
     |  __new__(*args, **kwargs) from builtins.type
     |      Create and return a new object.  See help(type) for accurate signature.
     |  
     |  maketrans(...)
     |      Return a translation table usable for str.translate().
     |      
     |      If there is only one argument, it must be a dictionary mapping Unicode
     |      ordinals (integers) or characters to Unicode ordinals, strings or None.
     |      Character keys will be then converted to ordinals.
     |      If there are two arguments, they must be strings of equal length, and
     |      in the resulting dictionary, each character in x will be mapped to the
     |      character at the same position in y. If there is a third argument, it
     |      must be a string, whose characters will be mapped to None in the result.
    
    


```python
help(print)
```

    Help on built-in function print in module builtins:
    
    print(...)
        print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
        
        Prints the values to a stream, or to sys.stdout by default.
        Optional keyword arguments:
        file:  a file-like object (stream); defaults to the current sys.stdout.
        sep:   string inserted between values, default a space.
        end:   string appended after the last value, default a newline.
        flush: whether to forcibly flush the stream.
    
    


```python
format?
```


```python
# 计算面积函数
def area(width, height):
    '''
    功能：计算矩形的面积

    参数：
    ----------
    width : 数值型
        矩形的宽度
    height :数值型
        矩形的高度

    返回值
    -------
    rec_area: 数值型
        矩形的面积：width * height
    '''
    rec_area = width * height
    return rec_area

w = 4
h = 5
print("width = ", w, " height =", h, " area = ", area(w, h))

```

    width =  4  height = 5  area =  20
    


```python
help(area)
```

    Help on function area in module __main__:
    
    area(width, height)
        功能：计算矩形的面积
        
        参数：
        ----------
        width : 数值型
            矩形的宽度
        height :数值型
            矩形的高度
        
        返回值
        -------
        rec_area: 数值型
            矩形的面积：width * height
    
    


```python
area.__doc__
```




    '\n    功能：计算矩形的面积\n\n    参数：\n    ----------\n    width : 数值型\n        矩形的宽度\n    height :数值型\n        矩形的高度\n\n    返回值\n    -------\n    rec_area: 数值型\n        矩形的面积：width * height\n    '




```python
print(area.__doc__)
```

    
        功能：计算矩形的面积
    
        参数：
        ----------
        width : 数值型
            矩形的宽度
        height :数值型
            矩形的高度
    
        返回值
        -------
        rec_area: 数值型
            矩形的面积：width * height
        
    


```python
area?
```

# 4.2 函数参数的“花式”传递

## 4.2.1 关键字传递


```python
def saySomething(name,word):
    print(name+':'+word)
saySomething("Zhangsan", "Hello World")
```

    Zhangsan:Hello World
    


```python
saySomething(word="Hello World",name="Zhangsan")
```

    Zhangsan:Hello World
    

## 4.2.2可变参数


```python
def varParaFun(name,*args):
    print("位置参数是：",name)
    print("收集参数是：", args)
    print("第一个收集参数是：",args[0])#元组
varParaFun("Zhangsan",111,222,333)
```

    位置参数是： Zhangsan
    收集参数是： (111, 222, 333)
    第一个收集参数是： 111
    


```python
def MySum(*args):
    sum=0
    for i in range(0,len(args)):
        sum+=args[i]
    return sum
print(MySum(1,2,3,4,5))
print(MySum(20.1,30.2))
```

    15
    50.3
    


```python
#(**)两个*号将多个参数打包为字典模样
def varFun(**x):
    if len(x)==0:
        print("None")
    else:
        print(x)
varFun()#0个参数
```

    None
    


```python
varFun(a=1,b=2)#有两个参数，以键/值对（即字典）的形式给函数传参
```

    {'a': 1, 'b': 2}
    


```python
varFun(1,3)#错误，必须以键/值对的形式给函数传参
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_14176/1515223353.py in <module>
    ----> 1 varFun(1,3)
    

    TypeError: varFun() takes 0 positional arguments but 2 were given



```python
#【用字典给可变关键字参数赋值】
def some_kwargs(name,age,sex):
    print("姓名：",name)
    print("年龄：",age)
    print("性别：",sex)
kwargs_dic={'name':'txk','age':18,'sex':'male'}
some_kwargs(**kwargs_dic)
```

    姓名： txk
    年龄： 18
    性别： male
    

## 4.2.3 默认参数


```python
def defaultFun(x,y=3):
    print(x,y)
defaultFun(4)
```

    4 3
    


```python
defaultFun(4,4)
```

    4 4
    


```python
defaultFun.__defaults__
```




    (3,)




```python
def add_end(L=[]):   #默认参数L为空列表
    L.append("END")
    return L
add_end(["Hello",'World','Python'])
```




    ['Hello', 'World', 'Python', 'END']




```python
add_end()#首次调用，没有提供实参，启用默认参数，输出正确
```




    ['END']




```python
add_end()#二次调用启用默认参数，输出错误
```




    ['END', 'END']




```python
add_end()#二次调用启用默认参数，输出错误，记忆了上次调用后添加的'END'
```




    ['END', 'END', 'END']




```python
def add_end(L=None):
    if L  is None:
        L=[]
    L.append('END')
    return L
add_end()
```




    ['END']




```python
add_end()
```




    ['END']



## 4.2.4参数序列的打包与解包


```python
val =1,2,3,4
type(val)
```




    tuple




```python
val
```




    (1, 2, 3, 4)




```python
a,b,c,d=val
print(a,b,c,d)
```

    1 2 3 4
    


```python
type(a)
```




    int




```python
val=1,2,3#没有足够的值来解包
a,b,c,d=val
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_14176/1260845033.py in <module>
          1 val=1,2,3
    ----> 2 a,b,c,d=val
    

    ValueError: not enough values to unpack (expected 4, got 3)



```python
#支持解包操作的不仅限于元组，还包括所有可迭代对象例如列表，字典等
def fun(a,b,c,d):
    print(a,b,c,d)
my_list=[1,2,3,4]
fun(*my_list)#*号必不可少，解包的标志
```

    1 2 3 4
    


```python
my_dict={'a':1,'b':2,'c':3,'d':4}
fun(*my_dict)
```

    a b c d
    


```python
fun(**my_dict)
```

    1 2 3 4
    

## 4.2.5传值还是传引用

 ## 4.3.3 递归函数的调用

# 4.4 函数式编程的高阶函数

## 4.4.1 lambda表达式


```python
lambda x,y:x+y
```




    <function __main__.<lambda>(x, y)>




```python
new_add=lambda x,y:x+y
new_add(9,8)
```




    17



## 4.4.2filter()函数【过滤器】


```python
def fun(variable):
    letters=['a','e','i','o','u']
    if( variable in letters):
        return True
    else:
        return False
sequence=['g','f','e','j','k','s','p','k','o']
filtered=filter(fun,sequence)
filtered# 不能直接输出筛选数据
```




    <filter at 0x1e759c73250>




```python
list(filtered)#转化为列表再输出
```




    ['e', 'o']




```python
a_list=[2,18,9,22,17,24,8,12,27]
data=filter(lambda x:x%3==0,a_list)
list(data)
```




    [18, 9, 24, 12, 27]



## 4.4.3 map()函数


```python
def myfun(x,y):
    return x+y
m=map(myfun,[1,2,3],[4,5,6])
```


```python
m
```




    <map at 0x1e759c73790>




```python
list(m)
```




    [5, 7, 9]




```python
a_list=[2,18,9,22,17,24,8,12,27]
my_map=map(lambda x:x*2+1,a_list)
new_list=list(my_map)
```


```python
new_list
```




    [5, 37, 19, 45, 35, 49, 17, 25, 55]




```python
str_cat=map(myfun,('apple ','banana ','I love'),('orange','lemon',' carmel'))
list(str_cat)
```




    ['apple orange', 'banana lemon', 'I love carmel']



## 4.4.4 reduce()函数


```python
from functools import reduce
reduce(lambda x,y:x+y,range(1,101))
```




    5050




```python
reduce(lambda x,y:x+y,[1,2,3,4,5])
```




    15




```python
reduce(lambda a,b:a if a>b else b,[8,44,561,1,888])
```




    888



## 4.4.5 sorted()函数 


```python
sorted([70,60,-20,10,-30])
```




    [-30, -20, 10, 60, 70]




```python
sorted([70,60,-20,10,-30],reverse=True)
```




    [70, 60, 10, -20, -30]




```python
sorted([70,60,-20,10,-30],key=abs,reverse=True)
```




    [70, 60, -30, -20, 10]




```python
def return_dict():
    d=dict()
    d['my_str']='Hello python'
    d['num']=20
    return d
dict_=return_dict()
    
```


```python
print(dict_)
```

    {'my_str': 'Hello python', 'num': 20}
    


```python
print(dict_['num'])
```

    20
    


```python
print(dict_['my_str'])
```

    Hello python
    


```python
matrix=[[1,2,3],[4,5,6]]
list(zip(*matrix))#*号有解包功能
```




    [(1, 4), (2, 5), (3, 6)]




```python
list(zip(matrix))#只有一个迭代器，matrix中的每个元素zip后的逗号必不可少
```




    [([1, 2, 3],), ([4, 5, 6],)]




```python
sorted(['bob','about','Zoo','Credit'],key=str.lower)
```




    ['about', 'bob', 'Credit', 'Zoo']




```python
sorted(['bob','about','Zoo','Credit'],key=len,reverse=True)
```




    ['Credit', 'about', 'bob', 'Zoo']




```python
from operator import itemgetter
students=[('Adam',89),('Bob',75),('Alice',96),('Lisa',78)]
name=sorted(students,key=itemgetter(0))
```


```python
print(name)
```

    [('Adam', 89), ('Alice', 96), ('Bob', 75), ('Lisa', 78)]
    


```python
score=sorted(students,key=itemgetter(1))
```


```python
print(score)
```

    [('Bob', 75), ('Lisa', 78), ('Adam', 89), ('Alice', 96)]
    
