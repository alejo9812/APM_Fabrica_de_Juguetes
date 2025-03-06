# Simulación de la Fábrica Digital

Haciendo uso del software *Siemens NX Mechatronics Concept Design*, se virtualiza parte de la planta propuesta.

Se hace un enfoque en la primera parte del proceso de automatización, donde entran pellest a la inyectora y de esta sale una pieza que contiene distintas piezas dependiendo del juguete. E transporte de las piezas es hecho por medio de un manipulador serial de 6 grados de libertad, que se encarga de sacar la piea de la inyectora y ponerla sobre la superficie de trabajo de la cortadora. Una vez que la cortadora termina de recortar la pieza, se obtiene las piezas individuales correspondientes. El manipulador serial toma estas pieszas y las posiciona en una banda transportadora.

No obstante, por motivos de tiempo, no se implementa el manipulador serial en la simulación.

![[WhatsApp Bild 2025-03-02 um 09.55.06_9097e786.jpg]]

Como se puede ver en la imagen, la inyectora se encuentra al inicio de la línea de manufactura, de aquí salen las piezas que pasan luego a la estación de corte. De aquí

![[Pasted image 20250306001405.png]]




**Ver siguiente sección:** [Implementación de Controladores Industriales](plcs.md)

