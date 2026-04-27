# Tarea para evaluar y practicar habilidades de GNU/Linux y R 

## Instrucciones Generales

A continuación encontrarás la descripción de las actividades en las que practicarás lo visto en clase hasta el momento. Sin embargo, en gran medida también deberás investigar y probar distintas soluciones por tu cuenta. 

La parte más importante a evaluar **NO** será que todas las actividades se resuelvan correctamente. En cambio, lo más relevante para la calificación consiste en **documentar y comentar tus esfuerzos por resolver las tareas**. Esto quiere decir que, aunque no logres obtener el resultado exacto que se te solicita, cada apartado puede obtener una alta calificación en función de que reportes el haber intentado resolverla y los abordajes que utilizaste.

¿Cómo se evaluará? 

| Contenido del informe | Valor |
| :--- | :--- |
| Documentar (notas, comandos, comentarios, capturas de pantalla) | 6/10 |
| Comentario sobre lo aprendido y autocrítica | 3/10 |
| Resultado de la tarea | 1/10 |

La calificación final será el promedio de calificaciones del las tres actividades.

El próximo jueves 30 de abril, desde las 11:00 am y hasta las 1:00 pm, estaré resolviendo dudas en una sesión por Google Meet. 

## Tareas 

### A) Ejercicios con Bedtools

Para esta sección necesitarás entrar en tu máquina virtual de Linux e instalar `bedtools`, el cual está disponible a través de `apt`.

También tienes que obtener los datos que usaremos para el ejercicio. Descárgalos usando `wget` a partir de los siguientes enlaces: 

* [https://raw.githubusercontent.com/cperalta22/rconcolab/refs/heads/master/datosTarea2/promotores_shuffled.bed](https://raw.githubusercontent.com/cperalta22/rconcolab/refs/heads/master/datosTarea2/promotores_shuffled.bed)
* [https://raw.githubusercontent.com/cperalta22/rconcolab/refs/heads/master/datosTarea2/regiones.bed](https://raw.githubusercontent.com/cperalta22/rconcolab/refs/heads/master/datosTarea2/regiones.bed)

Los archivos que descargaste son archivos `.bed` de coordenadas genómicas con columnas separadas por tabuladores. Cada renglón contiene un identificador de cromosoma, seguido del inicio de la coordenada y el final de la misma. 

El archivo `regiones.bed` contiene una cuarta columna con un identificador para cada coordenada, mientras que el archivo `promotores_shuffled.bed` contiene también una columna de identificadores y algunas columnas adicionales que no son relevantes para el ejercicio actual. 

#### Descripción de la tarea y sus objetivos

Has realizado un experimento que te ha arrojado como resultado un conjunto de coordenadas genómicas de interés biológico (`regiones.bed`).

Tu objetivo es conocer **cuántas** de dichas regiones coinciden con promotores de genes (`promotores_shuffled.bed`). También quieres conservar en un archivo `.bed` las regiones de interés que sobrelaparon con un promotor.

Finalmente, en otro archivo deberás conservar **los promotores** que coincidieron con **las regiones de interés**. Dicho archivo **debe incluir el dato de cuántas veces coincidieron los promotores con las regiones de interés**.

Para llevar a cabo la tarea utilizarás Bedtools, que es un conjunto de herramientas diseñadas para trabajar específicamente con archivos `.bed`. Además, **será necesario** que utilices comandos de manipulación de texto que hemos explorado en clase. 

Te recomiendo que revises específicamente la documentación de `bedtools intersect` y `bedtools sort`, así como que repases tus notas sobre `sed`:

* [https://bedtools.readthedocs.io/en/latest/content/tools/intersect.html](https://bedtools.readthedocs.io/en/latest/content/tools/intersect.html)
* [https://bedtools.readthedocs.io/en/latest/content/tools/sort.html](https://bedtools.readthedocs.io/en/latest/content/tools/sort.html)

#### ADVERTENCIA

Los archivos `.bed` proporcionados **NO van a funcionar** directamente para llevar a cabo la tarea.

Para que puedas usar los archivos deberás:

1. Visualizar los archivos (usando `cat`, `batcat -l tsv`, `less`, `nano`, etc.) y compararlos 'manualmente'.
2. Intentar ejecutar las acciones requeridas y estar sumamente al pendiente de los **fallos y mensajes de error** que devuelva la terminal.
3. Tomar las acciones correctivas necesarias, lo cual puede incluir la modificación o creación de archivos nuevos o intermedios para ir solucionando los errores de formato.

#### Reporte

* Crea una carpeta en tu máquina virtual que se llame `tareaBedtools`; en ella dejarás todos los archivos que generes.
* Toma capturas de pantalla y úsalas para escribir un reporte en formato libre sobre tu proceso. Recuerda incluir los aspectos mencionados en la tabla de evaluación.
* Guárdalo como `.pdf` y envíalo en Classroom en la sección que se habilitará para ello.

### B) Ejercicio con Tidyverse. 

#### Descripción de la tarea y sus objetivos

Utiliza el notebook de Jupyter `datosTabulares.ipynb` del repositorio de github de la clase ( https://github.com/cperalta22/rconcolab ) y lleva a cabo el ejercicio final. 

Si no recuerdas como se cargan o dónde están los datos que se utilizan, las instrucciones están al inicio del mismo notebook.

#### Reporte

guarda el notebook con tu solución dando click en Archivo > Descargar > Descargar .ipynb 

**renombra el notebook para incluir tu apellido**

súbe tu notebook en la sección del Classroom que habilitaré para ello.

### C) Ejercicio de lógica de programación. 

#### Descripción de la tarea, obejtivos y modo de reportar

En el repo de la clase puedes abrir el notebook de este ejercicio:

https://github.com/cperalta22/rconcolab/blob/master/ejercicioPromotores.ipynb 

Sigue las instrucciones y al igual que el ejercicio anterior, guarda el notebook completado y súbelo a Classroom
