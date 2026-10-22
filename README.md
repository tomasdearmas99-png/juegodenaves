# Simulador de Combate Espacial en Consola


## Descripción

**Simulador de Combate Espacial** es un juego en modo consola donde controlás una nave que debe esquivar y destruir asteroides que caen desde la parte superior de la pantalla. Cada choque te cuesta una vida: ¡si llegás a cero, se termina la partida!

El proyecto fue desarrollado como **Actividad 8** de la materia **Laboratorio de Programación (LPR)** y sirve para aplicar el paso de `struct` a `class`: atributos **privados**, métodos **públicos**, **constructores** y **encapsulamiento**.

## Datos académicos

| | |
|---|---|
| **Institución** | E.E.S.T. N° 999 "Österreichische Schule der Nationalökonomie" — Vicente López |
| **Materia** | Laboratorio de Programación (LPR) — 5° Año, 3° A-B |
| **Actividad** | 8 — Introducción a POO: Juego de Naves en Consola (`class Nave`) |
| **Docente** | Mansilla Muñoz York |
| **Ciclo lectivo** | 2026 — 2° Cuatrimestre |

## Integrantes

| Nombre y apellido |
|---|
| Sofia Mojica |
| Gabriel Zacarias |
| Mateo Roberts |
| Leonel De Armas |

## Características

- Nave controlable con movimiento en las cuatro direcciones.
- Sistema de disparo con balas independientes.
- Asteroides que reaparecen en posiciones aleatorias.
- Sistema de vidas con pantalla de *Game Over*.
- HUD con el nombre del piloto (identificación para las capturas de evidencia).
- Clases con **encapsulamiento**: atributos `private` y acceso mediante métodos `public`.

## Controles

| Tecla | Acción |
|:---:|---|
| `W` | Mover hacia arriba |
| `A` | Mover a la izquierda |
| `S` | Mover hacia abajo |
| `D` | Mover a la derecha |
| `ESPACIO` | Disparar |



## Requisitos

- **Sistema operativo:** Windows (usa `<windows.h>` y `<conio.h>`, por lo que **no compila en Linux ni macOS**).
- **Compilador:** `g++` (MinGW-w64) o MSVC, con soporte para C++11 o superior.
- **Editor sugerido:** Visual Studio Code, Dev-C++ o Code::Blocks.

## Compilación y ejecución

1. Clonar el repositorio:

   ```bash
   git clone <URL_DEL_REPOSITORIO>
   cd juegodenaves
   ```

2. Compilar con `g++`:

   ```bash
   g++ src/main.cpp -o juegodenaves.exe
   ```

3. Ejecutar:

   ```bash
   juegodenaves.exe
   ```

4. Ingresar **nombre y apellido** cuando el programa lo pida (aparecerá en el HUD) y ¡a jugar!

## Estructura del repositorio

```
juegodenaves/
├── .gitignore                  # Exclusiones (.exe, *.out, .vscode/)
├── LICENSE                     # Licencia MIT
├── README.md                   # Portada del proyecto
├── docs/
│   ├── InformeEEST1_LPR2026_ACT08_G03_v1.0.0.pdf   # Informe APA v7
│   ├── CHANGELOG.md            # Historial de versiones
│   └── manuales/
│       ├── manual_programador_v1.0.0.pdf
│       └── manual_usuario_v1.0.0.pdf
├── src/
│   └── main.cpp                # Código fuente C++
└── capturas/
    └── combate_consola.png     # Evidencia de ejecución
```

## Diseño de clases

| Clase | Responsabilidad | Atributos privados | Métodos públicos principales |
|---|---|---|---|
| `Nave` | Jugador | `x`, `y`, `vidas` | `getX()`, `getY()`, `getVidas()`, `reducirVida()`, `pintar()`, `borrar()`, `mover(char)` |
| `Asteroide` | Obstáculo que cae | `x`, `y` | `getX()`, `getY()`, `pintar()`, `borrar()`, `mover()` |
| `Bala` | Proyectil del jugador | `x`, `y` | `getX()`, `getY()`, `mover()`, `fueraDeRango()` |

**Conceptos de POO aplicados:**

- **Encapsulamiento:** los datos de cada objeto son `private`; solo se accede a ellos mediante métodos `public` ("puertas controladas").
- **Constructores:** inicializan cada objeto al crearlo (ej. `Nave jugador(35, 20, 3);`).
- **Métodos:** cada objeto sabe pintarse, borrarse y moverse por sí mismo.
- **Memoria dinámica:** `Asteroide` y `Bala` se crean con `new` y se liberan con `delete` dentro de `std::vector`.

## Funcionalidad extra implementada

> _Completar con la funcionalidad elegida del anexo de Classroom/Moodle._

- **Funcionalidad:** `<nombre de la funcionalidad>`
- **Descripción:** `<qué hace>`
- **Partes del código modificadas:** `<clases / funciones / secciones del main>`

## Documentación

- [Informe APA v7](docs/InformeEEST1_LPR2026_ACT08_G03_v1.0.0.pdf)
- [Manual del Programador](docs/manuales/manual_programador_v1.0.0.pdf)
- [Manual del Usuario](docs/manuales/manual_usuario_v1.0.0.pdf)
- [Historial de cambios (CHANGELOG)](docs/CHANGELOG.md)

## Captura de ejecución

![Captura del juego](capturas/combate_consola.png)

## Referencias

- [cplusplus.com — Clases y objetos en C++](https://cplusplus.com/doc/tutorial/classes/)
- [GeeksforGeeks — Modificadores de acceso en C++](https://www.geeksforgeeks.org/access-modifiers-in-c/)
- [Microsoft Learn — Constructores e inicialización de clases](https://learn.microsoft.com/es-es/cpp/cpp/constructors-cpp)
- [Git Documentation](https://git-scm.com/doc)

## Licencia

Distribuido bajo la licencia **MIT**. Consultá el archivo [LICENSE](LICENSE) para más información.

---

<p align="center">Desarrollado por Sofia Mojica, Gabriel Zacarias, Mateo Roberts y Leonel De Armas — E.E.S.T. N° 999 · 2026</p>
