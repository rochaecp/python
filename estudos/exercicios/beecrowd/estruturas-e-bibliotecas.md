# Python - Beecrowd

### 1022 - TDA Racional

~~~python
def mdc(m, n):
    if n > m:
        return mdc(abs(n), abs(m))
    elif n == 0:
        return abs(m)
    else:
        return mdc(abs(n), abs(m % n))

testes = int(input())

while testes != 0:
    linha = input().split(" ")
    n1 = int(linha[0])
    d1 = int(linha[2])
    op = linha[3]
    n2 = int(linha[4])
    d2 = int(linha[6])

    if op == '+':
        n = n1 * d2 + n2 * d1
        d = d1 * d2
    elif op == '-':
        n = n1 * d2 - n2 * d1 
        d = d1 * d2
    elif op == '*':
        n = n1 * n2
        d = d1 * d2
    elif op == '/':
        n = n1 * d2
        d = n2 * d1
    
    max = mdc(n, d)
    print("{}/{} = {}/{}".format(n, d, n // max, d // max))
        
    testes -= 1
~~~

### 1023 - 

~~~python

~~~

### 1025 - Onde está o Mármore?

~~~python
from bisect import bisect_left
def find(number,arr):
    index = (bisect_left(arr,number))

    if index < len(arr) and arr[index] == number:
       return index + 1
    else:
       return -1

seq = 1
while True:
    n, q = list(map(int,input().split()))
    if n == 0 and q == 0:
        break

    print("CASE# %d:" % seq)
    seq += 1
    lista = []
    for i in range(n+q):
        if i < n:
            lista.append(int(input()))

        if i == (n-1):
            lista.sort()

        if i >= n:
            pesq = int(input())
            index = find(pesq, lista)

            if index == -1:
                print(str(pesq) + " not found")
            else:
                print(str(pesq) + " found at " + str(index))
~~~