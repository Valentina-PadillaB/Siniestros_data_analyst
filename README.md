¡Bienvenidos al  proyecto ***Data Analyst***.
<p align='center'>
<img src = 'https://static.lajornadaestadodemexico.com/wp-content/uploads/2022/08/Siniestros-viales.jpg' height = 500>
<p>

# Siniestros Viales en CABA
En este proyecto, analizamos los siniestros viales en la Ciudad Autónoma de Buenos Aires (CABA) para generar información útil que permita a las autoridades locales tomar medidas para reducir la cantidad de víctimas fatales de los accidentes de tránsito. Para ello, utilizamos dos datasets provistos por el Observatorio de Movilidad y Seguridad Vial (OMSV), uno sobre homicidios en siniestros viales y otro sobre lesiones en siniestros viales, ambos correspondientes al período 2016-2021.

## Fuentes de Datos
Los datos utilizados en este proyecto provienen de dos conjuntos de datos diferentes, cada uno de los cuales consta de dos hojas de datos:
-> Homicidios en Siniestros Viales: Este conjunto de datos incluye información sobre los homicidios ocurridos en siniestros viales en la Ciudad de Buenos Aires durante el período mencionado. Proporciona detalles sobre los hechos en sí, como la fecha, la ubicación y las circunstancias.
-> Lesiones en Siniestros Viales: El segundo conjunto de datos se centra en las lesiones sufridas por las víctimas de siniestros viales en la ciudad. Al igual que el conjunto de datos de homicidios, proporciona información detallada sobre los incidentes, incluyendo la fecha, la ubicación y la gravedad de las lesiones.

## Origen de los Datos
Es importante destacar que los conjuntos de datos utilizados en este proyecto provienen de una fuente confiable y pública, Buenos Aires Data, lo que garantiza la integridad y la transparencia de los datos.

## Introducción
Para llevar a cabo este análisis, se dispuso de un valioso conjunto de datos recopilados durante el período 2016-2021. Estos datos se desglosan en dos categorías fundamentales: homicidios en siniestros viales y lesiones en siniestros viales, y cada una de ellas contiene dos hojas de datos: una dedicada a los hechos y otra a las víctimas involucradas.

Es importante destacar que el acceso a todo el proceso detallado de cada una de las secciones mencionadas a continuación está disponible en el archivo "Code.ipynb". En caso de dificultades en su visualización a través de la plataforma Git, recomendamos su descarga para una revisión más detallada.
1. Limpieza y preparación de los datos.
2. Exploración de datos y análisis descriptivo.
3. Análisis de víctimas.
4. Análisis espacial.
5. Creación de KIPs y métricas clave.
6. Conclusiones y sugerencias
   
## Limpieza y preparación de los datos
Antes de realizar un análisis de datos, es crucial identificar cuales son los datos que vamos a utilizar, por qué los vamos a utilizar, y estandarizarlos para mejor manejo de la base de datos. En este caso, decidimos normalizar los encabezados de las columnas, eliminar columnas redundantes o no necesarias, renombrar algunas columnas y eliminar valores nulos o no válidos.

## Exploración de datos y análisis descriptivo
En esta sección, llevamos a cabo un análisis exploratorio de los datos de siniestros viales en CABA. Algunos de los aspectos indispensables que abordamos en este análisis incluyen:
Búsqueda de valores faltantes, valores atípicos/extremos u outliers y registros duplicados.
Utilización de gráficos coherentes según la tipología de variable que corresponda.

### Homicidios Viales

#### Tasa de homicidios viales (número de homicidios viales por año o mes) como un KPI para seguimiento.
En cuanto a los homicidios viales, se realizó el cálculo de la tasa de homicidios viales, que consiste en determinar el número de homicidios viales por año o mes como un indicador clave de rendimiento (KPI) para su seguimiento. La tasa anual de homicidios viales proporciona una visión a largo plazo de la incidencia de estos casos en la Ciudad Autónoma de Buenos Aires durante un año completo. Este enfoque temporal nos permite identificar tendencias y patrones a lo largo de varios años, lo que resulta fundamental para evaluar el impacto de las políticas y medidas de seguridad implementadas a largo plazo en la reducción de la violencia vial en la ciudad.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Tasa%20anual%20de%20Homicidios%20Viales.png)

En la gráfica de la tasa anual de homicidios viales, se destaca una reducción significativa a partir del año 2018. Esta disminución puede atribuirse a la implementación del Decreto 101-2018 por parte del Gobierno de Buenos Aires, que autorizó programas de educación vial. A partir de 2019, se implementó a totalidad el 5954 decto 101-2018 y se llevaron a cabo campañas de concientización destinadas a educar a conductores, peatones y ciclistas, segmentadas por grupos de edad, sobre la importancia de respetar las normas de tráfico y las medidas de seguridad.

