# Ejercicio Práctico N° 1

Se necesita realizar un script que permita mediante un menú realizar distintas operaciones sobre un sistema Linux o MacOS.

Este script utilizará un parámetro optativo y una variable de ambiente llamada `FILENAME` para guardar el nombre de un archivo.

### Opciones
1. **Crear entorno**: Consiste en la creación de un directorio dentro del `home` que se llame `EPNro1`, dentro de este directorio deberán existir dos carpetas, una llamada `entrada`, otra `salida` y una última `procesado`.
2. **Correr proceso**: Se debe correr un proceso en background que ejecute un script llamado `consolidar.sh` que se encuentra en el directorio `EPNro1`, este script debe tomar cada archivo que ingresa en la carpeta `entrada` y adjuntar toda su información al final del archivo `FILENAME.txt` (donde `FILENAME.txt` es una variable de entorno, previamente definida) que se encuentra en la carpeta `salida`. Luego de esa operación el archivo original se debe mover a la carpeta “procesado”.
3. Si existe el archivo `FILENAME.txt` en la carpeta `salida`, mostrar por pantalla el listado de alumnos ordenados por *número de padrón*.
4. Si existe el archivo `FILENAME.txt` en la carpeta salida, mostrar por pantalla las *10 notas más altas del listado*.
5. Solicitar al usuario un *número de padrón*, y mostrar por pantalla, los datos del mismo provenientes del archivo `FILENAME.txt` de la carpeta `salida`.
6. Salir.

Parámetro optativo `-d`: Si el usuario corre el script con el parámetro optativo `-d` se borrará todo el entorno creado en la carpeta `EPNro1` y se matarán los procesos creados en background.

### Hipótesis
- Los archivos que ingresan a la carpeta entrada pueden tener cualquier nombre, pero su extensión debe ser `.txt`.
- El formato de los archivos de entrada deben respetar las siguientes columnas: `(Nro_Padrón, Nombre y apellido, email, nota)`. No es necesario validarlo, se considera que están correctos.
- Los padrones son únicos y los registros no están repetidos.
- Se utilizará Bash shell.

En **test.txt** hay nombres para copiar y pegar en archivos dentro de `/entrada`
