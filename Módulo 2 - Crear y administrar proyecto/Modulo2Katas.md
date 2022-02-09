# Ejercicio - Crear un paquete
En este ejercicio, aprenderás a utilizar entornos virtuales como una forma para no afectar a los paquetes instalados globalmente u otros programas que se ejecutan en tu máquina.

*Para este ejercicio es necesario que lo ejecutes desde la terminal, línea de comandos, cmd, consola, cli, etc. de tu computadora.*

## Crear un entorno virtual
Crea un entorno virtual mediante ``venv``
* Ejecutar en su terminal: ``python -m venv env``

![image](https://github.com/DanielaBeltranCruz/Curso-Introductorio-Python/blob/e484496e1831a6edd395f99deae5353070a6dead/M%C3%B3dulo%202%20-%20Crear%20y%20administrar%20proyecto/image_02.JPG)

    Ahora tienes un directorio (folder) ``env`` creado en tu terminal.

* Ejecuta el comando para activar el entorno virtual: ``source env/bin/activate``

    ```
    env\Scripts\activate
    ```
Ahora ves en tu terminal ``(env)``. Eso significa que has activado tu entorno virtual y se ha aislado del resto de tu máquina.

![image](https://github.com/DanielaBeltranCruz/Curso-Introductorio-Python/blob/e484496e1831a6edd395f99deae5353070a6dead/M%C3%B3dulo%202%20-%20Crear%20y%20administrar%20proyecto/image_03.JPG)

## Instalar una biblioteca

Ahora que estás dentro de tu entorno virtual, puedes instalar una biblioteca y saber que la biblioteca solo existirá en el entorno virtual.

* Ejecuta el comando ``pip freeze`` para ver las bibliotecas instaladas en tu entorno:

    ```
    pip freeze
    ```
    ![image](https://github.com/DanielaBeltranCruz/Curso-Introductorio-Python/blob/e484496e1831a6edd395f99deae5353070a6dead/M%C3%B3dulo%202%20-%20Crear%20y%20administrar%20proyecto/image_04.JPG)

    No deberías obtener respuesta. A continuación, veamos cómo cambia la salida de ``pip freeze`` cuando se agrega una biblioteca (un paquete).

* Ejecuta el comando ``pip install`` para instalar una biblioteca:
   ```
   pip install python-dateutil
   ```
* Un gran mensaje de salida de texto dice que está instalando tu biblioteca, y debe terminar con la siguiente oración:

    ```
    Successfully installed python-dateutil-2.8.2 six-1.16.0
    ```
    ![image](https://github.com/DanielaBeltranCruz/Curso-Introductorio-Python/blob/e484496e1831a6edd395f99deae5353070a6dead/M%C3%B3dulo%202%20-%20Crear%20y%20administrar%20proyecto/image_05.JPG)

* Vuelve a ejecutar ```pip freeze``` para ver cómo ha cambiado tu lista de bibliotecas:
    ```
    pip freeze
    ```
* Ahora deberías ver la siguiente lista:
    ```
    python-dateutil==2.8.2
    six==1.16.0
    ```
    ![image](https://github.com/DanielaBeltranCruz/Curso-Introductorio-Python/blob/e484496e1831a6edd395f99deae5353070a6dead/M%C3%B3dulo%202%20-%20Crear%20y%20administrar%20proyecto/image_06.JPG)

### Desactivar un entorno virtual

Hasta ahora, has creado un entorno virtual y le has agregado un paquete. Sin embargo, es posible que estés trabajando en varios proyectos de Python y necesites cambiar entre ellos. Para hacer eso, debes salir (desactivar) tu entorno virtual.

Ejecuta el comando ``deactivate``:
```
deactivate
```
![image](https://github.com/DanielaBeltranCruz/Curso-Introductorio-Python/blob/e484496e1831a6edd395f99deae5353070a6dead/M%C3%B3dulo%202%20-%20Crear%20y%20administrar%20proyecto/image_07.JPG)

Observa cómo cambia el mensaje de tu terminal ``(env)`` a cómo se veía antes.
