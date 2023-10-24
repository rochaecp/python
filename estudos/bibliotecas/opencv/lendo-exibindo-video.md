# OpenCV

## Lendo e exibindo um vídeo a partir da webcam

~~~python
import cv2

captura = cv2.VideoCapture(0) # abre a webcam 0

while (captura.isOpened()):
    check_captura, frame = captura.read() # captura frame
    if check_captura == True:
        cv2.imshow('Video Capturado', frame) # exibe o frame na tela
        if cv2.waitKey(1) & 0xFF == ord('x'): # 1 é o tempo mínimo, tecla x fecha
            break

captura.release() # fecha a webcam
cv2.destroyAllWindows() # fecha todas as janelas        
~~~

## Lendo e exibindo um arquivo de vídeo

~~~python
import cv2

captura = cv2.VideoCapture('video1.avi') # abre um video

while (captura.isOpened()):
    check_captura, frame = captura.read() # captura frame
    if check_captura == True:
        cv2.imshow('Video Capturado', frame) # exibe o frame na tela
        if cv2.waitKey(20) & 0xFF == ord('x'): # 1 é o tempo mínimo, tecla x fecha
            break
    if check_captura == False:
        break        

captura.release() 
cv2.destroyAllWindows() # fecha todas as janelas
~~~
