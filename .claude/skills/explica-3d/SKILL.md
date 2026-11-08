---
name: explica-3d
description: Explica cómo funciona algo (un aparato, un fenómeno, un proceso) con una página interactiva en 3D que se puede girar y explorar. Úsala cuando el usuario escriba /explica-3d seguido de un tema, o pida "explícame en 3D cómo funciona X".
---

# Explica en 3D

El usuario da un tema después del comando, por ejemplo: `/explica-3d cómo un refri mantiene frías las cosas`.

## Qué entregar

Una sola página HTML interactiva, publicada como Artifact, que explique el tema con un modelo 3D. Responde en el idioma del usuario (normalmente español).

## Pasos

1. **Entiende el mecanismo real.** Antes de dibujar, identifica las partes del sistema y el orden en que pasa la acción (qué entra, qué se transforma, qué sale). Divide la explicación en 3 a 6 etapas.
2. **Construye la escena 3D** con three.js cargado desde cdnjs (versión fija, por ejemplo `https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js`).
   - Modela cada parte con formas simples (cajas, cilindros, tubos, esferas). Claridad antes que realismo.
   - Agrega controles para girar la cámara con el mouse o el dedo (arrastrar) y hacer zoom (rueda o pellizco). Puedes escribir un control orbital pequeño a mano.
   - Anima lo que se mueve o fluye: partículas, flechas o colores que cambian (por ejemplo azul = frío, rojo = caliente).
3. **Etapas guiadas.** Junto a la escena, un panel con botones "Anterior / Siguiente" (y una lista de etapas). Cada etapa resalta las piezas que participan, mueve la cámara hacia ellas y muestra un texto corto (2 a 4 frases) en lenguaje sencillo.
4. **Etiquetas.** Nombra cada pieza importante en la escena o en una leyenda.
5. **Dato concreto.** Incluye al menos un número real del tema (temperaturas, presiones, velocidades) para que la explicación no sea solo genérica.
6. **Funciona en celular y en modo claro/oscuro.** En pantallas angostas el panel va debajo de la escena. Respeta `prefers-reduced-motion` (pausa la animación automática).

## Al terminar

Publica la página con la herramienta Artifact y responde con un resumen de 2 o 3 frases de la explicación y el enlace.
