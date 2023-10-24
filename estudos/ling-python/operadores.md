# Operadores

## Operador de Atribuição  

| Operador  | Nome do Operador  | Exemplo    |
| :---:     | :---:             | :---:      |
| ```=```   | Atribuição        |            |

## Operadores de atribuição ampliada (ou atribuição composta)  

| Operador     | Nome do Operador       | Exemplo    |
| :---:     | :---:                     | :---:      |
| ```+=```  | Atribuição de adição      |            |
| ```-=```  |                           |            |
| ```*=```  |                           |            |
| ```/=```  |                           |            |
| ```%=```  |                           |            |
| ```&=```  |                           |            |
| ```&=```  |                           |            |    
| ```\|=``` |                           |            | 
| ```^=```  |                           |            | 
| ```>>=``` |                           |            | 
| ```<<=``` |                           |            |

## Operadores Aritméticos 

| Operador  | Nome do Operador          | Exemplo       |
| :---:     | :---:                     | :---:         |
| ```+```   | Adição                    |               |
| ```-```   | Subtração                 |               |
| ```*```   | Multiplicação             |               |
| ```**```  | Exponenciação             | 7 ** 2 == 49  |
| ```/```   | Divisão                   |               |
| ```//```  | Divisão inteira           |               |
| ```%```   | Módulo                    |               |
| ```++```  | Pré ou pós incremento     |               |
| ```--```  | Pré ou pós decremento     |               |

## Operadores Relacionais  

| Operador  | Nome do Operador      | Exemplo       |
| :---:     | :---:                 | :---:         |
| ```==```  | Igualdade             |               | 
| ```!=```  | Desigualdade          |               |
| ```>```   |                       |               |
| ```<```   |                       |               |
| ```>=```  |                       |               |
| ```<=```  |                       |               |

## Operadores Lógicos    

| Operador      | Nome do Operador      | Exemplo       | 
| :---:         | :---:                 | :---:         |
| ```and```     | E lógico              |               | 
| ```or```      | OU lógico             |               | 
| ```not```     | NÃO lógico            |               | 

## Operadores de Identidade    

| Operador      | Nome do Operador      | Exemplo       | 
| :---:         | :---:                 | :---:         |
| ```is```      |                       |               | 
| ```is not```  |                       |               | 

## Operadores de Associação    

| Operador      | Nome do Operador      | Exemplo       | 
| :---:         | :---:                 | :---:         |
| ```in```      |                       |               | 
| ```not in```  |                       |               | 

## Operadores Bitwise (bit a bit)   

| Operador  | Nome do Operador | Exemplo                            |
| :---:     | :---:            | :---:                              |
| ```&```   | AND              |                                    | 
| ```\|```  | OR               |                                    |
| ```~```   | NOT              |                                    |
| ```^```   | XOR              |                                    |
| ```<<```  | left SHIFT       |                                    |
| ```>>```  | right SHIFT      | 5 >> 1 gera 2 pois 0101 vira 0010  |

## Operador Condicional (Operador Ternário)

~~~python
min = a if a < b else b
~~~

~~~python
print("a é maior") if a > b else print("b é maior")
~~~

~~~python
print("a é maior") if a > b else print("a igual a b") if a == b else print("b é maior")
~~~