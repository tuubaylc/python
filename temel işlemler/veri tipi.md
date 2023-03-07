```python
print("Merhaba\nNasılsın\niyi misin")
```

    Merhaba
    Nasılsın
    iyi misin
    


```python
print("selam\nGençler")
```

    selam
    Gençler
    


```python
print("Trakya\tKırklareli\tPınarhisar")
```

    Trakya	Kırklareli	Pınarhisar
    


```python
a=55
print(type(a))
```

    <class 'int'>
    

sep parametresi değerlerin arasına istediğimiz karakterlerin yazılmasını sağlar.


```python
print(3,4,5,6,7,8,9)
```

    3 4 5 6 7 8 9
    

sep parametresi sayesinde değerlerin arasına nokta konur.


```python
print(3,4,5,6,7,8,9,sep=".")
```

    3.4.5.6.7.8.9
    

değerlerin arasına "/" sembolü yerleştiriyor.


```python
print("ali","veli","kenan",sep="/")
```

    ali/veli/kenan
    

#yıldızlı parametreler

varsayılan olaak karakterlerin arasına boşluk konuluyor.


```python
print(*"python",sep="\n")
```

    p
    y
    t
    h
    o
    n
    


```python
print(*"TBMM",sep=".")
```

    T.B.M.M
    

float çevireceğimiz sayıyı parantez içine alıyoruz.


```python
a=43
float(a)
```




    43.0




```python

```
