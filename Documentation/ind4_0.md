# Industria 4.0 en Nuestro Proyecto

## Diagramas de Instrumentación

Se realiza el diagrama *P&ID* de la celda robotizada.

![[Pasted image 20250306005800.png]]

![[Pasted image 20250306005924.png]]


## Arquitectura de Control

![[Pasted image 20250306004502.png]]

![[Pasted image 20250306010018.png]]

## Gemelo Digital (Modelo Ciberfísico)

Se implementa el modelo de la planta en *Siemens NX Mechatronics Concept Design*. Allí  se simula el proceso y se puede visualizar en tiempo real, el estado de sensores y actuadores, además de poder determinar cómo funcionaría la planta si se implementara en la realidad

El gemelo digital permite simular, monitorear y analizar los procesos de producción en tiempo real, visualizando cómo funcionan las máquinas, líneas de ensamblaje y otros componentes sin necesidad de intervenir físicamente.

Ayuda a prever posibles fallas o cuellos de botella en la producción, lo que permite tomar decisiones proactivas y ajustar el proceso antes de que ocurran problemas.

Analizar el desempeño de las máquinas y los procesos para mejorar la calidad del producto final.

Mediante el análisis de datos históricos y en tiempo real, se pueden predecir fallas y planificar el mantenimiento predictivo, lo que reduce el tiempo de inactividad y los costos operativos.

## Uso de IoT (Internet de las Cosas)

El **Internet de las Cosas (IoT)** hace referencia a la interconexión de dispositivos físicos (sensores, actuadores, PLCs, máquinas) que están conectados a través de redes, generando y transmitiendo datos en tiempo real a sistemas de monitoreo, análisis y control.

Los dispositivos IoT pueden enviar información sobre el estado de las máquinas, niveles de inventarios, consumo energético, entre otros, directamente al sistema centralizado, facilitando el monitoreo remoto.

Permite que las máquinas y los equipos tomen decisiones autónomas basadas en datos en tiempo real, optimizando los procesos de producción sin intervención humana.

El IoT mejora la trazabilidad en la cadena de suministro, permitiendo el seguimiento de materiales desde su entrada en la planta hasta la producción final del juguete.

Los dispositivos IoT proporcionan grandes volúmenes de datos que pueden analizarse para obtener insights sobre la eficiencia de la producción y otros parámetros operativos.


### Recolección y Análisis de Datos de IoT, Sensores y Actuadores para Analizar Indicadores Financieros

La **recolección de datos** es uno de los aspectos más importantes en la automatización industrial. Los dispositivos IoT, sensores y actuadores instalados en las máquinas y equipos recolectan datos continuamente sobre diferentes parámetros de la producción, tales como:

- **Tiempo de operación**: Tiempo durante el cual las máquinas están activas y en funcionamiento.
- **Eficiencia de la máquina**: Datos sobre la velocidad de las máquinas y el rendimiento respecto a la capacidad máxima.
- **Consumo energético**: Información sobre el uso de energía por máquina o línea de producción.
- **Calidad del producto**: Medición de defectos, variabilidad y errores de fabricación.
- **Estado de los equipos**: Datos de condición, temperaturas, presiones y otros indicadores clave.

Una vez que los datos son recolectados a través de los dispositivos IoT, es fundamental procesarlos para extraer **indicadores financieros** y operativos que ayuden en la toma de decisiones estratégicas. Estos indicadores pueden incluir:

- **Costo por unidad de producción**: Calculando el costo total (incluyendo materiales, energía, y tiempo de máquina) y dividiéndolo entre las unidades producidas.
- **Rentabilidad**: Relacionando los costos de producción con los ingresos generados por la venta de los juguetes.
- **ROI (Retorno sobre la inversión)**: Medición del retorno de las inversiones realizadas en equipos automatizados, comparando los ahorros y la mejora en la eficiencia con los costos de implementación.
- **Tiempos de inactividad**: Cuantificación de los tiempos que las máquinas no están operativas, lo que impacta directamente en la productividad y los costos.
- **Optimización de inventarios**: Usando los datos de sensores de inventario para reducir los costos asociados al exceso o escasez de materiales.


### Implementación de Sistemas de Información Seguros, con Aspectos de Ciberseguridad y Protección de Datos


En una planta automatizada que utiliza tecnologías como el IoT y el Gemelo Digital, la **ciberseguridad** se vuelve crucial, ya que los sistemas están interconectados a través de redes industriales y conectividad a Internet. Los principales desafíos de ciberseguridad incluyen:

- **Accesos no autorizados**: La posibilidad de que actores maliciosos accedan a los sistemas de control y manipulen la producción o los datos.
- **Ataques a los dispositivos IoT**: Los sensores y actuadores pueden ser vulnerables a ataques que interfieran con la transmisión de datos o manipulen su funcionamiento.
- **Riesgos de manipulación de datos**: La alteración de los datos recopilados por los sistemas de monitoreo podría generar decisiones incorrectas y afectar la calidad del producto.

Para garantizar la **protección de los datos** y la seguridad del sistema, es fundamental implementar las siguientes medidas:

- **Autenticación y Control de Accesos**: Establecer protocolos estrictos de autenticación, como autenticación de múltiples factores, para controlar el acceso a los sistemas de información y redes industriales.
- **Cifrado de Datos**: Asegurar que los datos transmitidos desde los dispositivos IoT, sensores y sistemas de control estén cifrados para evitar interceptaciones maliciosas.
- **Firewalls y Sistemas de Detección de Intrusos (IDS)**: Utilizar firewalls industriales y sistemas IDS para monitorear y bloquear accesos no autorizados o comportamientos sospechosos en las redes de la planta.
- **Mantenimiento y Actualización de Software**: Realizar actualizaciones periódicas de los sistemas de software, especialmente en dispositivos IoT y sistemas SCADA, para protegerlos contra vulnerabilidades conocidas.
- **Segmentación de Redes**: Segmentar las redes industriales y administrativas para minimizar el riesgo de propagación de ataques cibernéticos a través de los sistemas conectados.


Con respecto a la protección y recuperación de datos, se tienen los siguientes puntos:

- **Cumplimiento con Normativas**: Asegurar que el sistema de información cumpla con las normativas internacionales de protección de datos, como la GDPR (Reglamento General de Protección de Datos) en Europa o la CCPA (California Consumer Privacy Act) en Estados Unidos.
- **Respaldo y Recuperación de Datos**: Implementar políticas de respaldo de datos regulares y establecer procedimientos de recuperación ante desastres para garantizar la disponibilidad y la integridad de los datos en caso de un incidente cibernético.


**Ver siguiente sección:** [Evaluación Económica del Proyecto](eva_economica.md)
