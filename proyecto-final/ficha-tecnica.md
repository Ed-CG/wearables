---
layout: default
title: Ficha Técnica
parent: Proyecto Final
nav_order: 9
---

## Ficha Técnica

Esta sección funciona como un resumen directo de las medidas, el peso, los requerimientos de energía y la lista completa de todos los materiales necesarios para construir la obra en su totalidad.

### Especificaciones Teóricas Finales

**Masa Total Estimada**
La armadura completa tiene un peso calculado que supera los 25 kilogramos. La gran mayoría de este peso corresponde a las 2,000 piezas de plástico sólido impresas en 3D. A esto se le suma el peso de los seis rollos de alambre metálico utilizados para el esqueleto interno y los cinco metros de tela.

**Consumo Eléctrico Máximo Proyectado**
El sistema de movimiento depende de 10 motores eléctricos que funcionan a 12 voltios. Si el sistema ordena a los 10 motores encenderse al mismo tiempo y jalar los hilos con su fuerza máxima, se calcula que la prenda consumiría picos de energía de hasta 15 amperios. Para entregar esta cantidad de energía de forma segura y sin que el sistema se apague, se requiere el uso de baterías recargables de alta capacidad de descarga.

### Lista de Materiales (Bill of Materials)

A continuación, se desglosan todos los componentes organizados en una tabla formal. Esta lista incluye tanto los materiales físicos que sí se compraron y utilizaron, como la electrónica que fue calculada en la planeación pero no se instaló en la pieza.

| Categoría | Componente | Cantidad | Descripción y Uso |
| :--- | :--- | :--- | :--- |
| **Polímeros** | Filamento plástico (PLA) | 25 kilogramos | Material necesario para la impresión 3D de las 2,000 escamas y sus respectivas bases. |
| **Textiles** | Tela tipo vinipiel | 5 metros | Recubrimiento exterior. Cuenta con una red o malla tejida de hilos de poliéster en su parte trasera para la unión con el plástico. |
| **Estructurales** | Alambre estructural | 6 rollos | Construcción del soporte interno (chasis) de la prenda. |
| **Estructurales** | Cinta de aislar | 6 rollos | Aseguramiento y fijación de todas las uniones del alambre. |
| **Mecánicos** | Manguera de teflón (PTFE) | 3 metros | Guías de baja fricción para los hilos (diámetro interno: 3 milímetros, diámetro externo: 4 milímetros). |
| **Mecánicos** | Hilo de pesca trenzado | 1 rollo (300 metros) | Líneas de tracción de alta resistencia utilizadas para jalar las piezas de plástico sin romperse ni estirarse. |
| **Electrónicos** (Proyectados) | Motores eléctricos con engranajes | 10 piezas | Modelo GM25-370 (12 voltios). Encargados de enrollar los hilos. |
| **Electrónicos** (Proyectados) | Tarjeta electrónica central | 1 pieza | Microcontrolador responsable de procesar la información del sistema. |
| **Electrónicos** (Proyectados) | Sensor de movimiento | 1 pieza | Encargado de detectar la inclinación y postura del cuerpo humano. |
| **Electrónicos** (Proyectados) | Controladores de energía | 5 módulos | Administran la electricidad desde la batería hacia los motores (cada módulo controla dos motores). |
| **Electrónicos** (Proyectados) | Reductor de voltaje | 1 pieza | Baja la energía de 12 voltios de la batería a los 5 voltios que soporta la tarjeta central de forma segura. |
| **Electrónicos** (Proyectados) | Batería recargable y cargador | 1 set | Tipo LiPo de 3 celdas (11.1 voltios) de alta descarga para alimentar todo el mecanismo. |
| **Electrónicos** (Proyectados) | Cables eléctricos de silicón | Varios metros | Calibre 22 para transportar la energía a los motores y calibre 26 para enviar datos de información. |
