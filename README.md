# Portafolio de Cristhian Rossi

Sitio estático (HTML y CSS a mano, sin compilar nada) que se publica con GitHub Pages en
<https://portafolio-cristhian-rossi.github.io/>.

## Verlo en local

Desde la carpeta del sitio:

```
python -m http.server 8090
```

y abrir <http://localhost:8090/>. Se ve igual que publicado.

## Etapas

1. **Local, con datos reales:** se arma y se revisa en `auto-catalog/portafolio/`, que no
   entra a git.
2. **Publicada, con datos de prueba:** imágenes difuminadas y sin el PDF, para probar el
   circuito de GitHub Pages sin publicar datos del negocio.
3. **Publicada, con datos reales:** con el permiso del dueño.

Para armar la copia que se publica (desde la raíz de auto-catalog):

```
.venv\Scripts\python portafolio\_herramientas\armar_publicacion.py <carpeta del repo publicado> --etapa prueba
.venv\Scripts\python portafolio\_herramientas\armar_publicacion.py <carpeta del repo publicado> --etapa real
```

Al final corre el verificador; si dice algo distinto de `OK`, no se publica.

## Sumar un proyecto

1. Copiar la carpeta `auto-catalog/` con el nombre del proyecto nuevo y cambiar su
   contenido y sus imágenes.
2. Agregar una tarjeta `.proyecto` en el `index.html` de inicio.
3. Correr `verificar_sitio.py` sobre la carpeta del sitio.