Estas campañas de concientización incluyeron charlas educativas en las escuelas y actividades de sensibilización pública. Además, se considera esencial estimar la tasa de homicidios viales a nivel mensual, ya que permite un seguimiento más detallado de la evolución de estos eventos en el corto plazo y facilita la identificación de problemas emergentes.

* Para obtener información adicional sobre estas campañas de educación vial, se puede consultar el siguiente enlace: [Enlace a la información.](https://buenosaires.gob.ar/movilidad/plan-de-seguridad-vial/educacion-para-la-movilidad-sustentable#:~:text=Docentes%3A%201%20Curso%20Educaci%C3%B3n%20Vial%20para%20la%20Movilidad,...%208%20Mi%20primera%20licencia%20...%20M%C3%A1s%20elementos)

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Tasa%20mensual%20de%20Homicidios%20Viales.png)

El análisis mediante el uso del promedio móvil nos proporciona una perspectiva valiosa sobre la tendencia de la tasa de homicidios viales a lo largo del tiempo. A pesar de un repunte registrado en diciembre de 2020, es evidente que, en general, la tasa ha experimentado una disminución desde la implementación del Decreto 101-2018 (conocido como 5954 decto 101-2018).

Sin embargo, es importante señalar que estos repuntes eventuales en la tasa indican la presencia de desafíos continuos en la solución planteada. Esto subraya la necesidad de seguir profundizando en nuestro análisis y de identificar posibles áreas de mejora para abordar de manera efectiva la problemática de los homicidios viales en la Ciudad de Buenos Aires.

#### Análisis de la distribución de la hora en que ocurren los homicidios viales.
El análisis del momento en que ocurren con mayor frecuencia los homicidios viales es fundamental para tomar decisiones efectivas en cuanto a medidas de seguridad pública. Esta información proporciona insights valiosos que pueden ser utilizados por las autoridades para mejorar la seguridad vial en momentos críticos. Por ejemplo, si se identifica que la mayoría de los homicidios viales ocurren en las primeras horas de la mañana, se pueden diseñar estrategias específicas, como la implementación de patrullas adicionales o campañas de concientización dirigidas a esa franja horaria, con el objetivo de reducir el riesgo y aumentar la seguridad de los ciudadanos.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Distribucion%20de%20Homicidios%20Viales%20por%20hora%20del%20dia.png)

El análisis de la distribución horaria de los homicidios viales revela patrones interesantes. En la gráfica, podemos observar que las horas con menor ocurrencia de homicidios viales son las 2:00 AM y la 1:00 PM. Esto puede explicarse por el hecho de que, en esas horas, la mayoría de las personas tiende a no estar en movimiento, ya sea debido al descanso nocturno o a la hora del almuerzo. Por otro lado, las horas con mayor incidencia de homicidios viales son las 6:00 AM y las 7:00 AM. Esta tendencia podría relacionarse con la fatiga o somnolencia de los conductores en las primeras horas de la mañana, ya que es un momento en el que es posible que no hayan tenido suficiente descanso. Estos hallazgos proporcionan información valiosa para la planificación de estrategias de seguridad vial específicas para las horas de mayor riesgo.

#### Exploración de la ubicación de los homicidios en función de la comuna y el tipo de calle.
La consideración del tipo de calle en la que ocurren más homicidios viales es fundamental, ya que esto puede indicar deficiencias en la infraestructura vial que deben abordarse para mejorar la seguridad de los actores viales. Por lo tanto, se genera un gráfico de distribución para identificar las infraestructuras viales más peligrosas para los ciudadanos.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Distribucion%20de%20Homicidios%20Viales%20por%20hora%20del%20dia.png)


Es interesante notar que la mayoría de los homicidios viales ocurren en las avenidas, lo que tiene sentido debido a varios factores. En primer lugar, las avenidas generalmente tienen un alto flujo de tráfico en comparación con otros tipos de calles. Además, las avenidas son una característica común en la ciudad, lo que aumenta las posibilidades de que ocurran accidentes de tráfico, incluidos los homicidios viales. Es notable que en casi todas las comunas (excepto la comuna 12) se registre un alto número de homicidios viales en las avenidas, lo que sugiere la necesidad de revisar la calidad de estas vías o aumentar la supervisión vial en esas áreas de la ciudad.

