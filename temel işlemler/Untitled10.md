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

```
