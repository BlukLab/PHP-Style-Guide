# <a name='php-style-guide'>PHP Style Guide</a>
El siguiente contenido describe la codificación para la contribución al desarrollo de Codeigniter. No hay ning´ñin requisito para utilizar estos estilos en su propia aplicación utilizando Codeigniter, aunque se recomiendan.

## <a name='TOC'>Tabla de Contenido</a>

* [PHP Stytle Guide](#php-style-guide)
  * [Formato de Archivo](#formato-de-archivos)
    * [TextMate](#texmate)
    * [BBEdit](#bbedit)
  * [Etiqueta de cierre PHP](#etiqueta-cierre-php)
  * [Nombre de archivos](#nombre-de-archivos)
  * [Nombre de clases y métodos](#nombre-de-clases-metodos)
  * [Nombre de variables](#nombre-de-variables)
  * [Comentarios](#comentarios)
  * [Constantes](#constantes)

## <a name='formato-de-archivos'>Formato de Archivo</a>
Los archivos deben ser guardados con codificación Unicode (UTF-8). BOM *no* debe ser utilizado. A diferencia de UTF-16 y UTF-32, no hay ningín orden de bytes para indicar en un archivo codificado en UTF-8. BOM puede tener un efecto negativo en el envío de la salida PHP, evitando a la aplicación la posibilidad de establecer sus propias cabeceras. Los fin de línea UNIX deben utilizarse (LF).

### <a name='texmate'>TextMate</a>

### <a name='bbedit'>BBEdit</a>

## <a name='etiqueta-cierre-php'>Etiqueta de cierre PHP</a>
La etiqueta de cierre PHP `?>` en un documento PHP es opcional para el intérprete PHP. Sin embargo, si se utiliza, cualquier espacio en blanco después de la etiqueta de cierre, ya sea presentada por el desarrollador, usuario o una aplicación FTP, puede causar una salida no deseada, errores PHP, o si estos último son suprimidos, páginas en blanco. Por esta razón todos los archivos PHP deben OMITIR la etiqueta de cierre PHP y terminar con una sola línea vacía en su lugar.

## <a name="nombre-de-archivos">Nombre de archivos</a>
Los archivos que son clases, deben ser nombrados de una manera similar a *Ucfirst*, mientras que cualquier otro nombre de archivo (configuraciones, vistas, secuencias de comandos genénericos, etc.) deben estar en mayúsculas.

#### INCORRECTO:

```php
somelibrary.php
someLibrary.php
SOMELIBRARY.php
Some_Library.php

Application_config.php
Application_Config.php
applicationConfig.php
```

#### CORRECTO:
```php
Somelibrary.php
Some_library.php

applicationconfig.php
application_config.php
```

Por otra parte los nombres de los archivos de las clases deben coincidir con el nombre de la clase en sí, Por ejemplo, si tiene una clase llamada *MiClase*, entonces el nombre del archivo debe ser **Myclass.php**.

## <a name="#nombre-de-clases-metodos">Nombre de clases y métodos</a>

Los nombres de clase siempre deben comenzar con una letra mayúscula. Cuando son varias palabras deben estar separadas por underscore (guión bajo) y no en estilo *CamelCase*.

#### INCORRECTO:
```php
class superclass
class SuperClass
```

#### CORRECTO:
```php
class Super_class
```

```php
class Super_class {

    public function __construct()
    {

    }
}
```

Los métodos de las clases deben ser completamente en minúsculas y se nombran para indicar claramente su función, que incluye preferentemente un verbo. Trate de evitar los nombres excesivamente largo y detallados. Las palabras deben estar separadas por un guión bajo (underscore).

#### INCORRECTO:
```php
function fileproperties()               // no es descriptiva y es necesario seperar con guión bajo (underscore)
function fileProperties()               // no es descriptiva y utiliza CamelCase
function getfileproperties()            // Mejor!  Pero todavía falta separa con guión bajo
function getFileProperties()            // utiliza CamelCase
function get_the_file_properties_from_the_file()        // Muchas palabras
```

#### CORRECTO:
```php
function get_file_properties()  // descriptiva, separada con guión bajo, y todas las letras en minúscula
```
## <a name="#nombre-de-variables">Nombre de variables</a>

La guía para nombrar varaibles son muy similares a los utilizados para los métodos. Las variables deben contener sólo letras minúsculas, usando guión bajo (underscore) como separador, y deben ser nombres razonables que indiquen su propósito y contenido. Las variables muy cortas que no son palabras solo deben utilizarse en iteradores como en los bucles `for()`.

#### INCORRECTO:

```php
$j = 'foo';             // variables de una sola letra solo debe utilizarse en bucles for()
$Str                    // contiene letras mayúsculas
$bufferedText           // utiliza CamelCase, y podría acortarse sin perder significado semántico
$groupid                // varias palabras, necesitan seperarse con guión bajo
$name_of_last_city_used // demasiado largo
```
#### CORRECTO:

```php
for ($j = 0; $j < 10; $j++)
$str
$buffer
$group_id
$last_city
```

## <a name="#comentarios">Comentarios</a>

En general, el código debe ser comentado prolíficamente. No sólo ayuda a describir el flujo y la intención del código para los programadores menos experimentados, pero puede resultar muy valioso volver a la línea de su propio código de hace meses. No hay un formato requerido par los comentarios, pero se recomieda lo siguiente:

Estilo DocBlock, antes de la declaración de clases, métodos y propiedades, para que puedar ser captados por los IDEs.

```php
/**
 * Super Class
 *
 * @package     Package Name
 * @subpackage  Subpackage
 * @category    Category
 * @author      Author Name
 * @link        http://example.com
 */
class Super_class {
```

```php
/**
 * Encodes string for use in XML
 *
 * @param       string  $str    Input string
 * @return      string
 */
function xml_encode($str)
```

```php
/**
 * Data for class manipulation
 *
 * @var array
 */
public $data = array();
```

En los comentarios de una sola línea, deje una línea en blanco entre grandes bloques de comentarios

```php
//Divide la cadena en saltos de línea
$parts = explode("\n", $str);

//Un comentario más largo que necesita para dar más detalles sobre lo que está
//ocurriendo y por qué pueden utilizar varios comentarios de una sola línea. Trate
//de mantener la anchura razonable, alrededor de 70 caracteres es el más fácil de
//leer. No dude en vincular a los recursos externos permanentes que puedan
//proporcionar mayor detalle:
//
// http://example.com/information_about_something/in_particular/

$parts = $this->foo($parts);
```

## <a name="#constantes">Constantes</a>

Las constantes siguemn el mismo patrón que las variablesm, con la condición de que las constantes deben ser siempre completamente en mayúsculas. *Siempre prefiera utilizar las contantes de Codeigniter cuando sea apropiado, es decir, SLASH, LD, RD, PATH_CACHE, etc.*

#### INCORRECTO:

```php
myConstant      // falta separar con guión bajo y estar completamente en mayúsculas
N               // no constantes de una sola letra
S_C_VER         // no descriptiva
$str = str_replace('{foo}', 'bar', $str);       // debe utilizar constantes LD y RD
```

#### CORRECTO:

```php
MY_CONSTANT
NEWLINE
SUPER_CLASS_VERSION
$str = str_replace(LD.'foo'.RD, 'bar', $str);
```
