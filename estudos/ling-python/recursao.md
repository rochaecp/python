# Recursão

- São funções que chamam a si mesmas.  

~~~python
def recursao(k):
    if(k > 0):
        result = k + recursao(k - 1)
        print(result)
    else:
        result = 0
    return result

recursao(6)
~~~
