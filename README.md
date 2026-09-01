# Generador de Horarios Escolares

Herramienta web para generar automáticamente el horario semanal de un
centro de secundaria pequeño: grupos, asignaturas, profesorado con jornada
parcial, guardias y reuniones de departamento — pensada especialmente para
el caso típico de **centros rurales pequeños** (CPEB, IES de una línea) con
disponibilidad de profesorado rotativa e irregular.

> ⚠️ **Antes de nada, lee [`AVISO_IA.md`](./AVISO_IA.md).** Este proyecto se
> ha desarrollado con ayuda extensiva de Inteligencia Artificial, sin
> auditoría de código por un desarrollador profesional independiente.

## Qué hace

A partir del currículo de cada grupo, el profesorado disponible y sus
restricciones, el programa:

1. Genera automáticamente **horarios completos sin conflictos** (Fase 1):
   ningún profesor da dos clases a la vez, se respeta la disponibilidad de
   cada uno, se cubren las horas de guardia y se colocan las reuniones de
   departamento.
2. **Refina la calidad** del horario elegido (Fase 2): reduce huecos en la
   jornada del profesorado, evita que una asignatura se repita el mismo día,
   y respeta las preferencias de quienes prefieren empezar tarde o acabar
   pronto — usando un algoritmo de optimización (Simulated Annealing) con
   varios mecanismos especializados y reinicios automáticos.

El resultado se puede exportar como Excel (con vista por grupo y por
profesor, coloreado) o CSV.

## Cómo empezar

1. Abre `Horario_v1.10.html` en cualquier navegador moderno (Chrome, Safari,
   Firefox, Edge). No hace falta instalar nada ni tener conexión a internet
   (salvo para exportar el Excel con colores).
2. Pulsa **"🎓 Cargar ejemplo CPEB genérico"** en la pantalla de bienvenida
   para ver el programa funcionando con datos de ejemplo, o empieza desde
   cero configurando tu propia jornada.
3. Sigue los 4 pasos de las pestañas: Grupos y asignaturas → Profesores →
   Asignación → Generar horario.
4. Dentro de la propia aplicación, el botón **"ⓘ Ayuda"** (arriba a la
   derecha) tiene una guía completa: flujo de trabajo paso a paso, valores
   recomendados, cómo guardar y retomar una sesión, y solución de problemas
   habituales. Cada sección técnica (Fase 1, Fase 2) tiene además su propia
   explicación desplegable justo donde se usa.

Este README es una introducción; **la guía de uso detallada vive dentro del
propio programa**, para no tener que ir cambiando de pestaña del navegador
mientras lo usas.

## Privacidad y datos

Todo el cálculo ocurre **en tu navegador**. No hay servidor, no hay base de
datos, no hay ninguna llamada de red que envíe información de tu centro a
ningún sitio — se ha comprobado explícitamente que el código no usa
`localStorage` ni hace peticiones `fetch`/`XMLHttpRequest` salvo para cargar
dos librerías de terceros (para generar el Excel con colores) desde una CDN
pública, que no reciben ni envían ningún dato tuyo. Tus datos (currículo,
profesorado, horarios generados) solo existen en la pestaña abierta de tu
navegador y en los archivos que tú decidas exportar.

## Licencia

Este proyecto se distribuye bajo licencia **CC BY-NC 4.0** (uso y
modificación libres, no comercial, con atribución). Ver
[`LICENSE.md`](./LICENSE.md) para el detalle completo.

## Autoría

Desarrollado por **Dani**, con ayuda extensiva de IA (ver
[`AVISO_IA.md`](./AVISO_IA.md)).

## Aportar cambios / reportar fallos

Si encuentras un error o quieres proponer una mejora, eres bienvenido a
abrir un *issue* o una *pull request* en el repositorio. No hay ningún
compromiso de mantenimiento continuo por parte del autor.
