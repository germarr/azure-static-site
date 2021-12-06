Durante mucho tiempo estuve buscando opciones para poder crear sitios estáticos y publicarlos rápidamente. Desupés de mucha experimentación con decenas de servicios decidi que este es el stack que más me gusta. 

## 1, Creando nuestro sitio muestra.
Para este ejemplo generaremos un sitio estatico usando html y tailwindcss. El primer paso es crear una carpeta llamada ´sitio-estatico-tailwind´. Dentro de esta carpeta guardaremos todos los archivos que usaremos para generar nuestro sitio.

´´´bash
mkdir sitio-estatico-tailwind
cd sitio-estatico-tailwind
´´´

Estando dentro de la carpeta ´sitio-estatico-tailwind´ iniciemos un archivo ´package.json´ este archivo llevará el seguimiento de los paquetes de javascript que usaremos para este proyecto. (Para este punto ya tienes que tener ´node´ instalado.

´´´bash
npm init -y
´´´
Ahora instalaremos [Tailwind](). Usando la terminal agregar los siguientes comando:

´´´bash
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest postcss-cli@latest
npx tailwindcss init -p
touch styles.css
mkdir str
´´´

Esto nos generará la estructura básica de archivos que necesitamos para utilizar Tailwind desde nuestro sitio estático. El siguiente paso es abrir el archvio ´styles.css´ y agregar el siguiente código:

´´´css
/* styles.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
´´´

Ahora abrimos nuestro archivo ´package.json´ y editamos valor de la llave ´scripts´ :

´´´json
  "scripts": {
    "build": "postcss styles.css -o src/styles.css"
  },
´´´

Para este punto, debemos tener dentro de nuestra carpeta ´sitio-estatico-tailwind´ un folder llamado ´src´, desplazemonos al mismo y generemos un archivo llamado ´index.html´ y copiamos este código:

´´´html
<!--index.html-->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Como hicimos esta página?</title>
    <link rel="stylesheet" href="./styles.css">
</head>
<body>
    <div class="w-screen h-screen bg-blue-200 flex items-center justify-center">
        <h1 class="text-6xl font-semibold">Hola! ✌️</h1>
    </div>
</body>
</html>
´´´

Listo tenemos una página estatica sencilla estilizada con TailwindCSS. 

## 2, Crear un Repositiorio para nuestro sitio en Github
Github es una plataforma que nos permite hacer control de versiones en nuestras aplicaciones web. 

## 3, Comprar un dominio web
Existen cientos de p'agianas que te permiten comprar nombres de dominios y la mayoría ofrece la misma funcionalidad. En esta ocasión voy a utilizar [Namecheap](https://namecheap.com/)

## 4. Obtener certificado SSL


## 3 Creando una cuenta de Azure
Azure es la nube de Microsoft, tiene decenas de funciones. Puede hostear desde sitios estáticos sencillos (como el que estamos por realizar) hasta aplicaciones que escalan casi al infinito.
Es muy sencillo crear una cuenta de Azure, solo debes visitar este [siitio]() y seguir las instrucciones.

## 4 Publicar
