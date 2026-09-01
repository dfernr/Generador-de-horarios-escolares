## ⚠️ AVISO IMPORTANTE: este proyecto está hecho con Inteligencia Artificial

**La práctica totalidad del código de este proyecto — diseño, algoritmos,
implementación, pruebas y esta misma documentación — ha sido escrita con la
ayuda extensiva de un modelo de IA (Claude, de Anthropic), guiado por
Dani.** No es un pequeño apoyo puntual (autocompletado, dudas sueltas): la
mayor parte del trabajo de programación se ha delegado directamente a la
IA, bajo la supervisión y las decisiones de producto de una persona sin
formación formal en ingeniería de software.

Esto significa, en concreto:

- **No ha pasado una auditoría de seguridad ni una revisión de código por
  parte de un desarrollador profesional independiente.** El código ha sido
  probado de forma bastante rigurosa desde el punto de vista funcional
  (existen decenas de pruebas automatizadas que comprueban que el motor de
  generación de horarios se comporta como se espera), pero eso no equivale
  a una auditoría de calidad de software o de seguridad.
- **Puede haber errores no detectados.** Tanto en la lógica de generación
  de horarios como en partes menos probadas de la interfaz. Revisa siempre
  el horario generado antes de usarlo como definitivo — el propio programa
  incluye avisos de conflictos, pero ningún aviso automático sustituye una
  revisión humana.
- **El estilo del código no es necesariamente el que escribiría un
  desarrollador profesional experimentado.** Prioriza que funcione
  correctamente y esté bien comentado sobre seguir al pie de la letra las
  convenciones que usaría un equipo de ingeniería de software.
- **Los datos siempre se quedan en tu navegador.** Esto no ha cambiado por
  usar IA para programarlo: se ha verificado explícitamente que no hay
  ninguna llamada de red que envíe tus datos a ningún sitio (ver el
  [`README.md`](./README.md), sección "Privacidad y datos").

**Por qué se publica así de todas formas**: el proyecto nació para resolver
un problema real y concreto (generar horarios en centros pequeños con
profesorado a jornada parcial), ha demostrado funcionar bien en la práctica,
y se comparte con la esperanza de que sea útil a otros centros en la misma
situación — no como un ejercicio de ingeniería de software para presumir de
código. Si eres desarrollador y quieres revisarlo, mejorarlo o señalar
fallos, eres más que bienvenido.

Si usas este programa para generar el horario real de tu centro: revísalo
tú mismo antes de publicarlo. No hay ninguna garantía, ni implícita ni
explícita, de que el resultado esté libre de errores (ver
[`LICENSE.md`](./LICENSE.md)).
