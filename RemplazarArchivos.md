# Como Remplazar archivos desde FoxPro
### 29 de Octubre del 2022
#### Hugo Sicairos Molina

En FoxPro, hay una manera facil de remplazar archivos desde el archivo con el que se está trabajando, hacía la ruta a la cual se hara la prueba de dicha ventana

Debemos saber en donde estamos posicionados, para identificar en que carpeta estamos, escribimos ```cd ```
Si deseamos movernos a otro lugar, debemos seleccionar toda la ruta
```vfp
cd C:\\ejercicios
```

Para ello, en la ventana de comando escribimos ``` modi comm + el nombre que deseemos dar a ese archivo de comandos ```
```vfp
modi comm make
```
Se creara una nueva ventana de comando con extensión .prg, la cual se guardara en la ruta donde estemos posicionados actualmente

En ella escribiremos varias lineas
``` set safety off ``` permite que Foxpro no muestre un cuadro de dialogo preguntando si deseamos sobreescribir los archivos

``` copy file + la ruta del archivo con el que se esta trabajando ```

``` to + la ruta hacía donde se pegaran los archivos ```

```vfp
set safety off

copy file C:\\ejercicios\catLinea.* to C:\\sait\empresa\catLinea.*
```

Damos ``` Ctrl + W ``` para guardar

Debemos de compilar el archivo, para ello utilizamos el comando ``` compile + el nombre del archivo de comandos ```
```vfp
compile make
```

Para finalizar, utilizamos el comando ``` do  + el nombre del archivo. ```
Para aplicar el archivo de comandos.
```vfp
do make
```
Con esto, los archivos serán reemplazados dentro del sistema y se podrán visualizar los nuevos
### Notas:
#### 1. El sistema no mostrara ningún mensaje de que se realizaron los cambios, ya qué se utiliza la linea "safety off" 
#### 2. Es necesario, que las ventanas que serán remplazadas estén cerradas, tanto en SAIT como en FoxPro, si no, se generara un error