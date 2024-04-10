# Python - Exercícios

### 1028 - Figurinhas

~~~python
def mdc(m, n):
  if n > m:
    return mdc(abs(n), abs(m))
  elif n == 0:
    return abs(m)
  else:
    return mdc(abs(n), abs(m % n))

f1 = f2 = 0
n = int(input())

for i in range(0, n):
  linha = input().split(" ")
  f1, f2 = int(linha[0]), int(linha[1])
  print(mdc(f1, f2))
~~~