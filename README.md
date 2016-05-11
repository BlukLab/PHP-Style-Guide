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
function fileproperties()               // not descriptive and needs underscore separator
function fileProperties()               // not descriptive and uses CamelCase
function getfileproperties()            // Better!  But still missing underscore separator
function getFileProperties()            // uses CamelCase
function get_the_file_properties_from_the_file()        // wordy
```

#### CORRECTO:
```php
function get_file_properties()  // descriptive, underscore separator, and all lowercase letters
```
