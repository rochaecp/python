# OpenCV

O cv2 lê a imagem como BGR (e não como RGB) e isso pode gerar alterações na imagem.  

## Lendo e exibindo uma imagem com o cv2

~~~python
import cv2                           # pip install opencv-python
from matplotlib import pyplot as plt # pip install matplotlib

imagem = cv2.imread('imagem1.jpg')   # lendo a imagem

cv2.imshow('Nome da Janela', imagem)    # exibindo a imagem com o cv2
cv2.waitKey(0)                          # 0 == permace com a janela aberta sempre
cv2.destroyAllWindows()
~~~

## Lendo, realizando o resize e exibindo uma imagem com o cv2

~~~python
import cv2 
from matplotlib import pyplot as plt 

imagem = cv2.imread('imagem1.jpg')

altura = imagem.shape[0]    # obtem a altura da imagem
largura = imagem.shape[1]   # obtem a largura da imagem

porcentagem_dimensao = 50
nova_largura = int(largura * porcentagem_dimensao / 100)
nova_altura = int(altura * porcentagem_dimensao / 100)
dim = (nova_largura, nova_altura)
imagem_reduzida = cv2.resize(imagem, dim, interpolation= cv2.INTER_AREA) # reduz a imagem

cv2.imshow('Nome da Janela', imagem_reduzida)   # exibindo a imagem com o cv2
cv2.waitKey(0)                                  # 0 == permace com a janela aberta sempre
cv2.destroyAllWindows()
~~~

## Lendo, convertendo para escala de cinza e exibindo uma imagem com o cv2

~~~python
import cv2
from matplotlib import pyplot as plt

imagem = cv2.imread('imagem1.jpg', 0) # 0 == le em escala de cinza

cv2.imshow('Nome da Janela', imagem)
cv2.waitKey(0)
cv2.destroyAllWindows()
~~~

## Lendo, convertendo de BGR para RGB e exibindo uma imagem com o matplotlib

~~~python
import cv2
from matplotlib import pyplot as plt

imagem = cv2.imread('imagem1.jpg')

imagem_rgb = cv2.cvtColor(imagem, cv2.COLOR_BGR2RGB) # convertendo de BGR para RGB

plt.imshow(imagem_rgb) 
plt.show() # exibindo a imagem com o matplotlib
~~~