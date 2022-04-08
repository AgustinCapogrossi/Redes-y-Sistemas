## Informe Laboratorio 01

### Redes y sistemas distribuidos 2022

> Alvaro Ariel, Capogrossi Agustín, Martinez Lisandro

#### Punto estrella

>Que mecanismos permiten funcionar a nombres de dominio como:
>
>- <http://中文.tw/>
>- <https://💩.la>

Aqui estamos en presencia de **"Nombres de dominios Internacionalizados"**, a grandes rasgos este contiene al menos una etiqueta que se muestra en las aplicaciones de software, en su totalidad o en parte, en una escritura o alfabeto no latino, como árabe, chino, cirílico, devanagari, caracteres basados ​​en el alfabeto griego, hebreo o latino con signos diacríticos o ligaduras, como el francés. Estos sistemas de escritura están codificados por computadoras en Unicode multibyte. **Los nombres de dominio internacionalizados se almacenan en el Sistema de nombres de dominio (DNS) como cadenas ASCII utilizando la transcripción Punycode**,el cual es un codificador especial usado para convertir caracteres Unicode a ASCII. Antes de esto se aplica **NAMEPREP** el cual es el proceso de conversión de mayúsculas y minúsculas en una cadena y la eliminación de algunos puntos de código generalmente invisibles antes de que sea adecuado para representar un nombre de dominio u otro nombre canónico similar.

##### Datos extra sobre la investigación

Visitar las páginas fue de gran ayuda, sobre todo <http://中文.tw/> en la cual encontramos todo lo necesario para entender acerca de los Nombres de dominios Internacionalizados, y que nos será de mucha ayuda para cuando necesitemos registrar nuestro nombre de dominio chino. Respecto a https://     al visitarla podiamos observar que el dominio cambiaba a <https://xn--ls8h.la/>, el cual es el equivalente en Punycode confirmando asi la veracidad sobre el mecanismo usado. Dentro de este dominio en particular podemos observar que además de tener la representación en Punycode para 💩, esta viene acompañada de xn-- el cual es el prefijo utilizado en la representación ASCII de un nombre de dominio internacionalizado.

Ademas de este mecanismo encontramos otras maneras de permitir el acceso a estos sitios, y es similar al formato que usamos en el código de la catedra. Se trata del formato **URL encoding** el cual convierte caracteres a un formato que puede ser transmitido a través de internet, **las URLs solo pueden ser enviadas a traves de internet usasndo el conjunto de caracteres ASCII** y dado que estas suelen tener caracteres fuera de este conjunto, URL debe convertilo a un formato valido:

- La codificación URL reemplaza los caracteres ASCII no seguros con un % seguido de 2 digitos hexadecimales, ASCII como un ejemplo porque tambien funciona para UTF-8 entre otros (este estandar es el que se usa al hacer la peticion en python, lo aplica con el metodo encode)
- Las URL no pueden contener espacios por lo que la codificación URL los reemplaza con %20 o un signo +.
