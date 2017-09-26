# Ejercicio 1
* Con un sistema centralizado, el peso aproximado sería 1.5 MB (0.5 MB + 5 MB + 1 MB - 5 MB), ya que se descargaría solamente el repositorio tal cual está en su cuarta versión.
* Con un sistema distribuido, el peso aproximado sería 6.5 MB (0.5 MB + 5 MB + 1 MB + 0 MB), ya que se descargan las 4 versiones pero aquellos archivos que no se modifican en una versión se representan mediante punteros.

# Ejercicio 3
* El branch que existe por default en todo repositorio Git se llama master.
* El identificador de cada commit se genera tomando el identificador del árbol "base" del commit, el identificador del commit padre, la información del autor y del committer (no son exactamente iguales) y el mensaje del commit. A todo esto se le anexa un header que consiste en la palabra "commit" y la longitud (en bytes) de toda la información anterior. A todo esto se le aplica SHA1, y el resultado es el identificador (40 bytes).
* Un tag se utiliza para marcar un punto particular del desarrollo (ej. la finalización de una versión nueva), mientras que un branch se utiliza para comenzar un hilo separado de desarrollo concurrente con otros desarrollos (ej. una nueva funcionalidad). Cada uno se guarda en lugares distintos (los tags en refs/tags y los branches en refs/heads) y, mientras que el branch solamente puede apuntar a un commit, el tag puede apuntar a un commit o a otro tag.

# Ejercicio 4
Supondremos que estamos trabajando sobre un archivo llamado archivo.txt ubicado en la carpeta raíz del repositorio y con un commit identificado como abcdef.
* Para sacar el archivo del área de staging, ejecutamos _git reset HEAD -- archivo.txt_
* Para revertir los cambios realizados en el commit en ese archivo (más allá de si el commit modifica o no otros archivos), ejecutamos _git checkout abcdef -- archivo.txt_
* Para volver al estado de cierto commit, ejecutamos _git checkout abcdef_
