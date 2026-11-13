# Nuestros juegos

Página sencilla de juegos para David y Natalia:

- **Sopa de letras** con 16 palabras de la relación.
- **¿Dónde fue?**: 13 fotos, tres opciones por foto.

## Archivos

```
index.html                 ← portada con la lista de juegos
estilos.css                ← colores y estilos compartidos por todos los juegos
sopa-de-letras/index.html  ← la sopa de letras
donde-fue/index.html       ← el juego de fotos
donde-fue/fotos/           ← las fotos (reducidas y sin datos de ubicación)
```

## Agregar fotos a «¿Dónde fue?»

1. Sube la foto a `donde-fue/fotos/` (por ejemplo `14.jpg`). Mejor si pesa menos de 400 KB.
2. En `donde-fue/index.html`, dentro de `FOTOS`, agrega una línea. La primera opción es la correcta:

```js
{ foto: "14.jpg", opciones: ["Respuesta correcta", "Opción falsa 1", "Opción falsa 2"] },
```

## Dónde está publicada

https://ndavidb.github.io/nuestros-juegos/

Se publica con GitHub Pages desde la rama `main`. Cada cambio que se sube a `main` aparece en la página en uno o dos minutos. También puedes editar los archivos directo en github.com (ícono del lápiz) y darle **Commit changes**.

Ojo: con GitHub Pages gratis el repositorio y la página son públicos. Cualquiera con el enlace puede verla.

## Cómo se juega entre los dos

- Los dos abren el mismo enlace y les sale **la misma sopa**.
- El reloj arranca cuando tocas el tablero. Cada pista (💡) suma 20 segundos.
- Al terminar sale el mensaje sorpresa y el botón **Enviar mi tiempo** para mandárselo al otro.
- **Nueva sopa** cambia la posición de las letras. Después usa **Retar a mi pareja** para enviarle el enlace nuevo, así juegan la misma.

## Cambiar palabras o el mensaje

Abre `sopa-de-letras/index.html` y busca el bloque que dice `PARA EDITAR`. Cada palabra es una línea:

```js
{ pista: "Primer beso", respuesta: "Carpita" },
```

Escribe la respuesta normal, con tildes y espacios. El juego quita solo tildes y espacios. Ahí mismo están `MENSAJE_FINAL` y `TAMANO` (la sopa es de 18×18; súbelo si agregas palabras muy largas).
