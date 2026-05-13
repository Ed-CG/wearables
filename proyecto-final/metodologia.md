---
layout: default
title: Metodología de diseño
parent: Proyecto Final
nav_order: 2
---

## 4. Metodología de Diseño y Arquitectura Electrónica

En esta sección se explica cómo se planeó que las piezas se movieran y cómo se unieron los materiales de plástico duro con la tela flexible. Todo este sistema fue diseñado en teoría y planificado detalladamente, aunque, como se mencionó antes, los componentes electrónicos no se compraron ni se instalaron en la pieza física.

### El Sistema de Movimiento

Para lograr que las piezas exteriores se levantaran, se descartó el uso de varillas rígidas que empujaran desde abajo. En su lugar, el diseño funciona mediante fuerza de tracción, es decir, jalando las piezas desde otro punto.

Se diseñó un mecanismo donde motores eléctricos tienen la función de enrollar hilos muy resistentes. Para esto, se seleccionó hilo de pesca trenzado, ya que soporta mucho peso y no se estira cuando se jala. Estos hilos estarían amarrados a las piezas plásticas. Cuando el motor gira, enrolla el hilo, tira de la pieza y hace que esta se levante de su posición original.

### Control del Roce y la Fricción

Tener cientos de hilos moviéndose sobre la tela generaría mucho desgaste y terminaría cortando el material con el paso del tiempo. Para evitar esto, el diseño incluyó tubos delgados hechos de teflón, un plástico que se caracteriza por ser extremadamente liso y resbaladizo.

Los hilos pasan por dentro de estos tubos a lo largo de toda la prenda. Esto asegura que el hilo no toque la tela directamente, eliminando el roce y permitiendo que el movimiento sea fluido y no requiera fuerza extra por parte de los motores.

### Lógica de los Componentes Electrónicos

El orden en que funciona la electrónica se estructuró en cuatro pasos directos y secuenciales:

1. **Detección:** Un sensor electrónico se encarga de detectar los movimientos y la inclinación del cuerpo de la persona que usa la prenda.
2. **Procesamiento:** Una tarjeta electrónica principal recibe la información de este sensor y calcula cuáles motores deben encenderse y en qué momento.
3. **Distribución:** La tarjeta envía la orden a unos controladores de energía. Estos dispositivos abren el paso de la electricidad desde las baterías hacia los motores correctos.
4. **Acción:** Los motores reciben la energía eléctrica, giran, enrollan los hilos y, en consecuencia, levantan las piezas plásticas.

### Unión Físicamente Integrada entre Plástico y Tela

Uno de los retos más grandes de la prenda era fijar 2,000 bases de plástico duro sobre la tela (vinipiel) sin que se cayeran por su propio peso o por los tirones de los hilos. Para resolverlo, no se utilizó ningún tipo de pegamento.

La solución se basó en el uso de calor. La parte trasera de la tela elegida cuenta con una red de hilos de poliéster. Se aplicó calor directamente a las bases de plástico hasta derretir su superficie inferior sobre esta red. El plástico en estado líquido penetró entre los agujeros de los hilos de poliéster. Al enfriarse y volver a ser sólido, el plástico quedó atrapado físicamente entre la tela, creando una unión sumamente fuerte que soporta la tensión de los motores sin despegarse.
