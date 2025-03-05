# Planeación del Proyecto

El desarrollo del proyecto fue llevado a cabo de acuerdo a la planificación de actividades previstas, durante las primeras semanas. Se implementó el modelo *PM4R* del *BID (Banco Intermediario de Desarrollo)*, el cual consiste de 7 pasos clave ([7 Steps to Obtain Results in Projects](http://www.pm4rglobal.org/steps.html?lang=en)).

## Alcance

Es fundamental conocer los objetivos del proyecto junto con los entregables específicos del mismo. A continuación, se listan los entregables principales tenidos en cuenta para la generación del listado de actividades:

- Gestión de Producción y Automatización
	- Simulación de la planta con el software Siemens Tecnomatix Plant Simulation
	- Diagramas VSM
	- Propuesta de integración de sistema MES
- Industria 4.0 en la Automatización
	- Diagramas P&ID, identificando sensores y actuadores en cada etapa
	- Diagrama de la Arquitectura de Control
	- Listado de tecnologías de la industria 4.0 implementadas en el proyecto
- Evaluación Económica
	- Memoria de cálculo con el flujo de caja
	- Memoria de cálculo con los indicadores: VPN, TIR y Payback
- Celda de Manufactura Robotizada
	- Análisis de implementación de celda robotizada en alguno de los procesos
	- Simulación de celda robotizada en el software RobotStudio
	- Identificación de peligros y gestión del riesgo
	- Medidas para prevención de riesgos
- Digital Factory
	- Simulación de la planta con el software Siemens NX
- Controladores Industriales
	- GRAFCET del proceso
	- LADDER al estilo GRAFCET del proceso
- SCADA
	- HMI del sistema

De acuerdo a los entregables principales listados anteriormente, se desglosa cada uno de ellos en subactividades. Por consiguiente, se hace uso de la herramienta *Estructura Desglosada de Trabajo (EDT)*, la cual ilustra en forma de diagrama la jerarquía de actividades que contiene el proyecto.

A la cabeza del diagrama se encuentra el nombre del proyecto, de aquí se desprenden los entregables principales, los cuales, se desglosan en actividades más pequeñas.

![Pasted image 20250303224016.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304212630.png)

Se muestra a continuación, la vista global del EDT, se abordará cada subsección individualmente.

![Pasted image 20250303232441.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303232441.png)


### Acciones Preliminares

Se plantea en las primeras semanas la identidad del grupo, así como los productos a ser fabricados. 

![Pasted image 20250303224318.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303224318.png)

Los productos son seleccionados de acuerdo a los parámetros establecidos en las instrucciones del proyecto. Se tuvieron en cuenta aspectos adicionales para la selección de los mismos, los cuales son:

- Relevancia del tipo de juguete en el mercado
- Piezas del mismo material en su mayoría
- No más de una de las piezas por juguete es provista por un tercero
- Se pueden identificar fácilmente todas las piezas presentes en el juguete
- Los juguetes deben poseer preferiblemente información acerca de sus dimensiones

A partir de los juguetes seleccionados, se analizan los materiales, sus partes y las normas de seguridad aplicables a los mismos. Para más información acerca de los productos, dirigirse a la sección [Productos](productos.md).


### Definición de Productos y Procesos

El objetivo principal de esta sección es definir por cada juguete, los siguientes puntos:
- Demanda en el contexto colombiano
- Procesos involucrados
- Maquinaria implementada en los procesos

Se analizan también algunos parámetros para la selección de maquinaria. Se seleccionan ciertas referencias en el mercado, de tal manera que se pueda tener un acercamiento más preciso sobre los costos y características de la maquinaria que influirá en otras actividades del proyecto.

![Pasted image 20250303230714.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303230714.png)

![Pasted image 20250303230745.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303230714.png)

![Pasted image 20250303230822.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303230822.png)


### Organización y Gestión

En esta sección se definen aquellas piezas adicionales en cada juguete que deben ser traidas de proveedores externos, así como también partes y procesos auxiliares.

Se define también el layout de la planta, junto con el número de máquinas en cada etapa.

![Pasted image 20250303232328.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303232328.png)

![Pasted image 20250303232354.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303232354.png)


### Análisis de Manufactura

De acuerdo al layout de la planta concebido en la anterior sección, se organiza y se termina de diseñar el mismo, utilizando herramientas de *Lean Manufacturing* ([Lean Manufacturing](https://www.youtube.com/watch?v=ZT3D0Sj6UY0)).

Se desarrolla en esta sección la simulación de la planta en con *Tecnomatix Plant Simulation*, y se obtienen los parámetros de gestión y producción.

![Pasted image 20250303233352.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303233352.png)

![Pasted image 20250303233455.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303233455.png)

![Pasted image 20250303233513.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303233513.png)

![Pasted image 20250303233541.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303233513.png)


### Análisis Empresarial

Se hace el análisis económico del proyecto, teniendo en cuenta los flujos de entrada y de salida para la generación del flujo de caja. Una vez hecho esto, se determinan los indicadores financieros para determinar la viabilidad del proyecto.

En caso de no considerarse el proyecto como válido, se deben reajustar los flujos de dinero, ya sea seleccionando elementos menos costosos, eliminando gastos, o aumentando el valor de los ingresos.

![Pasted image 20250303234927.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303234927.png)

![Pasted image 20250303234958.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303234958.png)

![Pasted image 20250303235041.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250303235041.png)


### Análisis Industrial

Se genera el gemelo digital que virtualiza la planta, con el software Siemens NX. A partir de esto, se desglosa el problema de control por medio de los lenguajes GRAFCET y LADDER.

![Pasted image 20250304001344.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304001344.png)

![Pasted image 20250304001448.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304001448.png)

![Pasted image 20250304001611.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304001611.png)


### Definición de Escalones altos en la Pirámide de Automatización

El objetivo de esta sección es generar un sistema SCADA donde sea posible supervisar y operar las variables de salida y de entrada, correspondientes a sensores y actuadores respectivamente.

Las variables obtenidas en la función de históricos de los sistemas SCADA, son utilizadas en la industria por los sistemas MES, por lo que se genera una propuesta para llevar a cabo esto.

![Pasted image 20250304001629.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304001629.png)


## Cronograma

De acuerdo a las actividades enunciadas en el *EDT*, se establecen los tiempos de ejecución de cada una de las mismas. Para este objetivo, se utiliza la herramienta de *Diagrama de Gantt*, teniendo en cuenta el desarrollo del curso, de acuerdo a cronograma de actividades propuesto en cada semana.

Se muestra a continuación, nuestro cronograma de actividades:

![Pasted image 20250304003102.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304003102.png)


Se tienen en cuenta las actividades principales, así como también los tiempos de ejecución pertienentes para el desarrollo de cada una de ellas. Las actividades con mayor relevancia, son aquellas de las que dependen otras actividades, por lo que estas deben hacerse en un menor tiempo, ya que, hay actividades que solo pueden comenzar después de estas.

Se alinean también los objetivos de cada semana, de acuerdo a los módulos vistos, con respecto al cronograma del curso.


## Desarrollo de Actividades Iniciales

Con respecto a los productos seleccionados, se identifican sus partes y se determinan materiales. Se selecciona el *acrilonitrilo butadieno estireno (ABS)* como material principal en los juguetes, debido a las siguientes razones:

- **Resistencia al impacto**: Capacidad para soportar golpes y tensiones sin fracturarse, incluso en condiciones de bajas temperaturas.

    
- **Estabilidad dimensional**: Mantiene sus dimensiones y forma bajo condiciones de carga y temperatura variables.
    
    
- **Facilidad de procesamiento**: Puede ser moldeado y mecanizado con facilidad, lo que lo hace adecuado para diversas aplicaciones industriales.
    
- **Resistencia química**: Es resistente a ácidos, álcalis y aceites, aunque puede ser afectado por solventes fuertes como cetonas y esteres.

Se comparan también las propiedades de los materiales utilizados en la industria de juguetes plásticos:

| Propiedad                                  | ABS       | Poliestireno (PS) | Polipropileno (PP)         |
| ------------------------------------------ | --------- | ----------------- | -------------------------- |
| **Módulo elástico en tracción (GPa)**      | 2,0 - 2,9 | 2,0 - 2,5 (HIPS)  | 1,1 - 1,6 (Homopolímero)   |
| **Alargamiento de rotura en tracción (%)** | -         | 20 - 65 (HIPS)    | 100 - 600 (Homopolímero)   |
| **Resistencia a la tracción (MPa)**        | 41 - 45   | 20 - 35 (HIPS)    | 31 - 42 (Homopolímero)     |
| **Módulo de flexión (GPa)**                | -         | 1,6 - 2,9 (HIPS)  | 1,19 - 1,75 (Homopolímero) |
| **Resistencia al impacto Izod (J/m)**      | 200 - 400 | -                 | -                          |
| **Resistencia al impacto Charpy (kJ/m²)**  | -         | 3 - 12 (HIPS)     | 4 - 20 (Homopolímero)      |
| **Dureza Shore D**                         | -         | 60 - 75 (HIPS)    | 72 - 74 (Homopolímero)     |

Referencias:
- [Guía de materiales plásticos en juguetes](https://www.demengtoy.com/es/guide-to-plastic-materials-used-in-toy-manufacturing.html)
- [ABS en Wikipedia](https://es.wikipedia.org/wiki/Acrilonitrilo_butadieno_estireno)
- [Poliestireno en Wikipedia](https://es.wikipedia.org/wiki/Poliestireno)
- [Polipropileno en Wikipedia](https://es.wikipedia.org/wiki/Polipropileno)

Se concluye que el ABS es la mejor opcion, de acuerdo a la aplicación de nuestros productos. Estos no serán sometidos a cargas grandes.

Teniendo en cuenta los colores de los juguetes, se identifican los colores de los pellets de ABS a ser utilizados:

- Amarillo
- Negro
- Blanco
- Azul Claro
- Verde Claro
- Verde Oscuro

Ahora bien, cada juguete posee elementos adicionales que deben ser traidos de proveedores externos. Por cada juguete, se enuncian estas piezas:

| Juguete    | Pieza a importar    | Cantidad |
| ---------- | ------------------- | -------- |
| Cargadora  | Neumático de caucho | 4        |
| Avión      | Rueda de caucho     | 2        |
| Dinosaurio | Ojos de juguete     | 2        |
|            | Tornillos M3        | 7        |

Adicionalmente, se necesitan las cajas y los moldes de plástico para la presentación de cada producto. Estos elementos son traídos de proveedores externos.

![Pasted image 20250304125359.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304003102.png)

### Definición de Procesos

Se investiga acerca de los procesos llevados a cabo en los juguetes seleccionados. Identificando etapas y maquinaria.

Se listan a continuación, algunas fuentes que nos sirvieron para determinar los procesos llevados a cabo en nuestro proyecto:

- [Inyección de caucho](https://www.youtube.com/watch?v=8scL3w9Osho)
- [CAM - CAD Design | Plastic toys making](http://www.youtube.com/watch?v=SnOWAwA6oFc)
- [Inside the Toy Factory : The Making of Plastic Toys Cars](https://www.youtube.com/watch?v=78InBA02KfQ)
- [Injection Moulding Machine Tending with JAKA Zu 12](https://www.youtube.com/watch?v=rA9lx6keugY)
- [DESVIADOR DE PRODUCTO BANDA TRANSPORTADORA](https://www.youtube.com/watch?v=Qxi1v9tzNAQ)

Se llegó a la conclusión de utilizar las siguientes etapas:

![Pasted image 20250304130414.png](https://github.com/alejo9812/APM_Fabrica_de_Juguetes/blob/main/Images/Pasted%20image%2020250304130414.png)

A partir de esto, se construye el layout de la planta, donde se definen los siguientes puntos:
- Maquinaria específica (referencias)
- Número de estaciones por etapa
- Organización de las estaciones
- Dimensiones del local
- Elementos de conexión entre estaciones


**Ver siguiente sección:** [Gestión de Producción y Automatización](gestion.md)







