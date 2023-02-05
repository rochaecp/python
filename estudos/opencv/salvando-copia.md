# OpenCV

## Salvando uma cópia de uma imagem

~~~python
import cv2
from matplotlib import pyplot as plt

imagem = cv2.imread('imagem1.jpg')

cv2.imwrite('nova_imagem.jpg', imagem) # salvando uma cópia da imagem
~~~