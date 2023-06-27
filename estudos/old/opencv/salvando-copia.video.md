# OpenCV

## Salvando uma cópia de um vídeo (webcam)

~~~python
import cv2

captura = cv2.VideoCapture(0) # abre a webcam 0
video_saida = cv2.VideoWriter(
    'videoFinal.avi', cv2.VideoWriter_fourcc(*'XVID'), 20.0, (640, 480)) # 20.0 frames, (640, 480) == tamanho 

while (captura.isOpened()):
    check_captura, frame = captura.read() # captura frame
    if check_captura == True:
        cv2.imshow('Video Capturado', frame) # exibe o frame na tela
        video_saida.write(frame) # salva o frame
        if cv2.waitKey(1) & 0xFF == ord('x'): # 1 é o tempo mínimo, tecla x fecha
            break

captura.release() # fecha a webcam
video_saida.release() # fecha o video de saida
cv2.destroyAllWindows() # fecha todas as janelas    
~~~