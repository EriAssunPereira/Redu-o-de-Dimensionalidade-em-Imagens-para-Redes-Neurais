# Redu-o-de-Dimensionalidade-em-Imagens-para-Redes-Neurais

Aqui está o código em Python que descreve como transformar uma imagem colorida para níveis de cinza e para uma versão binarizada:

```python
import cv2

# Carregar a imagem colorida
imagem = cv2.imread('caminho/para/a/imagem.jpg')

# Converter a imagem para tons de cinza
cinza = cv2.cvtColor(imagem, cv2.COLOR_BGR2GRAY)

# Aplicar um limiar para obter uma imagem binarizada
_, binarizada = cv2.threshold(cinza, 127, 255, cv2.THRESH_BINARY)

# Mostrar as imagens
cv2.imshow('Imagem Original', imagem)
cv2.imshow('Imagem em Cinza', cinza)
cv2.imshow('Imagem Binarizada', binarizada)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

Este código realiza os seguintes passos:
1. Carrega a imagem original usando `cv2.imread`.
2. Converte a imagem para tons de cinza com `cv2.cvtColor`.
3. Aplica um limiar para binarização usando `cv2.threshold`, onde pixels com valores abaixo de 127 se tornam pretos (0) e acima se tornam brancos (255).
4. Exibe as imagens usando `cv2.imshow`.

Lembre-se de substituir `'caminho/para/a/imagem.jpg'` pelo caminho correto da sua imagem.
