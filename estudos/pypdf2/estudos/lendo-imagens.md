# PyPDF2 - Lendo imagens de um PDF

## Lendo todas as imagens de uma página de um PDF

~~~python
from PyPDF2 import PdfReader

reader = PdfReader("example.pdf")

page = reader.pages[0]
count = 0

for image_file_object in page.images:
    with open(str(count) + image_file_object.name, "wb") as fp:
        fp.write(image_file_object.data)
        count += 1 
~~~



