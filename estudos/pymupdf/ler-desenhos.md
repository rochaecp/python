# Pymupdf - Ler desenhos de um PDF

## Gerar uma página de pdf com todos os desenhos de outra página de pdf

~~~python
import fitz
doc = fitz.open("example.pdf")
page = doc[3]
paths = page.get_drawings()  # extrai os desenhos
# this is a list of "paths", which can directly be drawn again using Shape
# -------------------------------------------------------------------------
#
# define some output page with the same dimensions
outpdf = fitz.open()
outpage = outpdf.new_page(width=page.rect.width, height=page.rect.height)
shape = outpage.new_shape()  # make a drawing canvas for the output page
# --------------------------------------
# loop through the paths and draw them
# --------------------------------------
for path in paths:
    # ------------------------------------
    # draw each entry of the 'items' list
    # ------------------------------------
    for item in path["items"]:  # these are the draw commands
        if item[0] == "l":  # line
            shape.draw_line(item[1], item[2])
        elif item[0] == "re":  # rectangle
            shape.draw_rect(item[1])
        elif item[0] == "qu":  # quad
            shape.draw_quad(item[1])
        elif item[0] == "c":  # curve
            shape.draw_bezier(item[1], item[2], item[3], item[4])
        else:
            raise ValueError("unhandled drawing", item)
    # ------------------------------------------------------
    # all items are drawn, now apply the common properties
    # to finish the path
    # ------------------------------------------------------
    shape.finish(
        fill=path["fill"],  # fill color
        color=path["color"],  # line color
        dashes=path["dashes"],  # line dashing
        even_odd=path.get("even_odd", True),  # control color of overlaps
        closePath=path["closePath"],  # whether to connect last and first point
        lineJoin=path["lineJoin"],  # how line joins should look like
        lineCap=max(path["lineCap"]),  # how line ends should look like
        width=path["width"],  # line width
        stroke_opacity=path.get("stroke_opacity", 1),  # same value for both
        fill_opacity=path.get("fill_opacity", 1),  # opacity parameters
        )
# all paths processed - commit the shape to its page
shape.commit()
outpdf.save("drawings-page-0.pdf")
~~~

























