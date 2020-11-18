# <h1 align=center><img src=https://raw.githubusercontent.com/systemnaut/Pinjection/master/isologotipo/pinjector-iso-1-alpha.png width=50> PInjector</h1>
![PInjector isologotype](isologotipo/pinjector-isologo-1.png)

## ¿Qué es?
PInjection es un script de Python que puede funcionar como Módulo o como script ejecutable desde la línea de comandos (CLI script). Este script lo que hace es inyectar Código Objeto en una región de memoria específica de un proceso utilizando la API de Windows ([OpenProcess](https://docs.microsoft.com/en-us/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [VirtuallAllocEx](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [WriteProcessMemory](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) y [ReadProcessMemory](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)).

## ¿Qué NO es?
-----------------
 - PInjection **NO** es un script ejecutable para meter tu virus ejecutarlo y romperle la computadora a tu amigue.
 - PInjection **NO** es un script ejecutable para guardar funciones en una región de memoria específica.
 
### ¡Que SÍ es!
-----------------
 - PInjection **SI** es un script ejecutable para meter Código Objeto específico en una región de memoria específica.
 - PInjection **SI** es un módulo que provee una interfaz sencilla de utilizar para cualquier novato en Python.
 - PInjection **SI** es una buena elección para ofuscar y ocultar código objeto en un proceso (Similar a [DLL Injection](https://en.wikipedia.org/wiki/DLL_injection))
 - PInjection **SI** es un software libre y gratuito. *(GNU GPLv3)*
 
### Limitaciones
-----------------
Como ya dije, esto no es un script para ejecutar y automáticamente vas a destruír permanentemente la computadora destino, sino un script/módulo para cargar código objeto en la memoria de un proceso, esto quiere decir explicitamente lo dícho, para ejecutar el código objeto que se guarda, se tiene que conocer qué es, ya que luego se tendrá que pasar a FunctionType utilizando la librería [types](https://docs.python.org/3/library/types.html), y ahí se tendrán que definír todas las constantes utilizadas en el código objeto. **_La carga del código objeto es automática, la ejecución NO_**
#### Notas 0.2

 - Borrado Shell, test_function y test_injection.
 - Modificado para ser utilizado como un script o desde la línea de comandos.
 - Probado en Python 3.7.9 utilizando Windows 10 Home.
 - Actualmente solo puede alojar memoria e imprimir (o asignar a una variable) la dirección base de memoria alojada, **NO ES RECOMENDABLE** ejecutar este script muchas veces, ya que este script genera [memory leaks](https://en.wikipedia.org/wiki/Memory_leak).

#### DISCLAIMER Y AVISOS LEGALES.
 - Todos los contenidos multimedia estan licenciados bajo la licencia [Creative Commons BY-SA](https://creativecommons.org/licenses/by-sa/3.0/deed.es)
 - Todos mal uso que se le de a este software, queda estricta y absolutamente absuelto de *mea culpa* y/o responsabilidad sobre los daños y perjuicios generados a través del uso de este software, al utilizar este software estas accediendo a tomar cualquier tipo de responsabilidad sobre lo que el software pueda generar al ser utilizado.
