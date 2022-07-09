# Ad3

Esta es la **actividad dirigida 3**, consiste en hacer un ejercicio de programación literaria aprovechando el código que hemos usado en programación con Python y dónde realizamos web scrapping. 


# Programación literaria

## Librerías y módulos que vamos a importar 


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
```

**A continuación detallamos que hace cada módulo y librería**

***Módulos***

 [time](https://www-programiz-com.translate.goog/python-programming/time?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sc): Maneja tareas relacionadas con el tiempo. 

[csv](https://www-programiz-com.translate.goog/python-programming/csv?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sc): Facilita mucho el trabajo con archivos CSV.

[re](https://docs.python.org/es/3/library/re.html): Proporciona operaciones de coincidencia de expresiones regulares similares a las encontradas en Perl.

[os](https://docs-python-org.translate.goog/3/library/os.html?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sc): Proporciona una forma portátil de usar la funcionalidad dependiente del sistema operativo.

***Librerías***

[requests](https://www-dataquest-io.translate.goog/blog/tutorial-an-introduction-to-python-requests-library/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sc): Admite el envío de información adicional a un servidor web a través de parámetros y encabezados, la codificación de las respuestas del servidor, la detección de errores y el manejo de redireccionamiento.

[bs4](https://omz--software-com.translate.goog/pythonista/docs/ios/beautifulsoup.html?_x_tr_sch=http&_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sc): Beautiful Soup es una librería que extraer datos de archivos HTML y XML. 

[pandas](https://aprendeconalf.es/docencia/python/manual/pandas/): Es una librería de Python especializada en el manejo y análisis de estructuras de datos.

[termcolor](https://pypi-org.translate.goog/project/termcolor/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sc):Formato de color ANSII para salida en terminal.



## Instalar librerías 


```python
pip install requests bs4 pandas termcolor
```

##  Desgloce del proceso del programa a desarrollar 


```python
resultados = []
```

Un espacio en el que se añadirán los resultados del scrapping.


```python
req = requests.get("https://resultados.elpais.com")
```

Una de las operaciones más habituales con la librería requests es hacer una petición GET, ya sea para obtener el contenido de una web o para realizar una petición a un API.

Para ello, simplemente tienes que invocar a la función get() indicando la URL a la que hacer la petición.


```python
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
```

La sentencia condicional ***if*** se usa para tomar decisiones, este evaluá básicamente una operación lógica. ***req.status_code***  su propio nombre describe son una serie de códigos de tres cifras estandarizados y que están relacionados con una serie de determinados errores que pueden suceder al introducir en nuestro navegador una dirección web. El valor 200 significa que la solicitud fue exitosa y el servidor respondió con los datos solicitados. En caso de que no se encuentre un resultado como el indicado se mostrará el mensaje "No se puede hacer Web Scrapping" en seguido de la URL errónea.


```python
soup = BeautifulSoup(req.text, 'html.parser')
```

Permite extraer información de contenido en formato ***HTML o XML***. Para usarla, es necesario especificar un ***parser***, que es responsable de transformar un documento HTML o XML en un árbol complejo de objetos Python. Esto permite, por ejemplo, que podamos interactuar con los elementos de una página web como si estuviésemos utilizando las herramientas del desarrollador de un navegador.


```python
tags = soup.findAll("h2")
```

El objeto ***Tag*** se refiere a una etiqueta XML o HTML real en el documento. Si le agregamos la variable "h2" permite encontrar todas las etiquetas (***h2***) dentro de la página que han desarrollado.


```python
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

Usamos el código en este caso, ya que necesitamos que se imprima el texto de la etiqueta ***h2*** 

Código fuente
---------------

A continuación pongo el **código fuente**:


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored

resultados = []

req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')

tags = soup.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')

tags = soup11.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')

tags = soup12.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')

tags = soup13.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')

tags = soup14.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')

tags = soup15.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')

tags = soup16.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')

tags = soup17.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)


os.system("clear")

print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))

print(colored("Igualdad", 'green', attrs=['bold']))

str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))

print(colored("Mujeres", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))

str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))

str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))

str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```