Por otro lado, el gráfico revela que la Comuna 1 es la que presenta la mayor cantidad de homicidios viales. Esta comuna es una de las áreas más transitadas y turísticas de Buenos Aires, con una gran cantidad de actividades culturales, comerciales y turísticas. Cada uno de sus barrios tiene su propio carácter y atractivo, lo que la convierte en una parte significativa de la vida urbana en la ciudad.

### Lesiones

#### Análisis de la distribución de la hora y el día de la semana en que ocurren las lesiones viales.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Distribucion%20de%20Lesiones%20Viales%20por%20D%C3%ADa%20de%20la%20Semana.png)

En contraste con los homicidios, las lesiones viales tienden a aumentar alrededor de las 5:00 PM, lo cual se alinea con informes recientes que indican que las horas pico en Buenos Aires comienzan a la 1:00 PM y se extienden hasta las 5:00 PM. Como se refleja en nuestro gráfico, estas son las horas en las que se registran la mayoría de las lesiones viales. Esto sugiere una relación directa entre el flujo de vehículos y la incidencia de lesiones viales, ya que un mayor flujo de tráfico durante las horas pico puede aumentar el riesgo de accidentes.

Fuente: [Enlace a la fuente](https://www.lanacion.com.ar/buenos-aires/fin-de-la-hora-pico-cuales-son-los-horarios-con-mayor-circulacion-de-vehiculos-en-las-autopistas-y-nid04092023/)

Adicionalmente, considerar en qué días de la semana se producen con mayor frecuencia las lesiones viales es crucial para implementar medidas de seguridad dirigidas a proteger a los actores viales que son más activos durante esos días. Esto podría incluir campañas de concientización específicas o patrullas de seguridad adicionales en momentos de mayor riesgo.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Distribucion%20por%20Tipo%20de%20Vehiculo%20Involucrado%20en%20Lesiones%20Viales.png)



La gráfica es contundente, sin embargo, es relevante destacar que los accidentes de tráfico y las lesiones viales son eventos multifactoriales, y aunque los viernes pueden experimentar un aumento debido al inicio del fin de semana y las actividades sociales, en términos generales, las lesiones tienden a ocurrir principalmente en los días laborales debido a la mayor actividad relacionada con el trabajo y el tráfico durante estos días. Esto subraya la importancia de implementar medidas de seguridad consistentes a lo largo de la semana para proteger a los actores viales en todo momento.

#### Exploración de la distribución por tipo de vehículo involucrado.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Distribucion%20por%20Tipo%20de%20Vehiculo%20Involucrado%20en%20Lesiones%20Viales.png)


Es evidente que la mayoría de las lesiones viales ocurren en motocicletas, y esto puede atribuirse a varias razones. Las motocicletas son vehículos altamente maniobrables, lo que las hace propensas a moverse con agilidad entre el tráfico. Sin embargo, si no se manejan con precaución, esta ventaja puede convertirse en un riesgo, ya que aumenta la posibilidad de colisiones y caídas. Además, algunos motociclistas pueden adoptar comportamientos de conducción riesgosos, como el exceso de velocidad o la omisión del uso de cascos protectores, lo que incrementa aún más el peligro de accidentes y lesiones.

Es crucial destacar la importancia de que los motociclistas respeten los límites de velocidad y sigan las normas de tráfico para mantener la seguridad vial. Esto puede lograrse mediante el uso de cámaras o detectores de velocidad en zonas estratégicas, como las avenidas, así como a través de programas de capacitación en seguridad vial específicamente diseñados para motociclistas. Estas medidas son fundamentales para reducir el número de lesiones viales en motocicletas y proteger la vida de los actores viales.

## 3. Análisis de Víctimas
Uno de los objetivos clave de esta fase fue calcular las posibles relaciones y distribuciones de homicidios y lesiones viales en la Ciudad Autónoma de Buenos Aires. Esta métrica fundamental nos proporcionó información sobre la gravedad de los siniestros viales en la región y fue esencial para comprender la magnitud del problema.

### Análisis de la distribución de edades y sexos de las víctimas en ambos conjuntos de datos.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/main/imagenes/Distribucion%20Esperada%20de%20Gravedad%20de%20Lesiones%20por%20Tipo%20de%20Actor%20Vial.png)

Los datos sobre sexo y edad de las víctimas son fundamentales para desarrollar políticas públicas y medidas de seguridad efectivas. Por ejemplo, en este gráfico se observa que un grupo demográfico particular (jóvenes adultos de entre 20 y 40 años) tiene una alta probabilidad de ser víctima de un accidente de tráfico, tanto hombres como mujeres. Esto sugiere la necesidad de implementar programas de educación vial específicos y campañas de concientización dirigidas a este grupo de edad para promover comportamientos seguros en la vía pública y reducir el riesgo de lesiones viales. Estos datos son valiosos para diseñar estrategias de prevención y mejorar la seguridad vial en la Ciudad Autónoma de Buenos Aires.

