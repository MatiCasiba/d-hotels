* Nombre: Matias Casiba
* Link Github Repo: https://github.com/MatiCasiba/d-hotels
* Link Netlify: https://disney-hoteles.netlify.app/

# Página de habitaciones

## Colocando titulos, subtitulos y textos
En la página para trabajar con los textos, estaré usando los elementos:
```sh
<h1> Titulo </h1>
<h2 lang="en"> Subtitulos </h2>
<p> texto </p>
```
* Nota: dentro del archivo index.html, en los elementos de h2 estaré usando lang="en" debido a que los subtítulos se encuentran en ingles.

## Agregando imágenes
Al momento de agregar las imágenes usaré el elemento:
```sh
<img src="direccion-de-imagen" alt="nombre de la imagen">
```

## Dándole estilo al logo y las imágenes
### Logo
Primero, al momento de trabajar con el logo de la página, estaré agregando un elemento div con una clase en el archivo index.html:
```sh
<div class="logo" >
    <img src="/image/logo-disney-hotels.webp" alt="logo de disney">
</div>
```
Luego trabajaré con esta clase en el archivo style.css:
```sh
img{
    width: 40%; # ocupa el 40% del ancho de la pantalla
    height: auto; # su alto quedará en automatico
}
.logo{
    text-align: center; # se encarga de centrar la imagen en el contenedor div
}
```
* Nota: con el width en 40%, voy a lograr que la imagen/logo se vaya disminuyendo cada vez que achique la pantalla, y si amplio la pantalla, se agranda el logo.

### Estilo en las demás imagenes
Vas a notar que las 4 imágenes que se encuentran en la página actuan de manera diferente, pues para lograr esto, tuve que agregar en el archivo index.htnml, clases con distinto valor en los elementos img, para luego trabajar con estos en el archivo css:
* index.html
```sh
<img class="imagen-derecha" src="/image/hoteles/disneys-pop-century-resort.webp" alt="imagen Disney pop century">
<img class="imagen-izquierda" src="/image/hoteles/disneys-caribbean-beach-resort.webp" alt=" imagen Disney Caribbean Beach">
<img class="imagen-derecha" src="/image/hoteles/disneys-animal-kingdom-lodge.webp" alt="imagen Disney animal Kingdom">
<img class="ancho-total" src="/image/mickey-minnie.webp" alt="imagen de mickey y minnie">
```

* style.css
```sh
.imagen-derecha{
    width: 300px;
    float: inline-end; # hace que la imágen se coloque a la derecha
    margin: 0 0 0 10px; # estos 4 valores se ven: margen arriba(0) derecha(0) abajo(0) izquierda(10px). Lo que quiere dececir que habra espacio en el margen izquierdo
}
.imagen-izquierda{
    width: 300px;
    float: inline-start; # la imagen se coloca al inicio (en la parte izquierda de la página)
    margin: 0 10px 0 0; # lo mismo que en la clase imagen-derecha, solo que ahora tendremos espacio en el margen derecho de 10px
}
.ancho-total{
    width: 100%; # ocupa el ancho total en la página
    height: auto;
}
```
* Nota: lo que genera que la imágen se coloque al lado de los textos es el "float".

## Dando color y diseño a la página 

Se le agregaron colores y fuetntes a los elementos h1, h2 y p:
```sh
h1{
    font-size: 40px; # tamaño de letra
    font-weight: normal; # grosor de la letra
    text-align: center; # para centrar el titulo
    letter-spacing: 10px; # espacios entre las letras
}
h2{
    font-size: 20px; 
    font-weight: normal;
    letter-spacing: 5px;
}
p{
    font-size: 10px;
    color: #3264a7; # color de texto
}
```
* Nota: para lograr el efecto de espacio entre las letras, usé el letter-spacing para que sea más prolijo.

### Diseño en el cuerpo de la página
Al momento de usar una fuente, lo use solamente en el body, para que sea hereditario a los elementos h1, h2 y p, esto me ahorrará de tener que estar escribiendo "font-family" en cada elemento:
```sh
body{
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    color: rgb(192,83,150);
}
```

## Actualización del ancho-total
En la clase ancho-total eh agregado un margin-top, cuando la pantalla se hacía más angosta, la imagen ultima se unia con la anteultima, entonces con este margin, se va a separar de la anteultima imagen.
```sh
.ancho-total{
    margin-top: 5px;
}
```
