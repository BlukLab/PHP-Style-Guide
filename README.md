# <a name='php-style-guide'>PHP Style Guide</a>
El siguiente contenido describe la codificación para la contribución al desarrollo de Codeigniter. No hay ning´ñin requisito para utilizar estos estilos en su propia aplicación utilizando Codeigniter, aunque se recomiendan.

## <a name='TOC'>Tabla de Contenido</a>

* [PHP Stytle Guide](#php-style-guide)
  * [Formato de Archivo]
    * [TextMate]
    * [BBEdit]
  * [Etiqueta de cierre PHP](#etiqueta-cierre-php)
  * [Nombres de archivos](#nombres-de-archivos)


## <a name='etiqueta-cierre-php'>Etiqueta de cierre PHP</a>
La etiqueta de cierre PHP `?>` en un documento PHP es opcional para el intérprete PHP. Sin embargo, si se utiliza, cualquier espacio en blanco después de la etiqueta de cierre, ya sea presentada por el desarrollador, usuario o una aplicación FTP, puede causar una salida no deseada, errores PHP, o si estos último son suprimidos, páginas en blanco. Por esta razón todos los archivos PHP deben OMITIR la etiqueta de cierre PHP y terminar con una sola línea vacía en su lugar.

## <a name="nombres-de-archivos">Nombres de archivos</a>
Los archivos que son clases, deben ser nombrados de una manera similar a *Ucfirst*, mientras que cualquier otro nombre de archivo (configuraciones, vistas, secuencias de comandos genénericos, etc.) deben estar en mayúsculas.
