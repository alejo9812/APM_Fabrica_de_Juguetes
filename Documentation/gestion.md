# Gestión de Producción y Automatización

Se utiliza el software *Siemens Tecnomatix Plant Simulation* con la finalidad de hacer un análisis sobre el sistema de producción y simular la planta, teniendo en cuenta tiempos de proceso, porcentajes de falla, tiempos de mantenimiento y balance de líneas. Esto nos permite también generar una distribución adecuada y definir el número de estaciones por etapa.

La plant a puede organizarse por sectores de acuerdo al tipo de producto o al tipo de proceso. Inicialmente se genera un layout dividido de acuerdo al tipo de producto, generando los 3 productos simultáneamente.

El layout va siendo modificado a medida que se tienen en cuenta otros aspectos como la evaluación económica, metodología de *Lean Manufaturing* y tiempos de proceso.

>[!Atención]
>Los dos layouts mostrados a continuación no son los layouts definitivos. Estos son prototipos iniciales que se exponen con la finalidad de mostrar el proceso que se hizo antes de llegar a una conclusión.
>
>El layout definitivo se encuentra en la sección: [Layout de la Planta](#Layout+de+la+Planta)


A continuación, se muestra la primera propuesta del layout de la planta. Su objetivo es generar un acercamiento a modo de prototipo inicial, donde se identifiquen las etapas mencionadas en la sección [Planeación](planeacion.md).

![image](https://github.com/user-attachments/assets/544e03e3-5eb5-49e3-b2ab-0add64ff4d5a)

![image](https://github.com/user-attachments/assets/a7515bfc-e0dd-4925-9b5d-414a9fdf6794)

Por tanto, en este primer layout no se ha definido aún exactamente el número de estaciones por etapa, la distribución y lo tiempos. Es un modelo lineal que únicamente ilustra cada etapa.

Reorganizando el layout anterior utilizando una distribución en U, se obtuvo lo siguiente:

![image](https://github.com/user-attachments/assets/ca6fa91a-341e-4916-8b3c-5d0056bb76b2)

Se organizan también las estaciones de ensamble manual:

![image](https://github.com/user-attachments/assets/d3fe73c5-edd3-4ee3-bbb2-bd274cbc65f5)

### Layout de la Planta

Se tienen en cuenta ahora los aspectos económicos como la demanda y el presupuesto establecido para el proyecto (ver sección [Evaluación Económica](eva_economica.md)).

Los principales problemas de los layouts propuestos anteriormente son los siguientes:
- Número de estaciones inadecuado de acuerdo a la demanda
- Tiempos de transporte muy altos
- Distribución poco adecuada con respecto a la cercanía de estaciones
- Sistema poco flexible y adaptable a nuevos productos
- Dificultad para implementar un plan de producción adecuado

Teniendo en cuenta estos criterios, se reevalúa la distribución de la planta, y se modifica para mejorar en estos aspectos.

Se muestra a continuación, el layout definitivo de la planta:

![image](https://github.com/user-attachments/assets/022145c8-a549-4581-a300-6a804b00c4aa)

![image](https://github.com/user-attachments/assets/ce706f8c-8019-4de2-abca-c4ad149a8a27)

Se ha organizado la planta teniendo en cuenta estrategias de *Lean Manufacturing*, las cuales se evidencian en la distribución, de la siguiente manera:
- *Metodología Just In Time (JIT)* : Se eliminan almacenes a la salida
- *Metodología Pokayoke* : Organización del espacio de trabajo en la sección de ensamble, para evitar errores humanos
- *Metodología 5 S's* : Distribución de la planta de manera ordenada, asegurando el orden y la limpieza
- *Metodología Single Minute Exchange of Die (SMED)* : Las estaciones de ensamble disponen de un orden adecuado, de tal manera que sea fácil para el trabajador cambiar las herramientas
- *Sistema de Manufactura Flexible (FMS)* : El sistema se adapta al tipo de producto en vez de hacer que el producto se adapte a la planta

Siendo así, se listan las ventajas de la distribución de la planta:
- Número de estaciones adecuado a la demanda y balanceado con respecto a todas las etapas
- El sistema cuenta ahora con un alto grado de flexibilidad, de tal manera que las máquinas se encuentran dedicadas al tipo de juguete que se requiera producir
- Sistema de almacenamiento *Warehouse Mangement System (WMS)*, se genera un espacio de almacenamiento de materia prima a medida que esta llega a la planta. Esto permite una mejor organización de los insumos y permite tener un registro del inventario
- Distribución en forma de U
- Máquinas cercanas entre sí
- Procesos contiguos de acuerdo a la secuencia
- Primera estación cercana a la última
- El sistema se adapta a la capacidad de producción
- Respuesta inmediata a fallos

Se muestran a continuación, imágenes de la planta para dar a entender mejor su distribución:

![image](https://github.com/user-attachments/assets/be773f7d-d5ce-41e4-bcb0-05ae8122cd07)

![image](https://github.com/user-attachments/assets/f5f24b85-6fc5-4b28-b5b1-ae75b5ba42dd)

![image](https://github.com/user-attachments/assets/d4f6025d-778a-423a-92b1-23dc96f1e6ef)

![image](https://github.com/user-attachments/assets/38525d0b-5b41-4f8f-8c79-625a9a8fcc4e)

![image](https://github.com/user-attachments/assets/a085ddac-e535-472d-9c3a-36100257d72b)

El layout de la planta sigue la siguiente estructura:

![image](https://github.com/user-attachments/assets/91dcd716-057c-4b30-ba1a-dabc3e5b185b)

Para la definición del número de estaciones, se tuvieron en cuenta los siguientes aspectos:
- Demanda requerida mensualmente ([Evaluación Económica](eva_economica.md))
- Balance de líneas
- Tiempos de proceso

Para los tiempos de proceso, se tiene en cuenta los tiempos estimados de cada máquina (ver sección [Selección de Maquinaria](#Selección+de+Maquinaria)). Se investiga sobre los tiempos de inactividad y se toman tiempos de transporte de la simulación.

A continuación, se enuncian los tiempos tenidos en cuenta:

| Número de Proceso | Proceso              | To [s] | Th [s] | Tth [s] | Tt [s] | Tno [s] | Tc [s] | TBF [h] | TTM [h] | A (%) |
| ----------------- | -------------------- | ------ | ------ | ------- | ------ | ------- | ------ | ------- | ------- | ----- |
| 1                 | Inyectora            | 30     | 2      | 0       | 1      | 1       | 34     | 2,880   | 6       | 98.0% |
| 2                 | Cortadora de Molde   | 4      | 2      | 0       | 5      | 2       | 13     | 2,880   | 2       | 99.0% |
| 3                 | Pulidora Superficial | 45     | 0      | 0       | 5      | 1       | 51     | 1,920   | 8       | 99.9% |
| 4                 | Ensamblaje           | 60     | 2      | 3       | 5      | 5       | 75     | 8,640   | 6       | 98.0% |
| 5                 | Empaque              | 5      | 2      | 0       | 3      | 1       | 11     | 2,880   | 4       | 99.5% |
| 6                 | Embalaje             | 0      | 5      | 0       | 3      | 2       | 10     | 250     | 1       | 99.5% |

Teniendo en cuenta que la demanda es de 5000 juguetes al mes, se tiene una producción anual de alrededor de 60.000 unidades. Esto sugiere que la empresa se puede clasificar como una compañía pequeña, de acuerdo a las clasificaciones empresariales del DANE y el Ministerio de Comercio, Industria y Turismo de Colombia.

En la simulación se tienen en cuenta todas las piezas de los juguetes, así como también su cantidad. Se establecen estos parámetros en las estaciones de ensamble, de acuerdo al tipo de producto. Se muestra a continuación, la tabla en *Tecnomatix* donde se guardan estos parámetros.

![image](https://github.com/user-attachments/assets/44563272-2329-4d6b-b9da-3d0c1f2b65d3)

El modelo de la planta propone un enfoque flexible, por lo que el sistema se adapta al tipo de producto y a la capacidad de producción. Se expone a continuación, la tabla en el software de simulación, donde se define el plan de producción con respecto a los insumos necesarios para lograr la demanda requerida mensual.

![image](https://github.com/user-attachments/assets/25aa886f-88bc-4af6-a519-e09bae5dc078)

Se tiene en cuenta que cada paquete de pellets, produce un producto a la salida de la inyectora. Los elementos que salen de esta, se componen de más piezas dependiendo del tipo de producto ( ver piezas de salida de la inyectora en la sección [Selección de Maquinaria](#Selección+de+Maquinaria)).

Debido a que la única estación en la que intervienen trabajadores de manera directa es la estación de ensamblaje, se analiza sobre el número de trabajadores necesarios para lograr este volumen de producción en una jornada de 8 horas y 5 días a la semana. Se investiga sobre el tiempo que le puede tomar a un trabajador ensamblar un juguete como los que se manejan en la planta.

Se concluye que para juguetes de complejidad media (entre 5 y 20 piezas), el tiempo estimado es de 75 segundos ([Análisis de operaciones en el ensamble de un carrito de juguete](https://de.slideshare.net/slideshow/anlisis-de-operaciones-en-el-ensamble-de-un-carrito-de-juguete-autobs/238835193?utm_source=chatgpt.com#2)).

 Se establecen 2 trabajadores en la parte de ensamble, lo que es más que suficiente para garantizar que se cumpla con la demanda diaria.

Se obtiene la siguiente distribución de cargas en las estaciones:

![image](https://github.com/user-attachments/assets/9aace369-4669-42bf-9d7c-059d267db435)

En la sección de ensamblaje se puede evidenciar una mayor carga, esto tiene sentido debido a que las operaciones son manuales y toman un mayor tiempo con respecto a las otras etapas, a su vez, se asignan porcentajes de falla más altos en estas estaciones, por lo que un humano es más propenso a presentar fallas en la manufactura, que una máquina.

Los tiempos de no operación en la inyectora y la cortadora, se deben al tiempo en el que el robot se tarda en llevar los elementos entre estas estaciones, por ello, se puede ver en la gráfica tiempos de bloqueo en las dos etapas anteriormente mencionadas.

Se asignaron porcentajes de falla bajos a las pulidoras, a la máquina de empaque y a la etapa de embalaje.

El diagrama VSM de la planta es el siguiente:

![[Pasted image 20250306004016.png]]


## Propuesta para llevar la información de la planta a un sistema MES

Las variables obtenidas de la parte baja de la pirámide, son supervisadas y recolectadas en los históricos del sistema SCADA. No obstante, con la finalidad de tomar decisiones financieras a partir de estos datos, es necesario integrar un sistema *Manufacturing Execution System (MES)*.

### 1. **Recopilación de Datos de la Planta**

- **Sensores y Dispositivos IoT**: Instalar sensores en la maquinaria y equipos de producción para monitorear variables clave como temperatura, velocidad, presión, ciclos de máquina, entre otros. Estos sensores pueden estar conectados a dispositivos IoT (Internet of Things) para la recopilación en tiempo real.
- **Controladores Lógicos Programables (PLC)**: Utilizar PLCs para controlar y monitorear las máquinas de la planta. Los PLCs pueden generar señales de estado, alarmas, y datos operativos que son fundamentales para la gestión del proceso.
- **SCADA (Supervisory Control and Data Acquisition)**: Integrar un sistema SCADA que recoja y visualice datos de los PLCs, controladores y otros equipos automatizados. SCADA también puede procesar y almacenar datos históricos.

### 2. **Conectividad y Transmisión de Datos**

- **Protocolos de Comunicación Industrial**: Utilizar protocolos de comunicación como OPC-UA (Open Platform Communications Unified Architecture), MQTT (Message Queuing Telemetry Transport), o Modbus TCP/IP para transmitir los datos entre los dispositivos de la planta (sensores, PLCs, etc.) y el sistema MES.
- **Redes Industriales**: Implementar una red industrial segura, como Ethernet Industrial, para garantizar la transmisión eficiente y segura de los datos desde la planta hacia el sistema MES.

### 3. **Integración con el Sistema MES**

- **Interfaz de Integración MES-PLC**: Configurar una interfaz de integración entre los PLCs y el sistema MES que pueda recibir y procesar datos en tiempo real. El MES debe estar preparado para recibir variables de producción, estado de las máquinas, cantidades producidas, tiempos de ciclo, entre otros.
- **Base de Datos Centralizada**: El sistema MES debe estar vinculado a una base de datos centralizada donde se almacenen todos los datos históricos, los registros de producción, las órdenes de trabajo, y las variables de proceso. Esto facilita la trazabilidad y el análisis posterior.
- **APIs para Interoperabilidad**: Desarrollar o utilizar APIs (interfaces de programación de aplicaciones) para permitir la interoperabilidad entre diferentes sistemas (como el ERP, SCADA y MES). Esto facilitará la actualización de información entre el sistema MES y otros sistemas como ERP (Enterprise Resource Planning) para la gestión de inventarios, pedidos y programación.

### 4. **Visualización y Monitoreo**

- **Paneles de Control en Tiempo Real**: Implementar paneles de control en tiempo real en el sistema MES, donde se muestren indicadores clave de desempeño (KPIs) como eficiencia de la máquina, tiempo de inactividad, tasa de producción, calidad, etc.
- **Alertas y Notificaciones**: Configurar alertas y notificaciones automáticas cuando ciertos parámetros de producción no se cumplan o cuando se detecten fallas o desvíos en el proceso. Esto permitirá a los operadores intervenir rápidamente.
- **Historial de Datos**: El sistema MES debe permitir la consulta y análisis de los datos históricos para mejorar la toma de decisiones y realizar mantenimiento predictivo.

### 5. **Trazabilidad y Reportes**

- **Seguimiento de Lotes y Productos**: El MES debe ser capaz de rastrear el flujo de materiales y productos en la planta, desde la materia prima hasta el producto final. Esto permite una trazabilidad completa y mejora la gestión de la calidad.
- **Reportes Automáticos**: Configurar reportes automáticos que se generen al final de cada turno o al completar un lote de producción. Estos reportes pueden incluir datos de eficiencia, calidad, utilización de recursos, etc.

### 6. **Mantenimiento Predictivo**

- **Análisis de Datos**: Usar los datos recolectados por los dispositivos IoT y sensores para realizar análisis predictivos sobre el estado de las máquinas. Implementar algoritmos de aprendizaje automático (Machine Learning) para predecir posibles fallas en la maquinaria y programar mantenimientos preventivos, reduciendo tiempos de inactividad.

### 7. **Seguridad y Cumplimiento**

- **Ciberseguridad**: Implementar medidas de ciberseguridad para proteger la infraestructura de la planta automatizada y el sistema MES de ataques cibernéticos. Esto incluye el uso de firewalls industriales, VPNs (Redes Privadas Virtuales), y autenticación de usuarios.
- **Cumplimiento Normativo**: Asegurar que el sistema MES cumpla con las normativas de calidad y seguridad, como ISO 9001, y que permita generar los reportes necesarios para auditorías y certificaciones.


## Parámetros de Manufactura

Se establecen los siguientes parámetros de producción:

- **Demanda requerida:** 5000 unidades/mes
- **Número de turnos:** 1 turno de 8 horas
- **Turnos a la semana:** 5

Por tanto, la demanda diaria establecida es:

$$
\begin{align*}
	D_{d} &= \frac{D_{m}}{d_{m}} \\\\
	&= \frac{5000}{20} = 250\,\,unidades/día
\end{align*}
$$

Donde $D_m$ es la demanda mensual y $d_m$ es el número de días trabajados al mes.

Se deben producir $31,5$ juguetes por hora.

| Variable | Descripción                     | Valor        |
| -------- | ------------------------------- | ------------ |
| **Tsu**  | Tiempo de alistamiento          | 5 min        |
| **Tb**   | Tiempo de producción de un lote | 105 min      |
| **Tp**   | Tiempo de producción por unidad | 10,5 min     |
| **Rp**   | Tasa de producción              | 5,714 unit/h |
| **Q**    | Tamaño del lote                 | 10 unit      |

De acuerdo a la demanda diaria y el número de horas por turno, se tiene un *Takt Time* de $115,2$ segundos.

De acuerdo a la simulación, se obtuvo una producción real de 1150 unidades al día. Por tanto, el *KIP* es del $92\%$.

Se estima una capacidad de producción de 1371 unidades a la semana.

De acuerdo a los tiempos útiles de cada máquina antes de efectuar un mantenimiento, y los tiempos de mantenimiento, se obtienen los promedios para cada uno de estos tiempos.

| Variable | Descripción               | Valor   |
| -------- | ------------------------- | ------- |
| **MTBF** | Mean Time Between Failure | 3,242 h |
| **MTTM** | Mean Time To Maintenance  | 5 h     |
| **A**    | Availability              | 99,86 % |

A continuación se listan los parámetros relacionados con el inventario en proceso:

| Parámetro | Descripción                                 | Valor         |
| --------- | ------------------------------------------- | ------------- |
| MLT       | Manufacturing Lead Time                     | 30 min        |
| LT        | Lead Time                                   | 8 horas       |
| CL        | Costumer Lead Time                          | 56 horas      |
| λ         | Tasa de arribo promedio                     | 0.52 unit/min |
| µ         | Tasa de servicio promedio                   | 1.52 unit/min |
| σ         | Desviación estándar del tiempo de serivicio | 0.58          |
| Lq        | Longitud de cola esperada                   | 0.16 unit     |
| ρ         | Factor de utilización                       | 0.34 -        |
| L         | Total de elementos en el sistema            | 0.50 unit     |
| $t_q$     | Tiempo de espera                            | 18,24 s       |
| $t_e$     | Tiempo en la estación                       | 39,474 s      |
| $t_s$     | Tiempo en el sistema                        | 57,714 s      |

| Parámetro          | Descripción                | Valor         |
| ------------------ | -------------------------- | ------------- |
| $T_C$              | Tiempo de ciclo real       | 32 min        |
| $T_E$              | Tiempo de ejecución real   | 1080 min      |
| $V_{RP}$           | Volumen real de producción | 1125 unidades |
| RE                 | Rate of Efficiency         | 0.920         |
| SE                 | Speed Efficiency           | 0.920         |
| PE                 | Performance Efficiency     | 0.846         |
| Salida defectuosos | Salida de defectuosos      | 22.5 unidades |
| Q                  | Quality Rate               | 0.98          |

De acuerdo a lo anterior, se determina el *OEE* de la compañía:

$$
\begin{align*}
	OEE &= A\cdot PE\cdot Q \\\\
	&= (0,9986\cdot 0,846\cdot 0,98) \\\\
	&= 82,832\,\,\%
\end{align*}
$$

	
## Selección de Maquinaria

Se hace una investigación sobre la maquinaria a utilizar en cada etapa, con la finalidad de identificar costos y tiempos de operación en cada estación.

Para la etapa de inyección, se generan los moldes estimados que se obtendría para la generación de las partes de cada juguete. Se tienen en cuenta las características del moldeo por inyección, así como dimensiones estándar para la los moldes. 

| Capacidad de Inyección (g) | Aplicaciones Comunes                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------ |
| 50 - 500 g                 | Piezas pequeñas (componentes pequeños, tapas de botellas)                                  |
| 500 - 2,000 g              | Piezas medianas (carcasas de electrodomésticos, juguetes más grandes, autopartes pequeñas) |
| 2,000 - 5,000 g            | Piezas grandes (cajas plásticas, contenedores, autopartes de tamaño mediano)               |
| 5,000 - 10,000 g           | Piezas de gran tamaño (parachoques de autos, muebles plásticos)                            |
| +10,000 g (10 kg o más)    | Producción especializada (componentes industriales, partes estructurales)                  |

Piezas obtenidas tras la inyección:

- **Cargadora**

![image](https://github.com/user-attachments/assets/a5fec518-7f98-4ab6-9692-bf5e96cc44d0)

![image](https://github.com/user-attachments/assets/f4a5ab7d-cb17-4d07-bd65-a9a46926fdba)

![image](https://github.com/user-attachments/assets/9956d331-f6e3-4703-9457-677bb347fd80)

- **Avión**

![Pasted image 20250304212559](https://github.com/user-attachments/assets/32b0d630-a678-49ee-9fc5-3f5fb6bd2392)

![image](https://github.com/user-attachments/assets/1740793d-12e5-4a96-a1dc-e625a85a80a7)

Con respecto a las dimensiones que toman estas piezas, se selecciona el tamaño de las placas del molde que debe tener la inyectora. Siendo así, se selecciona la inyectora *ARBURG 270 S 250-60*, la cual cuenta con un tamaño de placas de 400 x 400 mm.

Para la etapa de corte, se selecciona una máquina de cortado hidráulico como la que se usa en el siguiente proceso: [Injection Moulding Machine Tending with JAKA Zu 12](https://www.youtube.com/watch?v=rA9lx6keugY)

No se encontró alguna referencia en específico de esta máquina.

Después de la etapa de cortado, las piezas resentan rebabas e impefecciones que deben ser removidas. En la industria, existen varias máquinas para remover este tipo de desechos, estas máquinas estás se utilizan más que todo para piezas metálicas. Sin embargo, una manera de remover estas rebabas, es utilizando una máquina de pulido superficial por vibración ([Equipo de pulido superficial - Vibradora Rectangular](https://www.youtube.com/watch?v=Gmig4ZVl8B0)). Se selecciona la referencia *ZL80* de la línea *Jintaijing Polishing*.

A continuación, se exponen los resultados obtenidos a partir de esta investigación:

| Número de Proceso | Estación                  | Referencia          | Enlace                                                                                                                                                                                                                      | Descripción                                                                        | Proveedor             | Cantidad | Costo Unitario [Divisa Original] | Costo Unitario [COP] | Costo [COP] |
| ----------------- | ------------------------- | ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | --------------------- | -------- | -------------------------------- | -------------------- | ----------- |
| 1                 | Inyección de Plástico ABS | Arburg 270 S 250-60 | [Ver](https://machineryline.com.co/-/venta/maquinas-de-moldeo-por-inyeccion/Arburg/270-S-250-60--24102414483809520200)                                                                                                      | Tamaño de las placas del molde: 400x400 mm<br><br>Dimensiones: 2,9 m x 1 m x 1,8 m | Machineryline         | 1        | €4.900 EUR                       | $21.036.680          | $21.036.680 |
| 2                 | Corte de los Moldes       | -                   | -                                                                                                                                                                                                                           | Dimensiones: 1,2 x 0,5 x 1,4 m                                                     | -                     | 1        | -                                | -                    | -           |
| 3                 | Pulido Superficial        | ZL80                | [Ver](https://www.surface-polish.com/200l-300l-400l-vibratory-finishing-machine_p16.html?_gl=1*1px3uq2*_up*MQ..*_gs*MQ..&gclid=CjwKCAiAk8G9BhA0EiwAOQxmfub3zkYQo8l8CWQ9OHEk8NZLlmuAwTC7K6miw0iCepDrppXJsnyBeBoCNtAQAvD_BwE) | Dimensiones: 0,9m x 0,9m x 0,82                                                    | Jintaijing Polishing  | 2        | $6.500 USD                       | $27.905.800          | $55.811.600 |
| 4                 | Ensamblaje                | N/A                 | N/A                                                                                                                                                                                                                         | Dimensiones: 0,8m x 0,5m x 0,9m                                                    | N/A                   | 2        | €250 EUR                         | $1.073.300           | $0          |
| 5                 | Empaque                   | CES-4035-N          | [Ver](https://mcbrawn.com/encintadoras/carton-erector-ces-4035-n.html)                                                                                                                                                      | Dimensiones: 2m x 1,9m x 1,45m                                                     | Brother USA Machinery | 1        | $12.800 USD                      | $54.952.960          | $54.952.960 |


**Ver siguiente sección:** [Industria 4.0 en Nuestro Proyecto](ind4_0.md)

