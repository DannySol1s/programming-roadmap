# Pillow

**Categoría:** Python / Procesamiento de imágenes
**Visto en:** _(pendiente — agrega aquí el proyecto donde lo uses)_

## Definición

Pillow es una biblioteca de Python para trabajar con imágenes. Permite abrir y guardar archivos, convertir formatos, modificar el tamaño, recortar, rotar y aplicar filtros o ajustes como cambios de color, brillo y contraste.

También ofrece herramientas para crear imágenes desde cero y dibujar texto, formas y otros elementos sobre ellas. Es el paquete moderno que continúa el desarrollo de la antigua biblioteca PIL (Python Imaging Library).

## Ejemplo

Abrir una imagen, cambiar su tamaño y guardarla en otro formato:

```python
from PIL import Image

with Image.open("foto.jpg") as imagen:
    redimensionada = imagen.resize((800, 600))
    redimensionada.save("foto.png")
```

Pillow se instala con pip:

```bash
pip install Pillow
```

