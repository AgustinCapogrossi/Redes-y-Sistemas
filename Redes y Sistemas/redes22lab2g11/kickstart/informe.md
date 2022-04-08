# Informe Laboratorio 02

## Redes y sistemas distribuidos 2022

> Alvaro Ariel, Capogrossi Agustín, Martinez Lisandro

### Distribución

```md
redes22lab2g11
    ╚═ /kickstart
        ╠═ /__pycache__
        ║   ╠═ connection.cpython-38.pyc
        ║   ╚═ constants.cpython-38.pyc
        ╠═ /files
        ║   ╠═ agus
        ║   ╠═ lichi
        ║   ╚═ ariel
        ╠═ client.py
        ╠═ connection.py
        ╠═ constants.py
        ╠═ server-test.py
        ╠═ server.py
        ╚═ informe.md
```

### Organización

Utilizamos metodologías agile, en particular scrum, para la distribución de tareas.
Luego de leer detenidamente los requerimientos y condiciones para el laboratorio los transformamos en tareas y creamos un tablero en Jira para realizar un seguimiento del progreso. En este tablero establecimos criterios de aceptación para cada tarea así como tambien un puntaje basado en la dificultad especulada de la misma. Una vez realizado esto distribuimos las tareas de forma pareja.

La forma de subir el código al repositorio de bitbucket está distribuida en ramas siguiendo el siguiente esquema:

```md
Agustín  ➙ informe  ↘

Lisandro ➙ Clase  ➙  Main  ➙  Master

Ariel    ➙ Conexión ↗
```

En donde cada uno trabaja en una rama individual para completar cada tarea y el código funcional se combina en Main. El producto terminado es luego movido de Main a Master.

### Progreso

Tuvimos dificultades a la hora de entender la organización y funcionalidad de cada parte del código. Debimos leer extensivamente el código del primer laboratorio para poder entender como empezar. Originalmente no entendimos la distribución de las funciones y clases, puesto que no veiamos una clara diferencia entre la clase Connection y la clase Server por lo que realizamos la gran mayoría del trabajo en la clase server.

Para probar algunas de las funciones nos conectamos mediante el uso de la consola usando la función:

```bash
telnet 0.0.0.0 19500
```

En la que 0.0.0.0 es la dirección reservada y 19500 el puerto reservado.

Para la inicializacion de variables en la clase Connection se presentaron algunos problemas a la hora de trabajar con el directorio, puesto que originalmente nos parecía un concepto vago no sabíamos como inicializarla. Poco tiempo después entendimos la funcionalidad del servidor y referenciamos al directorio desde el principio.

Finalmente entendimos cual era la funcionalidad de cada uno por lo que lo transladamos y modularizamos como correspondía.

A mitad del trabajo redistribuímos algunas de las tareas asignadas originalmente para alcanzar un entendimiento mayor del laboratorio.

### Bibliografía

➤ [StackOverflow](https://es.stackoverflow.com/)
➤ [GeeksForGeeks](https://www.geeksforgeeks.org/)
