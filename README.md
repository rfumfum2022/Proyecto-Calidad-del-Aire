# Proyecto Calidad del Aire
Proyecto de centro de secundaria sobre calidad del aire CO2(ppm), temperatura(ºC) y humedad(%). Registrar datos en la nube a tiempo real (IoT)
en la plataforma THINGSPEAK, para su posterior recuperación en formato .CSV. Finalmente el alumnado hará DATA-SCIENCE, tratando los datos con 
la librería PANDAS, una de las más conocidas de PYTHON.

## Índice

* 1-[Introducción del Proyecto](#Introducción-del-Proyecto)

* 2-[Fundamentos Científicos](https://www.uam.es/uam/media/doc/1606849471777/plan-de-medicion-de-co2-en-espacios-docentes.pdf)

* 3-[Objetivos 20/30](https://www.un.org/sustainabledevelopment/es/biodiversity/)

* 4-Descripción del proyecto](#descripción-del-proyecto)

* 5-[Inventario](#Inventario)

* 6-[Montaje Prototipo](#Montaje-Prototipo)

* 7-[Código ARDUINO](https://github.com/rfumfum2022/Proyecto-Calidad-del-Aire/blob/main/IES_Andres_Bello_MQ_135_CO2_Calibrado_LOGO.ino)

* 8-[Código PYTHON](https://github.com/rfumfum2022/Proyecto-Calidad-del-Aire/blob/main/Plantilla_CO2.ipynb)

* 9-[ETAPAS del PROYECTO](#ETAPAS-del-PROYECTO)

   * 9.1- [Montaje de cajas de registro](#Montaje-cajas-de-registro)

   * 9.2- [IoT en la nube](#IoT-en-la-nube)

   * 9.3- [DATA SCIENCE](#DATA-SCIENCE)

   * 9.4- [Programación en PYTHON](#Programación-en-Python)

   * 9.5- [Google COLABORATOTY](#Google-COLABORATORY)

* 10-[Personas-Desarrolladores del Proyecto](#personas-desarrolladores)

* 11-[Licencia](#licencia)

* 12-[Conclusión](#conclusión)

__________________________________________________________________________________________________________________________________________________________

*[Introducción del Proyecto](#Introducción-del-Proyecto)

<div align="justify">
  
Un proyecto de medidor de CO<sub>2</sub> en la escuela es una iniciativa que tiene como objetivo medir y monitorear los niveles de dióxido de carbono en el aire interior de la escuela. Este proyecto es importante porque el aire interior de los edificios, incluyendo las escuelas, puede ser hasta cinco veces más contaminado que el aire exterior.

El exceso de CO<sub>2</sub> en el aire interior de un edificio puede tener un impacto negativo en la salud y el bienestar de los estudiantes y el personal escolar. Por lo tanto, es esencial mantener los niveles de CO<sub>2</sub> en un rango seguro.

Este proyecto implicará la implementación de medidores de CO<sub>2</sub> en diferentes aulas de la escuela, con el objetivo de recopilar datos sobre los niveles de CO<sub>2</sub> en tiempo real. Además, se utilizarán gráficos y visualizaciones para representar estos datos y permitir una interpretación más fácil.

El objetivo final del proyecto es utilizar estos datos para tomar medidas efectivas para mejorar la calidad del aire interior de la escuela y garantizar un ambiente saludable y seguro para todos.

En resumen, el proyecto de medidor de CO<sub>2</sub> en la escuela es una iniciativa importante para mejorar la salud y el bienestar de los estudiantes y el personal escolar, y para crear un ambiente más sostenible en la escuela.

</div>  
  
__________________________________________________________________________________________________________________________________________________________  
  
*[Fundamentos Científicos](https://www.uam.es/uam/media/doc/1606849471777/plan-de-medicion-de-co2-en-espacios-docentes.pdf)

<div align="justify">

La tasa de ventilación aconsejada para conseguir una calidad de aire buena es de 12,5 litros/segundo y persona y se corresponde aproximadamente a 56 renovaciones/hora. Esta tasa de ventilación puede conseguirse aumentando el caudal de aire exterior aportado por medios naturales (abriendo puertas y ventanas durante el tiempo que se estime necesario según las características de cada espacio) o mecánicos o bien reduciendo la ocupación del local. 

El tiempo de ventilación depende de múltiples factores, que varían de un aula a otra (m<sup>3</sup>, grado de ocupación, actividad realizada, orientación, condiciones ambientales exteriores, etc.). Para determinar cuánto tiempo es necesario tener las ventanas abiertas se puede calcular la concentración de CO<sub>2</sub> en el aire que es un buen indicador de la tasa de renovación de un espacio. 

En el exterior, las concentraciones de CO<sub>2</sub> son de aproximadamente **420-450 ppm** (partes por millón)1, aunque pueden variar en entornos urbanos o rurales. Cuando un edificio está ocupado, las concentraciones de CO<sub>2</sub> en el interior son elevadas por el CO<sub>2</sub> exhalado por sus ocupantes.   

Se establece que para garantizar una correcta ventilación los niveles de CO<sub>2</sub> no deberían superar el umbral de **800-1000 ppm**. Cuando se superan las **1000 ppm** (partes por millón) se debe ventilar hasta reducir la concentración a **800 ppm**. (Como referencia, la concentración de CO<sub>2</sub> en exterior es de **420 ppm**). 

Hay que recordar que estas concentraciones de CO<sub>2</sub> están muy lejos de ser perjudiciales para la respiración humana y sólo deben interpretarse como indicador para la necesidad de ventilación. 
  

</div>
  
<div align="center">
<img width="538" height="138" align=”middle” alt="Indices CO2" src="https://user-images.githubusercontent.com/59457645/216457621-f19b2ee1-5438-4ce8-8e22-aee5cefed786.png" >
</div>
  
 _________________________________________________________________________________________________________________________________________________________
  
*[Objetivos 20/30](https://www.un.org/sustainabledevelopment/es/biodiversity/)

<div align="justify">
  
   En la **Cumbre Mundial para el Desarrollo Sostenible de 2015 los Estados Miembros de la ONU aprobaron la Agenda 2030 para el Desarrollo Sostenible1, con el fin de erradicar la pobreza, proteger el planeta y asegurar la prosperidad para todas las personas para el año 2030**. Este acuerdo es un llamado universal para la lucha a favor del desarrollo humano sostenible en todo el planeta y para ello **define 17 objetivos**, los denominados **“Objetivos de Desarrollo Sostenible (ODS)”**, que contienen a su vez **169 metas**. 
  
   El desarrollo sostenible se plantea como la integración de forma equilibrada de las tres dimensiones del desarrollo: la social, la económica y la ambiental. 
- En la dimensión social, entre otros muchos aspectos, se plantea la erradicación de la pobreza como uno de los mayores desafíos que enfrenta el mundo y un requisito indispensable para el desarrollo sostenible. 
- En el ámbito económico, se plantea establecer condiciones para un crecimiento económico inclusivo y sostenido, una prosperidad compartida y el trabajo decente para todas las personas. 
- En la dimensión ambiental, junto con la protección del planeta y sus recursos naturales, incluye la definición del informe Brundtland de “satisfacer las necesidades del presente sin comprometer las necesidades de las futuras generaciones”. 
  
</div>  

__________________________________________________________________________________________________________________________________________________________

*[Descripción del proyecto](#descripción-del-proyecto)

<div align="justify">

Este proyecto para montar un medidor de CO<sub>2</sub> es una iniciativa interdisciplinaria que involucra departamentos de física y química, tecnología, biología y matemáticas. Su objetivo es medir y monitorear los niveles de dióxido de carbono (CO<sub>2</sub>), temperatura y humedad relativa en un ambiente determinado.

El proceso comenzará con la construcción y diseño del medidor de CO<sub>2</sub>, que será realizado por los departamentos de física y química y tecnología. Este medidor utilizará sensores para medir los niveles de CO<sub>2</sub>, temperatura y humedad relativa.

Una vez que se haya construido el medidor, se instalará en un lugar determinado y se comenzarán a recoger los datos en tiempo real. Estos datos serán transferidos a la nube, donde el departamento de matemáticas realizará un análisis de datos para identificar patrones y tendencias en los niveles de CO<sub>2</sub>, temperatura y humedad relativa.

El departamento de biología también participará en el proyecto, investigando cómo los niveles de CO<sub>2</sub>, temperatura y humedad relativa afectan a la salud y el bienestar de los seres vivos en el ambiente.

El proyecto permitirá a los estudiantes y profesores aprender sobre cómo funciona un medidor de CO<sub>2</sub>, cómo se realiza un análisis de datos y cómo los niveles de CO<sub>2</sub>, temperatura y humedad relativa afectan a la salud y el bienestar de los seres vivos.

En resumen, este proyecto es una oportunidad para los estudiantes y profesores para trabajar juntos en un proyecto interdisciplinario y aprender más sobre la tecnología, la ciencia y la matemática mientras se realiza una investigación importante sobre la calidad del aire en un ambiente determinado.

</div>  
  
__________________________________________________________________________________________________________________________________________________________
  
*[Inventario](#Inventario)

| Dispositivo | Precio|
| ------------- | ------------- |
| 1-WeMos D1 ESP8266 WiFi | 5,5600 € / 1 Unidad  |
| 2- Mini Protoboard 25 puntos  | 0,9813 € / 1 Unidad |
| 3-Cable Micro USB 50 cm  | 1,7300 € / 1 Unidad  |
| 4-Módulo con sensor de temperatura y humedad DHT22 | 5,9346 € / 1 Unidad |
| 5-Convertidor DC-DC LM2596 1,25-30V 3A Step-Down HW-411  | 2,4299 € / 1 Unidad  |
| 6-Fuente de alimentación 12V 2A con conector DC Jack  | 12,9000 € / 1 Unidad |
| 7-Conector DC Jack Hembra 5,5 x 2,1 mm borna   | 0,6100 € / 1 Unidad |
| 8-Set 40 cables Dupont 20 cm macho-hembra 1 y macho-macho | 2,8972 € / 1 Unidad   |
| 9-Caja de registro electrónico | 1,5 € / 1 Unidad |
| (Precios aproximados) |

__________________________________________________________________________________________________________________________________________________________

*[Montaje Prototipo](#Montaje-Prototipo)

https://user-images.githubusercontent.com/59457645/216448394-0041b0fe-fd36-4569-8b1d-80d863bcebb6.mp4

___________________________________________________________________________________________________________________________________________________

*[Código ARDUINO](https://github.com/rfumfum2022/Proyecto-Calidad-del-Aire/blob/main/IES_Andres_Bello_MQ_135_CO2_Calibrado_LOGO.ino)


<div align="justify">
  
Arduino es una plataforma de hardware y software libre y de código abierto que permite a los desarrolladores crear proyectos interactivos con sensores, actuadores, displays y otros componentes electrónicos. Fue diseñada para ser fácil de usar y accesible para personas sin experiencia previa en electrónica o programación.

El hardware de Arduino consiste en una placa de control basada en un microcontrolador y conexiones para componentes externos. El software de Arduino incluye un entorno de desarrollo integrado (IDE) que permite a los usuarios escribir, compilar y cargar código en la placa de control.

Arduino es ampliamente utilizado en una variedad de proyectos, desde juguetes interactivos hasta sistemas industriales. Algunas de las aplicaciones más comunes de Arduino incluyen la robótica, la automatización del hogar, la creación de instrumentos musicales digitales, la visualización de datos y la automatización de procesos en la industria.

En resumen, Arduino es una herramienta poderosa y versátil que permite a los desarrolladores crear proyectos electrónicos interactivos de manera fácil y accesible.
  
</div> 

__________________________________________________________________________________________________________________________________________________

*[Código PYTHON](https://github.com/rfumfum2022/Proyecto-Calidad-del-Aire/blob/main/Plantilla_CO2.ipynb)

<div align="justify">

Python es un lenguaje de programación de alto nivel, interpretado y orientado a objetos. Fue creado por Guido van Rossum en 1989 y es uno de los lenguajes de programación más populares y ampliamente utilizados en todo el mundo.

Python es conocido por su sintaxis clara y legible, lo que lo hace fácil de aprender y usar para programadores principiantes y experimentados por igual. Además, cuenta con una amplia variedad de bibliotecas y herramientas de análisis de datos, lo que lo hace ideal para el desarrollo de aplicaciones en áreas como la ciencia de datos, la inteligencia artificial, la automatización y la creación de juegos.

Además de ser fácil de aprender, Python es un lenguaje muy versátil y se puede utilizar para una amplia variedad de tareas, incluyendo el desarrollo de aplicaciones web, aplicaciones de escritorio, análisis de datos, automatización de tareas y mucho más.

En resumen, Python es un lenguaje de programación popular, fácil de aprender y versátil, que es ideal para una amplia variedad de proyectos y aplicaciones.

</div> 

____________________________________________________________________________________________________________________________________________________

*[ETAPAS del PROYECTO](#ETAPAS-del-PROYECTO)
* [Montaje de cajas de registro](#Montaje-cajas-de-registro)
* [IoT en la nube](#IoT-en-la-nube)
* [DATA SCIENCE](#DATA-SCIENCE)
* [Programación en PYTHON](#Programación-en-Python)
* [Google COLABORATOTY](#Google-COLABORATORY)

_____________________________________________________________________________________________________________________________________________________

*[Personas-Desarrolladores del Proyecto](#personas-desarrolladores)

_____________________________________________________________________________________________________________________________________________________

* [Licencia](#licencia)

______________________________________________________________________________________________________________________________________________________

*[Conclusión](#conclusión)
