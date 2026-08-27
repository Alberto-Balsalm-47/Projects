# Índice de Diseñadores

Guía de moda construida sobre archivo. Portada, y ficha de autor con
método, técnica, obra y bibliografía, en español e inglés.

Primer diseñador publicado: **Carol Christian Poell**. Kei Kagami, en preparación.

**En vivo:** <https://alberto-balsalm-47.github.io/Projects/> — no hace falta
clonar ni correr nada; se reconstruye solo con cada push a `main`.

## Estructura

```
index.html              el sitio entero (un solo archivo, sin dependencias)
fuentes/                los PDF de referencia          ← ver más abajo
archivo/poellinfo/      imágenes y clips del archivo   ← ver más abajo
```

No usa webfonts, ni librerías, ni build. Se abre igual desde el disco
(doble clic en `index.html`) que servido por GitHub Pages.

## Publicar

Ya está activado: Settings → Pages → Source **Deploy from a branch**, rama
`main`, carpeta `/ (root)`. Cada push a `main` publica en un minuto en
<https://alberto-balsalm-47.github.io/Projects/>.

## Las fuentes

Cada entrada de la ficha remite a su fuente. A dónde apunta cada remisión
lo decide `FUENTES_LOCALES`, arriba de todo en `index.html`:

**`false` (como está ahora).** Los enlaces van al lugar público de cada
fuente: Internet Archive para *Fashion Now 2* y *Landed–Geland* (con la
página exacta), la editorial para Lehmann, HAL (repositorio académico de
acceso abierto) para el capítulo de Michel, un flipbook público de Yumpu
para el editorial de FLUX, el perfil de @poellinfo para el archivo de
imágenes. No hace falta subir nada.

**`true`.** Los enlaces van a los archivos de este repositorio, con
`#page=` — la página exacta en los seis PDF. Para eso hay que copiar los
archivos en `fuentes/` con estos nombres:

| Archivo en `fuentes/` | Original |
|---|---|
| `michel-thought-without-concept.pdf` | CCP Thought without Concept Christian MICHEL.pdf |
| `lehmann-fashion-and-materialism.pdf` | fashion-and-materialism-9781474407922_compress.pdf |
| `flux-54-u-turn.pdf` | Carol Christian Poell.pdf |
| `fashion-now-2.pdf` | fashionnow2idsel0000unse_1.pdf |
| `landed-geland-2001.pdf` | fashion2001lande0000unse_1.pdf |
| `moda-historia-de-los-disenos-y-estilos.pdf` | moda-historia-de-los-disenos-y-estilos.pdf |

y el contenido de `@poellinfo instagram` en `archivo/poellinfo/`.

Antes de hacerlo, tener presente que un repositorio público con Pages
activado **publica** esos archivos. *Fashion and Materialism* (Edinburgh
University Press) y *Fashion Now 2* (Taschen) son libros con derechos
vigentes. Los cuatro clips de vídeo del archivo (`archivo/poellinfo/*.mp4`)
sí se cargan siempre desde el repositorio: sin ellos, esas cuatro fichas
de vídeo quedan vacías.

## Editar el contenido

Todo el texto vive en `index.html`, en el objeto `CCP`, como pares
`[español, inglés]`. Agregar un idioma es agregar una posición al par.
Agregar un diseñador es agregar un objeto a `DESIGNERS` y su ficha.