### Relación entre la gravedad de las lesiones y el tipo de actor vial
Los resultados de este tipo de estudio pueden tener un impacto significativo en las políticas y regulaciones de tráfico. Por ejemplo, si se encuentra que un cierto tipo de actor vial tiene una mayor probabilidad de sufrir lesiones graves, las autoridades pueden considerar la implementación de restricciones o regulaciones adicionales para mejorar su seguridad. En este análisis, también se tendrán en cuenta los "SD" para obtener una imagen más completa de las lesiones. Se utilizará la Prueba de Chi Cuadrado para determinar si existe una asociación significativa entre la gravedad de las lesiones y el tipo de actor vial, como peatones, ciclistas, conductores de automóviles, etc. Si se encuentra una asociación significativa, esto indicará que el tipo de actor vial y la gravedad de las lesiones no son independientes, lo que proporciona información valiosa para la toma de decisiones en materia de seguridad vial.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/raw/d48e2d3ae80a5e504060f7fec08bcde26afc252e/imagenes/Distribucion%20Esperada%20de%20Gravedad%20de%20Lesiones%20por%20Tipo%20de%20Actor%20Vial.png)


El análisis de este gráfico revela varias conclusiones importantes. En primer lugar, se destaca la necesidad de mejorar la recopilación de datos sobre accidentes de tránsito en la ciudad de Buenos Aires. La presencia de una cantidad significativa de casos etiquetados como "Sin Datos" sugiere que hay margen para fortalecer las entidades encargadas de la recopilación de datos, ya que contar con información completa y precisa es fundamental para realizar análisis efectivos y tomar medidas de seguridad vial adecuadas.

Además, es preocupante observar que los motociclistas representan el grupo con la mayor cantidad de lesiones graves, y esta diferencia es significativa en comparación con la distribución de lesiones entre automovilistas y ciclistas. Esto resalta la importancia de dirigir esfuerzos hacia la capacitación y concienciación de los motociclistas, así como de aplicar sanciones más rigurosas para aquellos que no cumplan con las normas de seguridad vial, especialmente en lo que respecta al uso de elementos de protección.

Estas conclusiones subrayan la necesidad de implementar políticas y medidas específicas para abordar la seguridad vial de los motociclistas y mejorar la calidad de los datos recopilados en futuros estudios.


## Creación de KPIs y métricas clave
Proponemos, medimos y graficamos los siguientes KPIs (Key Performance Indicators):

### El Ministerio de Seguridad de la Nación se propuso reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/blob/main/imagenes/poblacion_semestral%201.png)

La variación porcentual de la tasa de homicidios viales disminuyó considerablemente en el último semestre analizado, presentando una reducción del -24.02% (la tasa pasó de 1.79 a 1.36). Si bien esto indica que se ha logrado un avance significativo al reducir esta tasa y acercarse al objetivo, es importante destacar que aún es necesario continuar trabajando para mejorar la cifra de fallecidos en siniestros viales. Recordemos que detrás de cada número estadístico hay vidas humanas y familias afectadas, en este caso, 42 familias que han sufrido pérdidas.

### Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior
Este objetivo es de suma importancia, dado que casi la mitad de las víctimas fatales de los siniestros viales son motociclistas.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/blob/main/imagenes/poblacion_anual%201.png)

En el año 2021, se observó un incremento en la tasa de homicidios viales en motociclistas del 19.77%, con la tasa anual pasando de 0.94 a 1.49. Como recomendación para alcanzar este objetivo, que ha sido mencionado previamente, se pueden llevar a cabo programas de concientización vial dirigidos específicamente a los motociclistas, además de intensificar la supervisión del uso de equipos de seguridad, como el casco.

### Reducir la tasa anual de homicidios viales en las avenidas en un 20% con respecto al año anterior.
Este objetivo se establece en función de la sección 2, ya que al explorar la ubicación de los homicidios en relación con la comuna y el tipo de calle, se identificó que las avenidas son los lugares donde ocurren con mayor frecuencia los siniestros viales fatales.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/blob/main/imagenes/poblacion_anual%202.png) 

En los últimos años, la tasa de homicidios viales en las avenidas ha experimentado fluctuaciones significativas, y lamentablemente, no se logró cumplir con el objetivo el año pasado. Sin embargo, con un aumento en la presencia de las autoridades viales en las avenidas, se espera reducir esta tasa de manera efectiva.

