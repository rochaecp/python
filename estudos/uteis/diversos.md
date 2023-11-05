# Diversos

## Converter um colab em .md

- Baixe o .ipynb do colab e faça upload no ambiente de execução (diretório /content/)
- Rode a seguinte linha no mesmo colab:

~~~bash
!jupyter nbconvert --to markdown filename.ipynb
~~~