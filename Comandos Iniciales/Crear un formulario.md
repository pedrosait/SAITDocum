# Crear un formulario personalizado de Sait desde la ventana de comando en FoxPro
### 29 de Octubre del 2022
#### Hugo Sicairos Molina

Primero, debemos saber en donde estamos posicionados, para detectar donde se ubicaran nuestros archivos creados
Para ello, escribimos en la ventana de comandos, la palabra ``` cd ```

Si deseamos movernos de ruta, utilizamos la palabra ``` cd + la ruta deseada ```
```vfp
cd C:\\ejercicios
```

#### Nota: Movernos a una ruta deseada, nos permite tener una mejor organización de nuestros archivos al momento de crearlos

Para la creación de formularios de Sait, debemos utilizar las librerias encontradas en la carpeta * Msllib60 *, ya que está personaliza los formularios con el logo de la empresa

Para crear un catalogo, utilizamos la libreria * catmsl * que se encuentra en la carpeta mencionada anteriormente

Entonces, para crearlo, nos dirigimos en a la ventana de comandos y utilizamos
``` create form + el nombre del archivo + as catmsl from + la ruta donde se encuentra la libreria catmsl ```

```vfp
create form catalogoEmpresa as catmsl from c:\\msllib60\catmsl.vcx
```

Con esto, se nos creara un formulario con el logo de la empresa, un grid, un page y los botones para agregar, modificar, eliminar, etc.