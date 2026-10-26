# Diagnóstico del contexto — Proyecto de monitoreo de humedad en invernaderos

> **EJEMPLO HIPOTÉTICO PARA TDTA I.**

**Proyecto provisional:** Evaluación de la viabilidad de un sensor óptico para estimar humedad del sustrato, con posible monitoreo IoT.  
**Estado del documento:** avance después de las tarjetas **U3.1 y U3.2**.  
**Alcance actual:** identificar afirmaciones, buscar evidencias y reconocer incertidumbres. El diagnóstico causal y la decisión final se completarán en U3.3 y U3.4.

---

## 1. Situación inicial y alcance de la exploración

El equipo considera desarrollar un sensor óptico infrarrojo para estimar la humedad del sustrato de plántulas de tomate y registrar mediciones mediante un sistema IoT. La idea surgió de la percepción de que los sensores comerciales podrían presentar limitaciones de costo, mantenimiento o precisión.

**Problema inicial propuesto (todavía no comprobado):** se desconoce si los métodos de medición disponibles satisfacen las necesidades de seguimiento de humedad del sustrato en el contexto de cultivo que se desea atender.

Para esta etapa se estudiarán tres aspectos:

1. Cómo se mide actualmente la humedad del sustrato y qué decisiones se toman con esas mediciones.
2. Qué opciones comerciales existen y cuáles son sus características y costos comparables.
3. Qué evidencia técnica existe sobre métodos ópticos de estimación de humedad y bajo qué condiciones funcionan.

**No se investigará todavía** el diseño del circuito, la programación del sistema IoT ni la construcción del sensor.

---

## 2. U3.1 — Auditoría de afirmaciones del expediente inicial

**Fuente utilizada:** [Expediente inicial del Equipo 1](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md).

**Criterio de clasificación:** «Hecho documentado» se usa únicamente para hechos comprobables en el expediente (por ejemplo, que el equipo identificó ciertos beneficiarios), no para certificar que una necesidad técnica ya fue demostrada. «Supuesto por verificar» requiere respaldo externo o empírico; «Decisión preliminar» expresa una elección de diseño o alcance todavía revisable; «Pregunta abierta» expresa algo pendiente de resolver, incluso si el expediente contiene una respuesta inicial.

**Asignación de responsables:** es una **propuesta didáctica basada en los roles consignados en el expediente**, no una asignación ya aprobada por los estudiantes. Deben confirmarla en su Issue.

