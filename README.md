# --Usabilidad y accesibilidad--

##-Introducción al protocolo HTTP-
### Autor: Manuel Ramón Regalado Peraza.

1º Enlace

http://www.gobiernodecanarias.org/istac/api/ → Botón derecho (Inspeccionar elemento)
Navegador usado: Mozilla Firefox

• Qué peticiones desencadena la consulta.

![img1](/images/1.png "imagen1")

4 peticiones de recurso GET.

• ¿Qué tipo de petición estás realizando?

Todas las peticiones que se hacen son de tipo GET que son peticiones de recurso, en este
caso 4 peticiones de ese tipo de la página sobre protocolo HTTP

• Qué código de estatus devuelve.

2 codigos de retorno 302 → Redirección (Found)
2 codigos de retorno 200 → Exitos(OK)

• Qué DNS tiene el servidor

![img2](/images/2.png "imagen2")

Con el DNS se asignó a la IP de la página el nombre lógico de
“www.gobiernodecanarias.org”

• Qué IP tiene tiene el servidor

Si hacemos un ping al “nombre de la página” nos devuelve una IP que debería ser de la
misma.

![img3](/images/3.png "imagen3")

La IP es: 93.188.137.123

La otra manera en la que el inspeccionador de elementos del navegador ha dado la IP es
refrescar la página con un F5, el cual ahora sí, ofrece como elemento la página en HTML, e
inspeccionándola nos da la IP, que es 93.188.137.123:80

![img4](/images/4.png "imagen4")

• ¿La página tiene alguna cookie?, ¿Cuáles?.

Ninguno de los elementos de la página fué devuelto con cookies como se muestra en la
pestaña de ‘cookies’ de la pestaña de ‘red’.

![img5](/images/5.png "imagen5")

• ¿Qué idioma acepta?

![img6](/images/6.png "imagen6")

es-ES →Español de España (Castellano)
en_US → Inglés de Estados Unidos

• Alguna línea de código JavaScript

La página no presenta ficheros javascript ni código javascript en el fichero HTML de la
página.

• Alguna línea de código CSS que se aplique

![img7](/images/7.png "imagen7")

Esto son estilos para el texto de cabecera H1 y H2.

.section h1, .section h2 {
padding-bottom: 10px;
font-weight: bold;
font-size: 25px;
}
.section h2 {
border-bottom: 1px solid rgb(214, 214, 214);
box-sizing: border-box;
}
.section h2 a {
color: #999999;
font-size: 18px;
text-decoration: none;
}
.section h2 a:hover{
color: black;
text-decoration: underline;
}
• Alguna línea de código HTML que se aplique.

![img8](/images/8.png "imagen8")

Éste es el código del enlace del texto “API de recursos estructurales” de la página escrito en
HTML

<h2>
<a href="http://www.gobiernodecanarias.org/istac/api/structural-resources/v1.0/#/" alt="API
de recursos estructurales">API de recursos estructurales</a>
</h2>

2º Enlace

https://www3.gobiernodecanarias.org/istac/api/operations/v1.0/operations?limit=5 → Botón
derecho sobre la página (Inspeccionar)

Se trata de un fichero XML a la que se le ha pasado como parámetro ‘limit=5’ (sabemos que
es un parámetro/argumento pues viene a continuación de un símbolo ‘?’, se llama ‘limit’ y contiene
el valor 5) dentro de la misma URL, como ésta es la única manera de pasarle parámetros a las
peticiones de tipo GET sabemos que es una petición de ese tipo.

Navegador usado: Google Chrome y Mozilla Firefox

• Qué peticiones desencadena la consulta.


NOTA: Tuve que recargar la página al menos una vez cuando ya estaba cargada para que se
generaran y mostraran las peticiones por pantalla.

En Chrome tenemos dos respuestas de tipo 200 (creado, OK), una del documento XML que
se ha cargado al entrar a dicha URL y otro pertenece al recurso de una imagen en caché de la página
“http://www.w3.org/2000/svg”. Ambas respuestas son fruto de hacer un GET a esta página como
veremos en el siguiente punto.

![img9](/images/9.png "imagen9")

En Firefox en cambio se puede apreciar dos codigos de respuesta, en este caso:

-Un código de retorno tipo 200 (Correcto, OK) sobre un fichero XML que es la
página web.
-Un código de retorno tipo 404 (Error del cliente. Not Found) sobre una imagen
llamada “favicon.ico” que no logra encontrar.

![img10](/images/10.png "imagen10")

• ¿Qué tipo de petición estás realizando?

Chrome:

Las peticiones son de tipo GET.

-El documento.

![img11](/images/11.png "imagen11")

-El recurso de la imagen.

![img12](/images/12.png "imagen12")

Firefox:
Igualmente, son peticiones de tipo GET como se veía en la parte de la pestaña
de “Red” junto a los códigos de respuesta.

NOTA: Las peticiones con ambos navegadores se les ha pasado el argumento ‘limit=5’

• Qué código de estatus devuelve.

Como habíamos dicho → Chrome: 200: XML
200: Imagen cacheada

Firefox: 200: XML
404: Imagen no encontrada

• Qué DNS tiene el servidor

El servidor DNS ha “convertido” (asociado) la IP del la página web a la siguiente
URL en ambos navegadores:

Chrome: www3.gobiernodecanarias.org
Firefox: www3.gobiernodecanarias.org

![img13](/images/13.png "imagen13")

-

![img14](/images/14.png "imagen14")

• Qué IP tiene tiene el servidor:

Chrome: 93.188.137.126:443
Firefox: 93.188.137.126:443

![img15](/images/15.png "imagen15")

• ¿La página tiene alguna cookie?, ¿Cuáles?

No se encontraron cookies de ningún tipo con ambos navegadores.

![img16](/images/16.png "imagen16")

-

![img17](/images/17.png "imagen17")

• ¿Qué idioma acepta?

NOTA: No presenta los mismos lenguajes en cada navegador

Chrome: es-ES
Firefox: en-US

![img18](/images/18.png "imagen18")

-

![img19](/images/19.png "imagen19")

Por otra parte, la respuesta que devuelve, es decir el XML que se nos presenta,
contiene múltiples referencias tanto al lenguaje español (es) como al inglés (en) en ambos
navegadores en el código.

![img20](/images/20.png "imagen20")

• Alguna línea de código JavaScript

No hay ninguna línea de Javascript ni líneas que contengan el código para cargar un
fichero javascript alguno.

• Alguna línea de código CSS que se aplique

Como es un fichero XML no hay ninguna hoja de estilo que se aplique sobre el
fichero.

• Alguna línea de código HTML que se aplique.

No hay código HTML sólo enlaces que apunten a otras páginas que puede que
tengan ellas en su interior código de ese tipo.
