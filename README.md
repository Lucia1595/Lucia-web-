# Repositorio de trabajo del módulo de Periodismo de Datos II


#### Actividades dirigidas 


[Actividad dirigida 1](ad1.md)


[Actividad dirigida 2](ad2.md)


[Actividad dirigida 3](ad3.md)


[Actividad dirigida 4](ad4.md)


# ¿Qué prendimos durante la duración de esta materia?

La primera actividad comenzamos a investigar sobre alguna visualización que nos agradará y conocimos sobre Markdown. Utilizamos la sintaxis básica que nos presentan en la página de Markdown para la redacción y nos ayudó para realizar todas las demás asignaciones. Esto era totalmente nuevo para mí. 

**Entre los códigos más usados**

- El más fácil de todos, era el encabezado, se agregaba el signo numeral (#) delante de una palabra o frase. La cantidad de numeral así mismo iba cambiando el tamaño del texto. 
**Ejemplo**: un numeral se creaba, Título. dos numerales se creaba un Subtítulo y así sucesivamente.
 
- Para escribir alguna palabra se emplea * y si se quiere enfatizar agregamos dos asteriscos sin espacios alrededor de las letras. **letra** 
- Mientras que para cursiva se coloca tres asteriscos. 
- Para generar un enlace se encierra el texto del enlace entre corchetes y luego la URL entre paréntesis. Esta fue una de las formas que más lo utilice. 

## Por otra parte, en la segunda actividad nos tocó abrimos un github, muy particular en mi caso, primero abrí uno con el nombre lucia1595, por no conocer sobre el proceso de creación, siempre que conocemos algo nuevo tendemos a investigar, en mi caso por ingenua, tuve que correr con el riesgo y capaz, sea obejto de una mala calificación. Luego para que me agregaran al grupo de pd2 hice el Lucia-web-, con este me aceptaron, y logre estar en el grupo. Pero por error humano realicé un clic que hizo que ambas cuentas estuvieran forked y por lo cual, en el grupo, aparezco como Lucia-web- pero abajo de mi cuenta dice forked lucia1595/Lucia-web-. 


*Investigando un poco me doy cuenta de que esto sucede, para lo siguiente:*
 
Una bifurcación es una copia de un repositorio que administras. Las bifurcaciones le permiten ejecutar cambios en un proyecto sin afectar el repositorio original. Puede obtener actualizaciones o enviar cambios al repositorio original con solicitudes de incorporación de cambios.


## Seguido de Github, descargamos gitbash y anaconda. El Gitbash lo usamos en la segunda actividad, en el cual usamos para editar nuestro readme de GitHud.


*Para configurar usamos:*


- git clone para clonar el repositorio 
- git config para configirurar el Github 
- user.name aquí se colocó el nombre del usuario del Github 
- user.gmail aquí utilizamos el correo que utilizamos para abrir Github, el correo de nebrija. 


**Después usamos los siguientes pasos:**
- pwd para saber en qué carpeta estábamos.
- cd Lucia-web- para darle una ruta, cuya ruta era nuestro repositorio. 
- ls para conocer los archivos que teníamos en la carpeta. 
- git status para saber sobre qué archivo que tenemos en seguimiento.
- git add para añadir alguna carpeta. 
- git commit -m "añado" es para añadir algún comentario. 
- git push guarda los cambios en nuestro repositorio. 
- git pull nos guarda en el archivo local. 


En la tercera actividad utilizamos Jupyter notebook, esta nos abre si tenemos descargado Anaconta, primero suele abrise como especie de una terminal, luego se abre en nuestro navegador la carpeta de nuestro repositorio, en esa abrimos el notebook, en el que se trabajó una programación literaria, usando un código de Web Scrapping de una práctica que se hizo en una asignatura llamada Programación. En esta detallamos lo que hacía cada uno de los códigos, cuya escritura tenía que implemntarse con Markdown. Despúes de realizar esta tarea en Jupyter, con Gitbash la subiamos a Github. 


La cuarta actividad, mi favorita, fue la que usamos gráficos, pip install pandas, algo totalemnte nuevo para nosotros, ya que anteriormenete usabamos pyton, luego utilizamos el enunciado import para importar el programa panda. 


Hice gráfico con los casos de COVID-19 de España, en estos utilizamos variables que luego se iban reajustando para no solo hacer un gráfico de dos países, España y Panamá, sino hacer una comparativa de los países centroamericanos. 


Entre las variables que utilizamos: df data frame que busca de fragmentos de datos en los conjuntos de datos. Que si los queriamos ajustar en columnas se usó por ejemplo casos_es = df_rt_es.set_index('Date')['Cases']
casos_pa.plot(title="Casos de Covid-19 en España") trazar datos directamente desde su DataFrame usando el método plot(). Para trazar múltiples columnas de datos en un solo cuadro, simplemente tenemos que pasar la lista de columnas al argumento y de la función de trazado. 


Algo interesante fueron dos gráficos distintos a los que se buscaba plasmar, pero para saber que existen múltiples formas de mostrar los datos, el profesor nos enseña lo que hace kind="area" colorea el área o en cambio kind="bar" es una gráfica de barra. 


Después de haber pasado por ensayo y errores, por fin logramos recopilar todo este repertorio y ver todo culminado, aprendido nuevo lenguaje y nuevos códigos, además de poder poner el práctica
todo esto en mi trabajo diario.
