# Aprendiendo Tailwind

Repositorio personal para llevar nota de los avances con el [curso de freeCodeCamp](https://www.youtube.com/watch?v=5HtRcMSO1Ro) para aprender TailwindCSS.

## Index

- Instalación

## Instalación

Hay 2 métodos principales para la instalación de la herramienta, la primera es utilizar el enlace del playground, ideal para entornos de desarrollo y pruebas rápidas. Para utilizarlo simplemente hay que agregar en el archivo `html` una etiqueta script de la siguiente manera:

```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tailwind</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  </head>
  <body>
    <!-- CONTENIDO DEL SITIO-->
  </body>
</html>
```

La segunda opción es la instalación por medio de la consola, para esto primero debemos instalar `tailwindcss` y `@tailwindcss/cli` por medio de npm.

```cmd
npm install tailwindcss @tailwindcss/cli
```

Seguido se añade `@import "tailwindcss";` al archivo css principal.
Ahora ejecutamos el siguiente comando para escanear los archivos de origen y crear el CSS necesario.

```cmd
npx @tailwindcss/cli -i src/input.css -o src/output.css --watch
```

Finalmente se añade el CSS Compilado al `<head>` y se puede empezar a Tailwind.

## Colores

Para utilizar colores personalizados en Tailwind se añade en el CSS principal la espacio de nombre `--color-*` en los temas:

```CSS
@import "tailwindcss";

@theme {
  --color-kz: #b7144e;
  --color-midnight: #121063;
  --color-tahiti: #3ab7bf;
  --color-bermuda: #78dcca
}

```

Ahora puedes utilizarlos sin complicaciones en conjunto a las otras clases de utilidad de Tailwind.

```HTML
<h1 class="text-3xl font-bold underline bg-kz text-white">
    Tailwind en freeCodeCamp
</h1>
```
