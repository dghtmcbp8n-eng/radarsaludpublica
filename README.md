# Radar en Salud Pública

Boletín semanal de evidencia en salud pública, epidemiología y metodología de la
investigación, dirigido a la comunidad universitaria y al público general.

Sitio: https://radarsaludpublica.cl

## Cómo funciona

Cada lunes, una tarea automatizada ejecuta cinco búsquedas fijas en PubMed, aplica
criterios de selección definidos de antemano, redacta las fichas y actualiza este
repositorio. Cuatro de las búsquedas se acotan a los siete días previos; la quinta,
dedicada a la producción latinoamericana, usa una ventana de catorce días, porque esa
literatura entra a PubMed con más retraso. PubMed es la única fuente: LILACS/BVS,
SciELO y Web of Science se evaluaron y quedaron descartadas, las dos primeras porque
bloquean el acceso automatizado y la tercera porque exige credenciales institucionales. Cloudflare Pages despliega el sitio con cada cambio.

La página declara de forma permanente que se genera con inteligencia artificial y que
nadie revisa el resultado antes de publicarlo. Los criterios de selección están
descritos en la propia página, en la sección "Cómo se arma este boletín".

## Estructura

```
index.html              portada, siempre la edición más reciente
ediciones/NN.html       ediciones archivadas, con dirección permanente
404.html                página de error
robots.txt              indexación
sitemap.xml             mapa del sitio; se agrega una entrada por edición
_headers                cabeceras de seguridad y caché para Cloudflare Pages
```

## Al publicar una edición nueva

1. Archivar la portada saliente como `ediciones/NN.html`, sin el menú lateral y con el
   banner de edición archivada.
2. Escribir la portada nueva en `index.html`, con su entrada agregada al desplegable
   "Ediciones anteriores" del menú.
3. Agregar la nueva edición a `sitemap.xml`.
4. Confirmar los cambios y subirlos. El despliegue es automático.

Las ediciones archivadas no se modifican nunca.
