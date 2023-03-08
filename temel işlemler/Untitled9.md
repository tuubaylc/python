# dosya açma kapama

dosyaları açmak için open tırnak içinde bir isim beriyoruz virgül "w" oluyor.


```python
file=open("c:/users/user/desktop/bilgiler.txt,""w")
```


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_3592\3221944476.py in <module>
    ----> 1 file=open("c:/users/user/desktop/bilgiler.txt,""w")
    

    FileNotFoundError: [Errno 2] No such file or directory: 'c:/users/user/desktop/bilgiler.txt,w'



```python
file.close() #unutmayalım. dosyanın kapanması için close
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp\ipykernel_3592\1665129403.py in <module>
    ----> 1 file.close() #unutmayalım. dosyanın kapanması için close
    

    NameError: name 'file' is not defined



```python
file=open("bilgiler.txt","w",encoding="utf-8")
```


```python
file=open("D:/abc/bilgiler.txt","r",encoding= "utf-8")
for i in file: # tıpkı listeler gibi dosyanın  her bir satırına 
    print (i) # her bir satırı ekrana basıyoruz.
    
```

    merhaba pınarhisar nasılsın
    


```python
print(file.readline())# ilk satırı okuyor
```

    
    


```python
file.readlines()# alt alta bigiler geliyor
```




    []




```python

```
