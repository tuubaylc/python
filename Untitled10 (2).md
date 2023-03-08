# numpy kütüphanesi


```python
import numpy as np
vize = [10,20,30,40]
final = [2,60,32,50]

vize_np = np.array(vize)
final_np = np.array(final)

ortalama = (vize_np+final_np)/2
print(ortalama)
```

    [ 6. 40. 31. 45.]
    

# cok boyutlu numpy dizisi oluşturma


```python
import numpy as np
my_array = np.array([[1,2,3],[4,5,6]])
print(my_array)
```

    [[1 2 3]
     [4 5 6]]
    


```python
import numpy as np

arr = np.array([1,2,3,4,5,100])
max_value = np.amax(arr)
print(max_value)
```

    100
    


```python
import numpy as np

arr = np.array([[1,2,3],[4,5,6],[7,8,9]])
max_value = np.amax(arr,axis=1)
print(max_value)
```

    [3 6 9]
    

# her satırın maksimum değerini bulmak için kullanılır. Benzer şekilde sütunların maksimum değerleri için, axis=0 kullanılabilir.

# keepdims yaparsak parantez içinde verir. keepdims=true


```python
import numpy as np

arr = np.array([1,2,3,4,5])
max_valume = np.amax(arr,initial=0)
print(max_valume)
```

    5
    


```python
import pandas as pd

my_list = [1,2,3,4,5]
my_series = pd.series(my_list)
print(my_series)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_9968\1943169499.py in <module>
          2 
          3 my_list = [1,2,3,4,5]
    ----> 4 my_series = pd.series(my_list)
          5 print(my_series)
    

    ~\anaconda3\lib\site-packages\pandas\__init__.py in __getattr__(name)
        259         return _SparseArray
        260 
    --> 261     raise AttributeError(f"module 'pandas' has no attribute '{name}'")
        262 
        263 
    

    AttributeError: module 'pandas' has no attribute 'series'



```python
import pandas as pd
my_dict = {'name':['Alice','Bob','charlie'],'age':[25,30,35]}
my_dataframe = pd.DataFrame(my_dict)
print(my_dataframe)
```

          name  age
    0    Alice   25
    1      Bob   30
    2  charlie   35
    

# pandasla dosya işlemleri


```python
import pandas as pd
my_dataframe = pd.read_csv('D:/Yeni klasör/data.csv')
print(my_dataframe)

my_dataframe = pd.read_excel('D:/Yeni klasör/data.xlsx')
print(my_dataframe)

my_dataframe.to_csv('D:/Yeni klasör/data.csv',index=false)
```


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_9968\3391820763.py in <module>
          1 import pandas as pd
    ----> 2 my_dataframe = pd.read_csv('D:/Yeni klasör/csv')
          3 print(my_dataframe)
          4 
          5 my_dataframe = pd.read_excel('D:/Yeni klasör/xlsx')
    

    ~\anaconda3\lib\site-packages\pandas\util\_decorators.py in wrapper(*args, **kwargs)
        309                     stacklevel=stacklevel,
        310                 )
    --> 311             return func(*args, **kwargs)
        312 
        313         return wrapper
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in read_csv(filepath_or_buffer, sep, delimiter, header, names, index_col, usecols, squeeze, prefix, mangle_dupe_cols, dtype, engine, converters, true_values, false_values, skipinitialspace, skiprows, skipfooter, nrows, na_values, keep_default_na, na_filter, verbose, skip_blank_lines, parse_dates, infer_datetime_format, keep_date_col, date_parser, dayfirst, cache_dates, iterator, chunksize, compression, thousands, decimal, lineterminator, quotechar, quoting, doublequote, escapechar, comment, encoding, encoding_errors, dialect, error_bad_lines, warn_bad_lines, on_bad_lines, delim_whitespace, low_memory, memory_map, float_precision, storage_options)
        676     kwds.update(kwds_defaults)
        677 
    --> 678     return _read(filepath_or_buffer, kwds)
        679 
        680 
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in _read(filepath_or_buffer, kwds)
        573 
        574     # Create the parser.
    --> 575     parser = TextFileReader(filepath_or_buffer, **kwds)
        576 
        577     if chunksize or iterator:
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in __init__(self, f, engine, **kwds)
        930 
        931         self.handles: IOHandles | None = None
    --> 932         self._engine = self._make_engine(f, self.engine)
        933 
        934     def close(self):
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in _make_engine(self, f, engine)
       1214             # "Union[str, PathLike[str], ReadCsvBuffer[bytes], ReadCsvBuffer[str]]"
       1215             # , "str", "bool", "Any", "Any", "Any", "Any", "Any"
    -> 1216             self.handles = get_handle(  # type: ignore[call-overload]
       1217                 f,
       1218                 mode,
    

    ~\anaconda3\lib\site-packages\pandas\io\common.py in get_handle(path_or_buf, mode, encoding, compression, memory_map, is_text, errors, storage_options)
        784         if ioargs.encoding and "b" not in ioargs.mode:
        785             # Encoding
    --> 786             handle = open(
        787                 handle,
        788                 ioargs.mode,
    

    FileNotFoundError: [Errno 2] No such file or directory: 'D:/Yeni klasör/csv'


# iris veri seti yükleme


```python
import seaborn as sns

