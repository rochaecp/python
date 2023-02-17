# Pymupdf - Ler imagens de um PDF

## Gerar uma imagem para cada página do PDF

~~~python
import fitz

doc = fitz.open('example.pdf')
for page in doc:
    pix = page.get_pixmap(matrix=fitz.Identity, dpi=None,
                          colorspace=fitz.csRGB, clip=None, alpha=True, annots=True)
    pix.save("samplepdfimage-%i.jpg" % page.number)  # save file
~~~

## Gerar uma imagem para cada imagem de uma única página do PDF

~~~python
import fitz

doc = fitz.open('example.pdf')
page = doc.load_page(4) # abrir apenas a pagina 4
img_counter = 1
images = page.get_images(full=False)
for image in images:
    xref = image[0]
    pix = fitz.Pixmap(doc, xref)
    pix.save("%i.jpg" % img_counter)
    img_counter += 1
~~~