## 4. Análisis Espacial
### Localización de áreas geográficas con una alta incidencia de siniestros viales y posiblemente de víctimas fatales.
La identificación de las ubicaciones donde ocurre la mayoría de los siniestros viales es esencial para una asignación eficiente de recursos por parte de las autoridades. Esto les permite concentrar sus esfuerzos y recursos, como oficiales de tráfico, ambulancias y servicios de emergencia, en las áreas de mayor riesgo. Como resultado, se puede proporcionar una respuesta más rápida y efectiva en caso de accidentes, lo que puede marcar la diferencia en la atención a las víctimas y la prevención de lesiones graves o fatales. Esta estrategia contribuye a mejorar la seguridad vial y a reducir el impacto de los siniestros viales en la comunidad.

![Image text](https://github.com/Valentina-PadillaB/Siniestros_data_analyst/blob/d48e2d3ae80a5e504060f7fec08bcde26afc252e/imagenes/mapa_homicides_and_injuries.pjeg)

El mapa resalta la importancia de tomar medidas específicas en la Avenida General Paz debido a la alta tasa de siniestros viales en esa área. Para abordar esta problemática, se sugiere la instalación de cámaras de control de velocidad a lo largo de la avenida. Estas cámaras pueden ayudar a monitorear el cumplimiento de los límites de velocidad y detectar conductas de conducción peligrosas. Además, se recomienda aumentar la presencia policial en la zona para mejorar la supervisión y la aplicación de las normas de tráfico. Estas acciones combinadas pueden contribuir significativamente a reducir la incidencia de siniestros viales y a mejorar la seguridad en la Avenida General Paz y sus alrededores.

## 6. Conclusiones y sugerencias:

Este proyecto de análisis de datos se presenta como una herramienta valiosa para contribuir a la mejora de la seguridad vial en la Ciudad de Buenos Aires. Los resultados obtenidos ofrecen una base sólida para la implementación de políticas públicas y acciones concretas que apunten a la reducción de víctimas fatales en siniestros viales, protegiendo la vida de los ciudadanos.

A partir del análisis realizado, se proponen las siguientes medidas:

* 1. Fortalecimiento de las capacitaciones:

Continuidad y periodicidad: Mantener las capacitaciones segmentadas por edades, brindándolas al menos una vez al año a toda la comunidad.
Ampliación del enfoque: Incluir en las capacitaciones información sobre la importancia del buen descanso para prevenir siniestros viales por somnolencia, especialmente en las primeras horas del día.

* 2. Refuerzo del control y la vigilancia:

Incrementar la presencia policial: Priorizar la Comuna 1, con mayor concentración de siniestros viales, y aumentar la presencia de autoridades viales en las horas pico para garantizar un flujo vehicular seguro.

* 3. Inversión en infraestructura:

Destinar recursos a la mejora de la infraestructura vial: Implementar mejoras en las avenidas de todas las comunas.

* 4. Implementación de tecnología:

Utilizar herramientas tecnológicas: Instalar cámaras o detectores de velocidad en zonas estratégicas para el control del tránsito.

* 5. Foco en motociclistas:

Capacitaciones específicas: Implementar programas de formación en seguridad vial especialmente dirigidos a motociclistas.
Control del uso del casco: Intensificar el control y, en caso necesario, aplicar multas por no llevarlo correctamente.

* 6. Recopilación y análisis de datos:

Fortalecimiento de las entidades: Mejorar las capacidades de las entidades encargadas de la recopilación de datos o crear un grupo especializado en siniestros viales.
Monitoreo constante: Mantener una vigilancia permanente del comportamiento de los conductores en la Avenida General Paz.
La implementación de estas medidas, junto con un compromiso sostenido por parte de todos los actores viales, permitirá avanzar hacia un tránsito más seguro y responsable en la Ciudad de Buenos Aires.

   En resumen, para reducir la tasa de homicidios viales en las avenidas, es necesario implementar un enfoque integral que combine medidas de concientización, seguridad vial, prevención del delito y sanciones más severas. Estas medidas podrían generar un impacto significativo en la reducción de la tasa de homicidios viales en las avenidas y mejorar la seguridad vial en general.


## Repositorio de GitHub
El repositorio de este proyecto contiene un archivo Jupyter Notebook con el análisis de datos y visualizaciones, un archivo de datos sobre homicidios en siniestros viales y otro sobre lesiones en siniestros viales, y un archivo README principal donde presentamos, en una primera instancia, de forma general nuestro proyecto y detallamos qué hay en cada archivo/carpeta del propio repositorio.




