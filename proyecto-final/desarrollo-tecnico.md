---
layout: default
title: Desarrollo Técnico
parent: Proyecto Final
nav_order: 8
---

## Desarrollo Técnico (Iteraciones en CAD y Simulaciones)

En esta fase se detalla cómo los modelos 3D fueron modificados en la computadora antes de ser impresos. El diseño requirió ajustes de medidas para asegurar que las piezas encajaran bien y se movieran correctamente sin atorarse.

### Evolución de la Base (Clip Pivote)

La pieza que se fija a la tela, llamada clip pivote, pasó por tres versiones de diseño en la computadora. Es importante señalar que las primeras versiones nunca se rompieron ni fallaron estructuralmente; los cambios se hicieron únicamente para mejorar el funcionamiento y el movimiento.

Las modificaciones principales fueron tres:

1. **Altura del punto de giro:** Se ajustó la altura a la que la pieza móvil gira en relación con la superficie de la tela. Esto garantizó que las piezas no rasparan ni chocaran con el material al moverse.
2. **Ajuste de medidas para el movimiento:** Se modificaron los espacios exactos en la zona donde las dos piezas se unen a presión. El objetivo fue evitar que la unión quedara muy apretada, logrando un movimiento mucho más fluido y suave.
3. **Cambio en el método de sujeción:** Como se explicó en la sección anterior, el diseño original tenía ranuras pensadas para coser la pieza con hilo. En la versión final, estas ranuras se eliminaron para dejar una base sólida que pudiera fundirse y unirse con calor directamente a la tela.

### Evolución de la Pieza Móvil (Escama Bisagra)

De manera similar, la pieza que se levanta (la escama) pasó por dos versiones. Los cambios en el diseño por computadora consistieron en ajustar los espacios libres en la zona de la bisagra y en el área de unión a presión. Estos ajustes se hicieron para que coincidieran con las mejoras de la base, asegurando que ambas piezas encajaran perfectamente y trabajaran en conjunto sin fricción.

### Diseño del Carrete para los Hilos

Para lograr que los motores jalaran los hilos de pesca de manera ordenada, se diseñó un carrete (también conocido como spool). La forma de esta pieza incluía canales independientes para cada conjunto de hilos. El sistema fue diseñado para que, mientras un canal enrolla un extremo del hilo para jalar la pieza, el otro canal desenrolla el hilo opuesto al mismo tiempo.

Para fijar los hilos al plástico del carrete y evitar que resbalaran, el diseño incluyó una pequeña ranura que cruzaba cada canal. Esta ranura permitía sostener el hilo en su lugar mientras se le aplicaba un pegamento líquido de secado rápido (Kola Loka), asegurando una unión firme antes de que el motor comenzara a girar.

### Simulaciones Eléctricas

Los requisitos del proyecto contemplaban la realización de simulaciones por computadora para comprobar el diseño antes de construirlo. En el caso de este proyecto, las simulaciones requeridas correspondían a los circuitos eléctricos.

Sin embargo, no fue necesario realizar estas pruebas virtuales. El diseño electrónico no requería la creación de circuitos complejos desde cero, sino que utilizaba componentes electrónicos y módulos ya fabricados que se comunican directamente con la tarjeta principal. Por lo tanto, el funcionamiento del sistema dependía totalmente de la programación escrita, haciendo innecesario simular el comportamiento de la electricidad en un programa de computadora.
