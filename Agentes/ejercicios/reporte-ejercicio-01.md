# Reporte Ejercicio 1 - Mundo de Wumpus

## 1. Diagrama de la Cueva (`mi_cueva_4x4.yaml`)

| Fila/Col | 1 | 2 | 3 | 4 |
| :---: | :---: | :---: | :---: | :---: |
| **4** | . | Wumpus | . | Oro |
| **3** | . | . | . | . |
| **2** | . | . | . | Pit |
| **1** | Agente> | Pit | . | . |

## 2. Preguntas del Reporte

**¿Qué agentes lograron salir con el oro en tu mapa y cuáles no?**
La verdad es que **ninguno** logró salir con el oro. Resulta que como puse un pozo (pit) en la coordenada `[2, 1]`, el agente siente la brisa desde que empieza en `[1, 1]`. Los agentes lógicos (como el basado en modelo y en metas) son súper precavidos; al sentir peligro de inmediato y no estar seguros de si el pozo está arriba en `[1, 2]` o a la derecha en `[2, 1]`, prefieren no arriesgarse y se quedan dando vueltas sobre su propio eje hasta que se les acaba el tiempo (llegando al límite de pasos). El agente basado en utilidad a veces se arriesga pero casi siempre termina cayendo al pozo, y el de aprendizaje simplemente decide salir de la cueva rápido para no perder tantos puntos.

**¿Por qué el agente de reflejo simple falla (o tiene suerte) en tu diseño?**
Falla totalmente. Como este agente es de reflejo simple, no tiene memoria ni forma un modelo interno para deducir dónde están los peligros a futuro. Solo reacciona a lo que tiene enfrente. Al arrancar y percibir la brisa, sus reglas básicamente le dicen que no avance a ciegas. Termina atrapado en un ciclo girando y girando porque no tiene un mecanismo para sortear el peligro basándose en suposiciones.

**¿Cómo cambia el resultado del agente basado en modelo si acercas o alejas un pit de la casilla inicial?**
Cambia un buen. En mi mapa actual, el pit está pegadito a la entrada (`[2, 1]`), lo que paraliza al agente basado en modelo porque su regla es jugar seguro y ahí no tiene suficiente información para saber qué paso dar. Si alejara ese pit a otra casilla más profunda (como `[3, 3]`), el agente empezaría libre de peligro. Eso le daría confianza para visitar primero las casillas seguras `[1, 2]` y `[2, 1]`, ir armando su mapa mental poco a poco y, por eliminación, ir marcando dónde están las trampas reales hasta encontrar la ruta segura hacia el oro.