| Afirmación textual o parafraseada                                                                                                                        | Clasificación          | Evidencia disponible y enlace                                                                                                                                                                                                                       | Información faltante                                                   | Forma de obtenerla                                                      | Responsables                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------- |
| El equipo propone desarrollar y caracterizar un sensor óptico de humedad por reflexión infrarroja.                                                       | Decisión preliminar    | La propuesta está registrada en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md); no se aportan pruebas experimentales.                                                                       | Antecedentes de viabilidad y condiciones de medición.                  | Revisar artículos técnicos y protocolos de caracterización.             |                                                               |
| El equipo propone crear un sistema IoT para registrar y visualizar datos y comparar sensores.                                                            | Decisión preliminar    | La propuesta figura en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md); no se documenta una necesidad validada de conectividad.                                                              | Usuarios, utilidad del registro remoto y conectividad disponible.      | Consultar a posibles usuarios y describir el flujo actual de datos.     |                                                               |
| «La problemática que identificamos es la falta de un sistema automatizado» para monitorear humedad y temperatura de plántulas.                           | Supuesto por verificar | El [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md) describe el problema; no incorpora observaciones o entrevistas que corroboren esa falta.                                                     | Contexto concreto, sistema actual y evidencia de la carencia.          | Observación autorizada, entrevista y registro del procedimiento actual. |                                                               |
| El equipo considera necesario un sensor óptico IR «menos invasiva y más económica» que sensores resistivos o capacitivos.                                | Supuesto por verificar | La comparación se afirma en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md); no se adjuntan mediciones ni costos.                                                                            | Modelos comparables, tipo de contacto, costos y mantenimiento.         | Consultar fichas técnicas, cotizaciones y estudios de desempeño.        |                                                               |
| «Los sensores tradicionales requieren contacto directo, son más costosos y pueden degradarse con el tiempo».                                             | Supuesto por verificar | La afirmación aparece en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md), sin referencias técnicas que la sustenten.                                                                         | Qué sensores, condiciones, costos y mecanismos de degradación.         | Comparar especificaciones y literatura técnica verificable.             |                                                               |
| El equipo identifica como posibles beneficiarios a productores de tomate, operadores de invernaderos, investigadores agrícolas y docentes de ingeniería. | Hecho documentado      | La lista de beneficiarios está consignada en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md). Esto prueba la identificación por el equipo, no necesidades confirmadas por los beneficiarios. | Usuarios concretos y necesidades reales de cada grupo.                 | Entrevistas y delimitación del usuario objetivo.                        |                                                               |
| El equipo considera viable desarrollar el proyecto progresivamente durante los cinco TDTA.                                                               | Supuesto por verificar | La valoración del equipo consta en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md); no hay evaluación detallada de recursos y tiempos.                                                       | Recursos, riesgos, dependencias y alcance por etapa.                   | Inventario de recursos y análisis preliminar de factibilidad.           |                                                               |
| «Se requiere una precisión de ±5% de humedad volumétrica».                                                                                               | Decisión preliminar    | El valor está registrado en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md), sin fuente o necesidad de usuario que lo justifique.                                                            | Definición del error, fundamento de tolerancia y método de referencia. | Consultar requerimientos de uso y literatura metrológica.               |                                                               |
| «Se mide por validación cruzada contra un sensor de humedad de referencia resistivo o capacitivo».                                                       | Decisión preliminar    | El método está propuesto en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md); no hay evidencia de validación efectuada.                                                                       | Modelo de referencia, calibración, incertidumbre y protocolo.          | Consultar especificaciones y diseñar un protocolo comparativo.          |                                                               |
| ¿La luz ambiental afectará la lectura del fotodetector? ¿Se necesita encapsulado oscuro?                                                                 | Pregunta abierta       | La pregunta y una respuesta inicial aparecen en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md); no se presentan ensayos.                                                                    | Magnitud de interferencia y necesidad real de encapsulado.             | Revisar literatura y diseñar pruebas controladas posteriores.           |                                                               |
| El equipo indica que el sensor debe funcionar con 5 V/3.3 V del microcontrolador del Proyecto 2.                                                         | Decisión preliminar    | La restricción está registrada en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md); no se adjunta identificación del microcontrolador ni cálculo eléctrico.                                   | Compatibilidad, consumo y márgenes eléctricos.                         | Consultar documentación del microcontrolador y componentes.             |                                                               |
| «los sensores ópticos y capacitivos de bajo costo reportan errores de ±3% a ±8%».                                                                        | Supuesto por verificar | La cifra se menciona en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md), pero no se proporcionan referencias.                                                                                | Estudios originales, condiciones de prueba y definición del error.     | Localizar y comparar estudios con referencias completas.                |                                                               |
| «No se hace uso de balanza de precesión en el proyecto».                                                                                                 | Decisión preliminar    | La decisión está consignada en el [expediente inicial](https://github.com/adriana71/Eq1-Humedad/blob/main/docs/expediente-inicial.md).                                                                                                              | Método alternativo para establecer humedad de referencia.              | Revisar métodos de referencia y disponibilidad de instrumentos.         | @jmosqueda03-ux (integración/validación); @Miguelg30 (datos). |

### Preguntas prioritarias derivadas de la matriz

1. ¿Qué observaciones o testimonios confirman que falta un sistema de monitoreo en el contexto que se desea atender?
2. ¿Qué evidencia sustenta la comparación de costo, invasividad y durabilidad entre sensores?
3. ¿Qué antecedentes permiten evaluar la alternativa óptica y justificar la precisión propuesta?
4. ¿Qué necesidades concretas justifican incorporar IoT?

**Resultado de U3.1:** identificar lo que el equipo afirmó, lo que ya documentó y lo que todavía debe investigar; no demostrar anticipadamente que su solución es superior.

---

## 3. U3.2 — Búsqueda y registro de evidencias

### 3.1 Estrategia de búsqueda

| Pregunta | Palabras clave de ejemplo                                                                       | Fuentes por consultar                                              | Qué se registrará                                                        |
| -------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| P1       | «humedad del sustrato», «riego de plántulas», «frecuencia de medición»                          | Manuales agronómicos, documentación técnica, entrevista autorizada | Práctica actual, necesidad, decisiones y contexto.                       |
| P2       | «soil moisture sensor datasheet», «capacitive soil moisture sensor», «sensor de humedad precio» | Fichas de fabricante y cotizaciones comparables                    | Principio, rango, costo total, mantenimiento y limitaciones.             |
| P3       | «near infrared soil moisture», «optical soil moisture sensing», «calibration substrate»         | Artículos arbitrados, tesis y revisiones técnicas                  | Sustrato, método de referencia, rango, calibración y errores reportados. |

**Criterios de selección:** pertinencia con el problema, autoría identificable, fecha, descripción del método y condiciones de aplicación. Una ficha comercial puede informar especificaciones, pero no sustituye por sí sola una validación independiente.

### 3.2 Registro de fuentes y evidencias — datos simulados

| Código | Pregunta | Fuente hipotética                                                    | Tipo                                 | Hallazgo hipotético                                                                                        | Contexto / limitación                                                                    | Evaluación                                                             |
| ------ | -------- | -------------------------------------------------------------------- | ------------------------------------ | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| E1     | P1       | Entrevista simulada con responsable de invernadero (12/10/2026)      | Evidencia directa **simulada**       | El riego se decide por observación y mediciones esporádicas; el responsable desearía consultar tendencias. | Una persona y un solo invernadero; no representa a todos los cultivos.                   | Útil para definir necesidades locales, pendiente de verificación real. |
| F1     | P2       | Ficha técnica **ficticia** de sensor capacitivo modelo C-100         | Documento de fabricante **simulado** | Precio ilustrativo: $180 MXN por unidad; requiere calibración para el sustrato.                            | No incluye instalación, mantenimiento ni prueba independiente.                           | Útil para comparar características; no demuestra desempeño real.       |
| F2     | P2       | Cotización **ficticia** de sensor profesional modelo P-200           | Cotización **simulada**              | Precio ilustrativo: $2,400 MXN; incluye acondicionamiento y especificaciones ampliadas.                    | No comparable directamente sin definir uso, precisión y accesorios.                      | Comparación preliminar, insuficiente para concluir «alto costo».       |
| F3     | P3       | Artículo académico **ficticio** sobre estimación óptica en sustratos | Literatura científica **simulada**   | Reporta relación entre respuesta óptica y humedad bajo calibración controlada.                             | Resultados limitados al sustrato y montaje estudiados; no extrapolables automáticamente. | Indicio de factibilidad, no prueba para el proyecto.                   |

> **Importante:** estos cuatro registros son ejemplos de cómo llenar la matriz. No deben citarse como fuentes reales. En una entrega auténtica, cada registro debe incluir referencia completa, enlace o archivo verificable y fecha de consulta.

### 3.3 Síntesis de los hallazgos hipotéticos

**Sobre P1 — necesidad:** la entrevista simulada sugiere interés en consultar tendencias de humedad. Esto **no demuestra** que sea indispensable desarrollar un nuevo sensor; podría bastar un dispositivo existente.

**Sobre P2 — alternativas comerciales:** los precios ilustrativos muestran que las opciones pueden diferir mucho. Por tanto, la frase «todos los sensores son costosos» es demasiado general. Se necesita una comparación con el mismo uso previsto, condiciones de operación y costo total.

**Sobre P3 — método óptico:** el artículo ficticio sugiere que la estimación óptica podría ser investigable, pero no prueba que funcione para el sustrato, el montaje o el rango del equipo. Harían falta una calibración y un método independiente de referencia.

### 3.4 Actualización didáctica de afirmaciones del expediente (escenario hipotético)

La siguiente tabla **no representa una verificación efectuada por el Equipo 1**: muestra cómo podría cambiar la evaluación de afirmaciones reales **si se obtuvieran** las evidencias simuladas de § 3.2.

| ID real del expediente | Estado hipotético tras U3.2                                          | Acción necesaria                                             |
| ---------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------ |
| A1                     | Parcialmente apoyada para un invernadero particular por E1 ficticia. | Corroborar con registros reales del proceso.                 |
| A2–A3                  | Ventajas económicas y de invasividad no demostradas.                 | Comparar modelos equivalentes y condiciones de montaje.      |
| A4                     | Línea de desarrollo plausible, todavía sin validación.               | Obtener antecedentes reales y definir el experimento.        |
| A5                     | Utilidad de IoT aún por verificar.                                   | Precisar usuarios, decisiones y necesidades de conectividad. |
| A6                     | Tolerancia ±5 % sin justificación suficiente.                        | Precisar magnitud y fundamento del requisito.                |
| A7 y A9                | Método de referencia insuficientemente descrito.                     | Verificar calibración e independencia de la referencia.      |
| A8                     | Rango de errores sin fuente comprobable en el expediente.            | Recuperar publicaciones originales.                          |
| A10                    | Restricción de alimentación preliminar.                              | Verificar compatibilidad y necesidad real.                   |

### 3.5 Contradicciones y limitaciones

- **Contradicción aparente:** el equipo supone que los sensores existentes son costosos, pero la comparación ilustrativa incluye una opción económica. Eso obliga a precisar qué significa «costoso» en su aplicación.
- **Limitación de contexto:** una entrevista aislada no permite generalizar a todos los invernaderos.
- **Limitación técnica:** una prueba óptica en un sustrato no garantiza desempeño en otro.
- **Limitación metodológica:** no se dispone aún de mediciones propias ni de un procedimiento validado de referencia.

---

## 4. Conclusiones provisionales después de U3.1 y U3.2

1. La **necesidad de monitoreo** es una posibilidad que requiere corroboración en un contexto definido.
2. La **desventaja de los sensores comerciales** no puede afirmarse sin comparación técnica y económica homogénea.
3. El **desarrollo de un sensor óptico** debe tratarse como alternativa o línea de investigación, no como solución ya justificada.
4. La **integración IoT** permanece como opción y no como requisito definitivo.

**Conclusión provisional modelo:** «Con la información disponible, el equipo considera pertinente continuar investigando la necesidad de seguimiento de humedad del sustrato en un contexto de cultivo delimitado. Todavía no cuenta con evidencia suficiente para afirmar que el desarrollo de un sensor óptico propio sea superior a las alternativas existentes. Antes de fijar una solución, será necesario contrastar el proceso de medición actual, comparar tecnologías y establecer criterios verificables».

---

## 5. Referencias y trazabilidad

**Fuente documental real para U3.1:** Equipo 1, *expediente-inicial.md*, secciones 2, 3, 6 y 7, disponible en el repositorio enlazado al comienzo de la sección 2. **Fuentes de evidencia U3.2:** `F1`, `F2`, `F3` y `E1` son identificadores ficticios.

En el trabajo auténtico, cada fuente debe registrarse así:

- **Fuente documental:** Autor/institución. (Año). *Título*. Editorial/revista/fabricante. Enlace. Fecha de consulta cuando corresponda.
- **Evidencia directa:** Código de entrevista u observación, fecha, lugar general, autorización, instrumento utilizado y archivo de resguardo, sin divulgar datos personales innecesarios.
- **Trazabilidad:** enlazar los issues U3.1 y U3.2, los commits de actualización y la entrada correspondiente en la bitácora.

**Ejemplo de registro de bitácora (hipotético):** «12/10/2026. Se decidió mantener el desarrollo del sensor óptico como alternativa por investigar, no como solución definitiva, porque la comparación de opciones comerciales y la validación del principio de medición siguen incompletas. Responsables: integrantes A, B y C».