iris = sns.load_dataset("iris")

print(iris.head())
```

       sepal_length  sepal_width  petal_length  petal_width species
    0           5.1          3.5           1.4          0.2  setosa
    1           4.9          3.0           1.4          0.2  setosa
    2           4.7          3.2           1.3          0.2  setosa
    3           4.6          3.1           1.5          0.2  setosa
    4           5.0          3.6           1.4          0.2  setosa
    


```python
import seaborn as sns

iris = sns.load_dataset("iris")

print(iris.head())
```

       sepal_length  sepal_width  petal_length  petal_width species
    0           5.1          3.5           1.4          0.2  setosa
    1           4.9          3.0           1.4          0.2  setosa
    2           4.7          3.2           1.3          0.2  setosa
    3           4.6          3.1           1.5          0.2  setosa
    4           5.0          3.6           1.4          0.2  setosa
    


```python
import pandas as pd

df=pd.read_csv('C:/Users/user/Downloads/IRIS.csv')

print(df.head())

```


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_9968\3984699131.py in <module>
          1 import pandas as pd
          2 
    ----> 3 df=pd.read_csv('C:/Users/user/Downloads/IRIS.csv')
          4 
          5 print(df.head())
    

    ~\anaconda3\lib\site-packages\pandas\util\_decorators.py in wrapper(*args, **kwargs)
        309                     stacklevel=stacklevel,
        310                 )
    --> 311             return func(*args, **kwargs)
        312 
        313         return wrapper
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in read_csv(filepath_or_buffer, sep, delimiter, header, names, index_col, usecols, squeeze, prefix, mangle_dupe_cols, dtype, engine, converters, true_values, false_values, skipinitialspace, skiprows, skipfooter, nrows, na_values, keep_default_na, na_filter, verbose, skip_blank_lines, parse_dates, infer_datetime_format, keep_date_col, date_parser, dayfirst, cache_dates, iterator, chunksize, compression, thousands, decimal, lineterminator, quotechar, quoting, doublequote, escapechar, comment, encoding, encoding_errors, dialect, error_bad_lines, warn_bad_lines, on_bad_lines, delim_whitespace, low_memory, memory_map, float_precision, storage_options)
        676     kwds.update(kwds_defaults)
        677 
    --> 678     return _read(filepath_or_buffer, kwds)
        679 
        680 
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in _read(filepath_or_buffer, kwds)
        573 
        574     # Create the parser.
    --> 575     parser = TextFileReader(filepath_or_buffer, **kwds)
        576 
        577     if chunksize or iterator:
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in __init__(self, f, engine, **kwds)
        930 
        931         self.handles: IOHandles | None = None
    --> 932         self._engine = self._make_engine(f, self.engine)
        933 
        934     def close(self):
    

    ~\anaconda3\lib\site-packages\pandas\io\parsers\readers.py in _make_engine(self, f, engine)
       1214             # "Union[str, PathLike[str], ReadCsvBuffer[bytes], ReadCsvBuffer[str]]"
       1215             # , "str", "bool", "Any", "Any", "Any", "Any", "Any"
    -> 1216             self.handles = get_handle(  # type: ignore[call-overload]
       1217                 f,
       1218                 mode,
    

    ~\anaconda3\lib\site-packages\pandas\io\common.py in get_handle(path_or_buf, mode, encoding, compression, memory_map, is_text, errors, storage_options)
        784         if ioargs.encoding and "b" not in ioargs.mode:
        785             # Encoding
    --> 786             handle = open(
        787                 handle,
        788                 ioargs.mode,
    

    FileNotFoundError: [Errno 2] No such file or directory: 'C:/Users/user/Downloads/IRIS.csv'



```python

```
