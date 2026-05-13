---
layout: default
title: Proceso de manufactura
parent: Proyecto Final
nav_order: 3
---

## 6. Proceso de Manufactura e Implementación

En esta sección se detalla el proceso de fabricación de las piezas de plástico y se explican los resultados de la prueba física que detuvo la construcción de la armadura completa.

### Manufactura Aditiva a Gran Escala

Fabricar las piezas para la armadura requirió planificar un proceso de producción masiva utilizando impresión 3D. En total, imprimir las piezas necesarias para cubrir toda la prenda demandaba más de 609 horas de trabajo continuo de las máquinas.

Para hacer este proceso eficiente, se agruparon múltiples piezas en cada ciclo de impresión. La configuración de las máquinas permitió imprimir lotes de 44 escamas en ciclos de 12 horas, y lotes de 48 bases en ciclos de una hora y media. En el programa de computadora que prepara los archivos para la impresora, se ajustaron las configuraciones de retracción del plástico. Esto se hizo para evitar que quedaran hilos de material sobrante entre las piezas y garantizar que encajaran a la perfección directamente al salir de la máquina, sin necesidad de lijarlas a mano.

### El Prototipo de Validación (Prueba de Estrés)

Antes de intentar armar las 2,000 piezas sobre la prenda final, se construyó un modelo a escala reducida para comprobar que el sistema funcionaba en la vida real.

Para este experimento físico, se utilizó un trozo de tela suelto, sin fijarlo a ninguna estructura de metal. Sobre este trozo de tela se montaron únicamente 35 escamas completas (con sus bases y piezas móviles). Para conectar estas 35 escamas al motor central, fue necesario utilizar 70 hilos en total, ya que cada escama requería dos extremos de hilo para funcionar.

### Reporte Forense del Fallo Mecánico

Al encender el motor para levantar las 35 escamas al mismo tiempo, el sistema se rompió. El fallo no ocurrió en la tela ni en los hilos, sino en el carrete de plástico impreso que estaba conectado al motor.

La explicación física de esta ruptura se debe a la forma en que se fabrican las piezas en 3D. Las impresoras construyen los objetos depositando capas de plástico derretido una sobre otra, de abajo hacia arriba. La unión entre una capa y otra es el punto más débil de cualquier pieza impresa.

Cuando el motor giró, tuvo que aplicar mucha fuerza de torsión para jalar los 70 hilos tensados al mismo tiempo. La pieza de plástico no resistió esta fuerza de giro; el carrete se partió exactamente a lo largo de las líneas horizontales de las capas de impresión. La fuerza requerida por el motor simplemente superó la resistencia física del material.

### Reporte Forense del Ensamblaje

Además de la ruptura del plástico, la prueba física expuso un problema grave en el trabajo manual. El proceso de conectar las 35 escamas al carrete del motor requirió tomar los 70 hilos de pesca, pasarlos por sus canales correspondientes, tensarlos a mano y asegurarlos individualmente aplicando pegamento líquido de secado rápido en las ranuras del carrete.

Este trabajo manual resultó ser un proceso lento, repetitivo y sumamente cansado. Al medir el tiempo y el esfuerzo necesarios para conectar solo 70 hilos, quedó en evidencia que intentar repetir este mismo proceso para los 4,000 hilos que requería la armadura completa era humanamente inviable dentro del tiempo disponible para el proyecto. El ensamblaje manual se convirtió en un obstáculo que impedía la construcción de la pieza a gran escala.
