# Juego de Damas

![Juego de Damas](https://img.shields.io/badge/Juego-Damas-blue)
![Version](https://img.shields.io/badge/Versión-2.0-green)
![Estado](https://img.shields.io/badge/Estado-Activo-success)

Un juego de damas completo con IA, desarrollado con HTML, CSS y JavaScript vanilla. Interfaz moderna con glassmorphism, sonidos sintetizados, y motor de juego con reglas oficiales incluyendo reyes, capturas obligatorias y multi-saltos.

[Jugar Ahora](https://mt3k.net/mondo/Games/Checkers/)

## Caracteristicas

- **Motor de Juego Completo**
  - Reglas oficiales de damas
  - Reyes (damas) con movimiento en 4 direcciones
  - Capturas obligatorias
  - Multi-salto (cadenas de capturas)
  - Deteccion automatica de ganador
  - Sistema de deshacer movimiento

- **Inteligencia Artificial**
  - Algoritmo Minimax con poda Alpha-Beta
  - 3 niveles de dificultad (Facil, Media, Dificil)
  - Evaluacion posicional (material, avance, control del centro, movilidad)
  - Ordenamiento de movimientos para mejor rendimiento
  - Modo vs Jugador (2 jugadores local)

- **Interfaz Moderna**
  - Glassmorphism con paleta gaming (purple + rose)
  - Tipografia Russo One + Chakra Petch
  - Piezas con gradientes radiales 3D
  - Indicadores visuales de capturas obligatorias
  - Marcador en tiempo real y cronometro

- **Animaciones y Sonido**
  - Movimiento suave con Web Animations API
  - Animacion de captura (implosion + rotacion)
  - Coronacion con glow dorado
  - Confetti canvas para el ganador
  - 6 efectos de sonido sintetizados con Web Audio API (sin archivos externos)
  - Respeta `prefers-reduced-motion`

- **Responsive y Accesible**
  - Responsive de 320px a 1440px+ con `clamp()` y media queries
  - Touch-friendly (min 44px targets)
  - Soporte landscape y portrait
  - ARIA roles y focus-visible
  - Event delegation (0 memory leaks)

## Como Jugar

1. **Movimientos Basicos**
   - Las piezas rojas se mueven hacia arriba en diagonal
   - Las piezas plata se mueven hacia abajo en diagonal
   - Un movimiento por turno

2. **Capturas**
   - Si puedes capturar, es obligatorio hacerlo
   - Salta sobre una pieza enemiga para capturarla
   - Si despues de capturar puedes capturar otra, debes continuar (multi-salto)

3. **Reyes (Damas)**
   - Cuando una pieza llega al extremo opuesto, se corona como rey
   - Los reyes se mueven en las 4 direcciones diagonales

4. **Victoria**
   - Gana quien capture todas las piezas del oponente
   - Tambien gana quien deje al oponente sin movimientos validos

5. **Controles**
   - **Nueva Partida** - reinicia el juego
   - **Deshacer** - deshace el ultimo movimiento (en modo IA deshace ambos)
   - **Sonido** - activa/desactiva efectos de sonido
   - **Selector de dificultad** - elige vs Jugador o nivel de IA

## Tecnologias

- HTML5
- CSS3 (glassmorphism, CSS Grid, custom properties, keyframes)
- JavaScript ES6+ (Web Audio API, Web Animations API, Canvas 2D)
- Google Fonts (Russo One, Chakra Petch)

## Instalacion

1. Clona el repositorio:
```bash
git clone https://github.com/MondoBoricua/Checkers-Game.git
```

2. Abre `index.html` en tu navegador. No requiere servidor ni dependencias.

## Compatibilidad

- Chrome
- Firefox
- Safari
- Edge
- Dispositivos moviles y tablets

## Personalizacion

Las variables CSS en `:root` permiten cambiar facilmente:

```css
--color-primary: #7C3AED;    /* Color principal */
--color-accent: #F43F5E;     /* Color de acento */
--color-bg: #0F0F23;         /* Fondo */
--board-light: #2A2A4A;      /* Casillas claras */
--board-dark: #16162E;       /* Casillas oscuras */
--board-size: clamp(280px, 80vmin, 560px); /* Tamano del tablero */
```

## Licencia

Este proyecto esta bajo la Licencia MIT.

---

Desarrollado por [MondoBoricua](https://github.com/MondoBoricua)
