# Proyecto Calidad del Aire
Proyecto de centro de secundaria sobre calidad del aire CO2(ppm), temperatura(ºC) y humedad(%). Registrar datos en la nube a tiempo real (IoT)
en la plataforma THINGSPEAK, para su posterior recuperación en formato .CSV. Finalmente el alumnado hará DATA-SIENCE, tratando los datos con 
la librería PANDAS, una de las más conocidas de PYTHON.

## Índice

*[Introducción del Proyecto](#Introducción-del-Proyecto)

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
  
*[Objetivos 20/30](https://www.un.org/sustainabledevelopment/es/biodiversity/)

<div align="justify">
   En la Cumbre Mundial para el Desarrollo Sostenible de 2015 los Estados Miembros de la ONU aprobaron la Agenda 2030 para el Desarrollo Sostenible1, con el fin de erradicar la pobreza, proteger el planeta y asegurar la prosperidad para todas las personas para el año 2030. Este acuerdo es un llamado universal para la lucha a favor del desarrollo humano sostenible en todo el planeta y para ello define 17 objetivos, los denominados “Objetivos de Desarrollo Sostenible (ODS)”, que contienen a su vez 169 metas. 
   El desarrollo sostenible se plantea como la integración de forma equilibrada de las tres dimensiones del desarrollo: la social, la económica y la ambiental. En la dimensión social, entre otros muchos aspectos, se plantea la erradicación de la pobreza como uno de los mayores desafíos que enfrenta el mundo y un requisito indispensable para el desarrollo sostenible. En el ámbito económico, se plantea establecer condiciones para un crecimiento económico inclusivo y sostenido, una prosperidad compartida y el trabajo decente para todas las personas. En la dimensión ambiental, junto con la protección del planeta y sus recursos naturales, incluye la definición del informe Brundtland de “satisfacer las necesidades del presente sin comprometer las necesidades de las futuras generaciones”. 
</div>  

*[Descripción del proyecto](#descripción-del-proyecto)

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

*[Montaje Prototipo](#Montaje-Prototipo)

https://user-images.githubusercontent.com/59457645/216448394-0041b0fe-fd36-4569-8b1d-80d863bcebb6.mp4

*[Código ARDUINO](https://github.com/rfumfum2022/Proyecto-Calidad-del-Aire/blob/main/IES_Andres_Bello_MQ_135_CO2_Calibrado_LOGO.ino)

*[Código PYTHON](https://github.com/rfumfum2022/Proyecto-Calidad-del-Aire/blob/main/Plantilla_CO2.ipynb)

*[ETAPAS del PROYECTO](#ETAPAS-del-PROYECTO)
* [Montaje de cajas de registro](#Montaje-cajas-de-registro)
* [IoT en la nube](#IoT-en-la-nube)
* [DATA SCIENCE](#DATA-SCIENCE)
* [Programación en PYTHON](#Programación-en-Python)
* [Google COLABORATOTY](#Google-COLABORATORY)

*[Personas-Desarrolladores del Proyecto](#personas-desarrolladores)

* [Licencia](#licencia)

*[Conclusión](#conclusión)
