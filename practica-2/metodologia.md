---
layout: default
title: Metodología
parent: Práctica 2
nav_order: 2
---

## 2. Metodología de Diseño y Arquitectura Electrónica

Aplicamos la metodología *Pahl & Beitz* para dividir el problema en módulos funcionales, separando la interfaz táctil del procesamiento lógico.

* **El Switch Analógico y Seguridad Inmediata:** Integramos áreas de tela conductiva en los extremos de la pulsera que actúan como un interruptor físico. Aprovechando la resistencia *pull-up* interna del microcontrolador, la pulsera sabe exactamente cuándo está puesta (circuito cerrado a GND) o quitada (circuito abierto). Si la pulsera se retira del brazo en cualquier momento, el sistema lo detecta y apaga los LEDs inmediatamente.
* **Arquitectura de Software (Máquina de Estados):** El mayor reto tecnológico fue garantizar que el sistema respondiera instantáneamente al usuario. Por ello, abandonamos el uso de funciones bloqueantes y construimos una Máquina de Estados basada en la lectura de tiempo real (`millis()`).
* **Flujo de Emergencia:** El código transita de manera fluida a través de 5 estados lógicos (espera, compresiones, pausa de transición, respiraciones y retorno al inicio). Esto permite que el microcontrolador ejecute las animaciones matemáticas de la luz cian y roja mientras, en segundo plano, vigila constantemente si el usuario ha desabrochado el dispositivo.

---
