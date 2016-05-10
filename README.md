# <a name='php-style-guide'>PHP Style Guide</a>
El siguiente contenido describe la codificación para la contribución al desarrollo de Codeigniter. No hay ning´ñin requisito para utilizar estos estilos en su propia aplicación utilizando Codeigniter, aunque se recomiendan.

## <a name='TOC'>Tabla de Contenido</a>

* [PHP Stytle Guide](#php-style-guide)
  * [Formato de Archivo](#formato-de-archivos)
    * [TextMate](#texmate)
    * [BBEdit](#bbedit)
  * [Etiqueta de cierre PHP](#etiqueta-cierre-php)
  * [Nombres de archivos](#nombres-de-archivos)

## <a name='formato-de-archivos'>Formato de Archivo</a>
Los archivos deben ser guardados con codificación Unicode (UTF-8). BOM *no* debe ser utilizado. A diferencia de UTF-16 y UTF-32, no hay ningín orden de bytes para indicar en un archivo codificado en UTF-8. BOM puede tener un efecto negativo en el envío de la salida PHP, evitando a la aplicación la posibilidad de establecer sus propias cabeceras. Los fin de línea UNIX deben utilizarse (LF).

### <a name='texmate'>TextMate</a>

### <a name='bbedit'>BBEdit</a>

## <a name='etiqueta-cierre-php'>Etiqueta de cierre PHP</a>
La etiqueta de cierre PHP `?>` en un documento PHP es opcional para el intérprete PHP. Sin embargo, si se utiliza, cualquier espacio en blanco después de la etiqueta de cierre, ya sea presentada por el desarrollador, usuario o una aplicación FTP, puede causar una salida no deseada, errores PHP, o si estos último son suprimidos, páginas en blanco. Por esta razón todos los archivos PHP deben OMITIR la etiqueta de cierre PHP y terminar con una sola línea vacía en su lugar.

## <a name="nombres-de-archivos">Nombres de archivos</a>
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
