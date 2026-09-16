# Camino a experto en Revit / BIM (arquitectura y diseño de interiores) — 100% gratis y legal

Proyecto de investigación continua para construir, corrida a corrida, la ruta completa hacia un nivel **experto** en Autodesk Revit y en metodología BIM aplicada a arquitectura y diseño de interiores, sin pagar nada, para un lector argentino que arranca **desde cero**.

Regla dura del proyecto: todo lo recomendado tiene que ser gratis y legal. La licencia educativa de Autodesk cuenta como gratuita y legal siempre que se respeten sus condiciones reales (uso estrictamente no comercial, vencimiento, verificación de condición de estudiante). **Nunca se recomiendan cracks, keygens ni "versiones full" pirateadas de Revit/Autodesk.**

Este documento se actualiza agregando contenido en cada corrida, nunca borrando ni resumiendo lo ya escrito. Ver el **Log de iteraciones** al final para el estado de avance.

---

## Roadmap de aprendizaje

Estructura general (se irá detallando etapa por etapa en corridas sucesivas; lo marcado como "cubierto en profundidad" ya tiene guía práctica más abajo, lo demás es esqueleto pendiente de desarrollo):

**Etapa 0 — Acceso legal a la herramienta (CUBIERTO EN PROFUNDIDAD en esta iteración, 2026-09-16)**
Conseguir Revit gratis y legal vía Autodesk Education Plan, entender sus condiciones reales, e instalar en paralelo el camino libre (Blender+Bonsai / FreeCAD BIM) que no caduca.

**Etapa 1 — Fundamentos de modelado arquitectónico (pendiente de desarrollo en profundidad)**
Interfaz de Revit, niveles y grillas, muros, pisos, cubiertas/techos, puertas y ventanas, escaleras y barandas, Rooms/Áreas, vistas y organización de proyecto.

**Etapa 2 — Documentación técnica y planos (pendiente)**
Anotaciones, cotas, textos, tablas de planificación (schedules), leyendas, hojas (sheets), normativa de representación gráfica, plotting/export a PDF y DWG.

**Etapa 3 — Diseño de interiores en Revit (pendiente)**
Espacios (Rooms) y su rol en el cómputo, materiales y acabados, mobiliario (familias de equipamiento), iluminación (familias de luminarias + análisis básico), especificación de acabados por ambiente (finish schedules), paletas y renders de interior.

**Etapa 4 — Familias paramétricas (Family Editor) (pendiente)**
Lógica paramétrica, familias basadas en host vs. independientes, parámetros y fórmulas, familias de mobiliario y equipamiento a medida, buenas prácticas de biblioteca de familias.

**Etapa 5 — Sitio, topografía y paisajismo (pendiente)**
Topografía (toposurface/site), plataformas y subregiones, componentes de sitio y paisajismo, emplazamiento del proyecto respecto al terreno real.

**Etapa 6 — BIM colaborativo (pendiente)**
Worksets y trabajo compartido (worksharing), vínculos entre modelos (arquitectura/estructura/instalaciones), coordinación multidisciplinaria, detección de interferencias (clash detection) con Navisworks u otra herramienta gratuita equivalente.

**Etapa 7 — Diseño computacional con Dynamo (pendiente)**
Programación visual, automatización de tareas repetitivas, generación paramétrica de geometría y datos, extracción/edición masiva de parámetros.

**Etapa 8 — Renderizado y visualización arquitectónica (pendiente)**
Motores de render disponibles gratis (Twinmotion con sus condiciones reales, Enscape en su versión de prueba, render nativo de Revit), técnicas de iluminación y materialización para presentación.

**Etapa 9 — Interoperabilidad openBIM (pendiente)**
IFC en profundidad (esquema, IFC2x3 vs IFC4, cómo exportar/importar sin pérdida de datos), COBie, nociones de ISO 19650 (gestión de información BIM), BCF para gestión de incidencias de coordinación.

**Etapa 10 — Cómputo y presupuesto desde el modelo (pendiente)**
Tablas de planificación de materiales y cantidades, cómputo métrico desde el modelo, vínculo con presupuesto, control de calidad del modelo para que el cómputo sea confiable.

**Etapa 11 — Normativa argentina aplicada (transversal, se va integrando en cada etapa relevante)**
Código de Edificación (jurisdicción por defecto: CABA), Ley 962 y normas IRAM de accesibilidad, normas de seguridad contra incendios, marco de ejercicio profesional (CPAU u organismo que corresponda). Este roadmap enseña la herramienta BIM; **no reemplaza la matrícula profesional habilitante para firmar planos.**

**Etapa 12 — Validación y empleabilidad (transversal)**
Certificación Autodesk Certified Professional (Revit) — tiene costo, es dato de contexto no gasto obligatorio —, comunidades y foros para resolver dudas y mostrar trabajo, portfolio.

---

## Software y herramientas gratuitas

### Camino con licencia educativa (Autodesk)

| Herramienta | Versión / plataforma | Licencia y límites | Para qué sirve | Formatos de intercambio |
|---|---|---|---|---|
| **Autodesk Revit** | Última versión estable (2026), solo **Windows** (no hay versión nativa Mac/Linux) | Autodesk Education Plan: gratis 1 año renovable mientras se mantenga la condición de estudiante verificada. **Uso estrictamente no comercial, no profesional, no lucrativo** (ver detalle en Etapa 0 más abajo). | Modelado BIM arquitectónico completo, documentación, familias paramétricas, colaboración (worksets), Dynamo integrado | RVT (nativo), RFA (familias), exporta/importa IFC, DWG/DXF, exporta NWC (a Navisworks), gbXML (análisis energético) |
| **Dynamo** | Se instala junto con Revit (Dynamo for Revit); también existe **Dynamo Core/Sandbox** standalone y open source (proyecto en GitHub, licencia libre) que corre sin Revit para programación visual pura | Gratis. La integración completa con elementos de Revit requiere tener Revit instalado y licenciado. | Programación visual, automatización dentro de Revit | Trabaja sobre el modelo RVT abierto |
| **Twinmotion** | Última versión, Windows/Mac | Gratis para individuos, estudiantes y empresas con **facturación anual menor a USD 1.000.000**, uso comercial incluido bajo ese tope. Por encima del tope o si se necesita Twinmotion Cloud, es pago (~USD 445/año). Requiere cuenta de Epic Games. *(Verificar condiciones vigentes en twinmotion.com antes de asumir "gratis sin condiciones".)* | Renderizado y visualización arquitectónica en tiempo real | Importa modelo desde Revit vía Datasmith |
| **Navisworks** (Simulate/Manage) | — | Mencionado en fuentes secundarias como incluido dentro del Autodesk Education Plan junto con "más de 60 aplicaciones", pero **no pude confirmar esto contra la fuente oficial** en esta corrida porque autodesk.com estuvo bloqueado para el fetch directo (ver limitaciones). Queda pendiente confirmar en próxima iteración. | Coordinación multidisciplinaria y detección de interferencias (clash detection) | NWC/NWD |

### Camino 100% libre y de código abierto — no caduca, no tiene restricción de uso comercial

Este es el argumento de fondo del proyecto, no una alternativa menor: es el camino que el lector puede seguir usando **después de perder la condición de estudiante**, sin depender de ninguna verificación ni renovación.

| Herramienta | Versión / plataforma | Licencia | Para qué sirve | Para qué NO sirve (o sirve peor que Revit) | Formatos |
|---|---|---|---|---|---|
| **Blender + extensión Bonsai** (ex BlenderBIM) | Bonsai 0.8.5 (post1), compatible con Blender 4.2 LTS; **no soportado en Blender 5.1+** todavía a la fecha de esta corrida — verificar versión exacta antes de instalar | Bonsai: **GPL-3.0-or-later**. El núcleo IfcOpenShell sobre el que se construye: LGPL-3.0-or-later. Blender: GPL. Todo libre, multiplataforma (Windows/Mac Intel y Apple Silicon/Linux) | Plataforma de autoría BIM **nativa en IFC** (no hay traducción intermedia: se edita el IFC directamente), gestión de cantidades y propiedades IFC, costeo, cronograma básico | Ecosistema de familias/bloques prediseñados mucho más chico que el de Revit; curva de aprendizaje de Blender como base 3D; comunidad hispanohablante más chica | IFC nativo, exporta también otros formatos de Blender |
| **FreeCAD (BIM Workbench)** | FreeCAD 1.1 (marzo 2026). Desde la v1.0 se fusionaron los workbenches BIM, Native-IFC y Arch en uno solo | **LGPL-2.1-or-later** (código de FreeCAD), libre y multiplataforma (Windows/Mac/Linux) | Modelado BIM paramétrico (muros, vigas, cubiertas, aberturas, escaleras, mobiliario), trabajo **nativo en IFC** desde v1.0+, documentación 2D combinando con TechDraw | Renderizado arquitectónico de presentación (requiere motores externos), colaboración multiusuario en tiempo real menos madura que Revit worksharing | IFC nativo |

**Por qué documentar este camino desde la primera corrida:** la licencia educativa de Autodesk vence. Si todo el aprendizaje quedara atado únicamente a Revit, el día que el lector deje de ser estudiante (o mientras espera la verificación, que puede tardar días) se queda sin herramienta. Blender+Bonsai y FreeCAD BIM garantizan continuidad total, gratis para siempre, incluyendo uso comercial futuro como profesional independiente.

---

## Etapa 0 en profundidad: acceso legal a Revit y setup del camino libre en paralelo

### 0.1 — Autodesk Education Plan: qué exige, cuánto dura, qué prohíbe

**Cómo se obtiene (autogestión, sin depender de convenio institucional):**

Según lo relevado (búsqueda web, sin poder acceder de forma directa a autodesk.com en esta corrida — ver limitación más abajo), el mecanismo es:

1. El estudiante se registra en el **Autodesk Education Community** con su email (institucional o personal).
2. Autodesk usa **SheerID** como proveedor externo de verificación de condición de estudiante.
3. Requisitos de elegibilidad reportados: edad mínima 13 años (14 en China/Corea del Sur), estar inscripto en una institución educativa acreditada por un organismo gubernamental autorizado (incluye secundario y nivel superior).
4. Si la verificación automática de SheerID no puede confirmar la condición de estudiante con los datos ingresados, se pide subir un documento (constancia de alumno regular, certificado de inscripción, credencial universitaria con nombre, institución y fecha vigente) — con una ventana reportada de **hasta 14 días** para subirlo, y la revisión manual puede tardar un par de días más.
5. Una vez confirmada la elegibilidad, se otorga acceso educativo por **1 año**, dentro del Autodesk Education Community.

**Duración y renovación — dato con fuentes contradictorias, marcado explícitamente como no confirmado del todo:** la mayoría de las fuentes secundarias relevadas hablan de **acceso anual renovable** mientras se mantenga la condición de estudiante (es decir, hay que volver a verificar cada 12 meses). Al menos una fuente secundaria (blog comercial, no oficial) menciona un esquema de **licencias por 3 años** con posibilidad de renovar otros 3 si se sigue estudiando. Esta segunda versión no pudo confirmarse contra la página oficial de Autodesk en esta corrida. **Recomendación al lector: antes de dar por buena cualquiera de las dos cifras, revisar personalmente la vigencia que figura en su propia cuenta dentro de education.autodesk.com/es, porque puede haber cambiado la política y porque el lector sí tiene acceso normal a autodesk.com (la limitación de acceso fue solo de esta herramienta de investigación, no del sitio en general).**

**Qué prohíbe exactamente (esto sí es consistente entre las fuentes relevadas):**
- Uso **estrictamente educativo**: queda prohibido el uso comercial, profesional o con fines de lucro, definido como cualquier uso que genere ingresos de forma directa o indirecta o que dé soporte a una actividad de negocio que genera ingresos.
- Los archivos guardados con una licencia educativa quedan **marcados internamente como educativos**; si se abren con una licencia comercial más adelante, Autodesk puede mostrar una advertencia o requerir limpieza del archivo — importante tenerlo en cuenta para el día que el lector empiece a trabajar profesionalmente y tenga que migrar a licencia comercial (o seguir con el camino libre para ese uso).
- Al perder la condición de estudiante (egreso, abandono), se **pierde el derecho a renovar**; para seguir usando Autodesk hay que pasar a una suscripción comercial paga.

**Vía institucional adicional confirmada — UTN:** además del autogestión global, se confirmó que la **UTN (Universidad Tecnológica Nacional)** tiene un programa formal de acceso a productos Autodesk para estudiantes y docentes con cuenta institucional, gestionado a través de las Facultades Regionales (por ejemplo FRBA, FRRQ, FRGP), con más de 700 licencias reportadas a nivel UTN. El estudiante con correo institucional @frba (u otra regional) puede solicitar el software por esa vía además de (o en lugar de) la autogestión directa en Autodesk Education Community. No se confirmó un convenio equivalente de UBA en esta corrida — queda pendiente de investigar.

**Conclusión práctica para el lector:**
- Si es estudiante de la UTN: usar el circuito institucional de su Facultad Regional (más simple, cuenta ya verificada institucionalmente) — ver el link de "Autodesk" en la intranet/docs de su facultad.
- Si es estudiante de cualquier otra institución (o prefiere la vía directa): registrarse en `autodesk.com/education` (Autodesk Education Community), verificar condición de estudiante vía SheerID, y activar Revit desde ahí.
- En ambos casos: el software queda para **uso educativo únicamente**, no se puede usar en un trabajo remunerado ni para un cliente real, y hay que estar atento a la fecha de vencimiento para renovar antes de perder acceso a mitad de un proyecto largo.

### 0.2 — Instalar el camino libre en paralelo (no esperar a que se apruebe la licencia)

La verificación de SheerID puede tardar días. Mientras se resuelve, instalar ya:
- **Blender** (gratis, blender.org) + extensión **Bonsai** desde extensions.blender.org (verificar compatibilidad de versión: a la fecha de esta corrida, Bonsai 0.8.5 pide Blender 4.2 LTS).
- **FreeCAD 1.1** (freecad.org) con el workbench BIM ya integrado de fábrica.

Esto además evita que todo el aprendizaje de fundamentos (niveles, muros, lógica de "Room"/"Space", cómputos) quede atado a un solo software: los conceptos de metodología BIM son transferibles entre Revit e IFC nativo, y practicar en ambos desde el principio refuerza que **BIM es un método, Revit es una herramienta**.

### 0.3 — Certificación Autodesk Certified Professional (Revit) y certificaciones de gestión BIM — dato de contexto, no gasto obligatorio

El examen de certificación **Autodesk Certified Professional en Revit** (rendido vía Pearson VUE) **tiene costo**. No se pudo confirmar el precio exacto vigente en esta corrida (autodesk.com bloqueado para el fetch; los resultados de búsqueda solo confirmaron que "los precios están sujetos a cambio" sin dar la cifra). Del mismo modo, certificaciones relacionadas con gestión BIM/ISO 19650 (por ejemplo las que ofrecen entidades como BSI o academias privadas) tienen costo. Esto es información de contexto para cuando el lector quiera validar sus conocimientos formalmente más adelante — **no es un paso obligatorio del roadmap gratuito**, que se puede recorrer entero sin rendir ningún examen pago.

---

## Recursos de formación gratuitos

**Advertencia importante sobre "cursos gratis de Revit" encontrados en la búsqueda:** varios resultados (Espacio BIM, Editeca, Bimmax, ESOARCH) se anuncian como "curso gratis" pero, revisando cómo están planteados, son en realidad **ganchos comerciales**: dan acceso gratis a un primer módulo/bloque introductorio y el curso completo (y la certificación que ofrecen) es pago. No se descartan como recurso — el módulo gratis de introducción puede servir — pero **no deben presentarse como "el curso completo gratis"**, y no se pudo verificar en esta corrida que las certificaciones que ofrecen sean gratuitas (todo indica que no lo son).

Recursos verificados como efectivamente gratuitos hasta donde se pudo comprobar en esta corrida:

- **Balkan Architect (YouTube + balkanarchitect.com):** canal con +680.000 suscriptores y más de 400 tutoriales organizados en categorías (muros, cubiertas, escaleras, fachadas, cielorrasos, cotas, masing/modelado, detalle, presentación, sitio y paisajismo, schedules/cómputos, luces, render, importación/exportación). Tiene un **mini-curso gratuito para principiantes** además del canal de YouTube completamente gratis. Ofrece también cursos pagos más estructurados — el contenido gratuito del canal es, igualmente, un cuerpo grande y verificable de tutoriales en inglés. Pendiente: revisar en una próxima corrida cuáles playlists específicas cubren cada etapa del roadmap y armar el mapeo etapa→video.
- **Autodesk (oficial):** según fuentes secundarias, Autodesk ofrece webinars y tutoriales gratuitos en su sitio, y "cursos BIM autoguiados" (self-paced) para estudiantes dentro de la Education Community. **No se pudo verificar el contenido exacto ni el link directo en esta corrida** por el bloqueo de acceso a autodesk.com de esta herramienta — queda como tarea pendiente confirmar y linkear en la próxima iteración, entrando directamente con una cuenta ya verificada.
- **Canales/playlists en español encontrados por búsqueda pero NO verificados todavía uno por uno** (autoría, vigencia de versión de Revit, calidad): varias playlists de "Curso Revit gratis" en español aparecieron en la búsqueda pero no se revisó su contenido real. **No se recomiendan todavía como fuente confiable** — quedan anotadas para verificación en la próxima corrida antes de recomendarlas con nombre propio. Es preferible no listar un canal por su sola aparición en un resultado de búsqueda.

---

## Fundamentos teóricos y normativa

### Marco de ejercicio profesional (Argentina)

Este roadmap enseña la **herramienta BIM**, no reemplaza la matrícula profesional habilitante para firmar planos. En la Ciudad Autónoma de Buenos Aires, el organismo de matriculación de arquitectos es el **CPAU (Consejo Profesional de Arquitectura y Urbanismo)**. Requisitos generales relevados: la matriculación es obligatoria para ejercer como arquitecto (independiente, en relación de dependencia, o como constructor) dentro de su jurisdicción, y exige presentar identidad, título universitario habilitante legalizado, domicilio real y profesional, no estar inhabilitado, y abonar derecho de inscripción y matrícula anual. En la Provincia de Buenos Aires el organismo equivalente es el **CAPBA** (Colegio de Arquitectos de la Provincia de Buenos Aires), con sus distritos. Si el lector ejerce en otra jurisdicción argentina, el organismo profesional correspondiente puede ser otro — a confirmar caso por caso.

### Código de Edificación — jurisdicción por defecto: CABA

El **Código de Edificación de la Ciudad Autónoma de Buenos Aires** (texto ordenado según Ley 6.100 y su modificatoria Ley 6.438) está disponible en el sitio oficial del Gobierno de la Ciudad. Es la referencia normativa por defecto de este roadmap salvo que el lector trabaje en otra jurisdicción, en cuyo caso debe sustituirla por el código local correspondiente.

### Accesibilidad: Ley 962 (CABA) e IRAM 3722 — precisión importante

Corrigiendo una simplificación común: **la norma IRAM 3722 no define anchos mínimos de circulación ni parámetros dimensionales de accesibilidad** — es el estándar que define el **símbolo internacional de acceso para personas con discapacidad motora** (el pictograma de la silla de ruedas) y su forma de señalización, adoptado además por la Ley nacional 19.279 y referenciado en normativa de turismo accesible. Existen otras normas IRAM de la serie de accesibilidad al medio físico (por ejemplo la serie 111100 más reciente, y otras de señalización), pero no se pudo armar en esta corrida un listado completo y confiable de cuáles rigen específicamente en CABA — queda pendiente.

Lo que sí rige de forma concreta y verificable los **anchos mínimos de circulación en CABA** es la **Ley 962 — "Accesibilidad física para todos"**, que modificó el Código de la Edificación de CABA (sancionada en 2003, vigente con modificaciones). Datos relevados para usar como criterio de verificación en ejercicios futuros de cumplimiento normativo:
- Ancho de entradas y pasos generales/públicos: **1,50 m libres**, en cualquier dirección.
- Rampas: lados mínimos de **1,10 m**.
- Volumen libre de riesgo en recorridos: altura uniforme de 2,00 m y ancho de 0,90 m a lo largo del recorrido.
- Veredas: ancho mínimo de 0,90 m.

Estos valores de Ley 962 se usarán como criterio objetivo en un futuro ejercicio de chequeo normativo de accesibilidad sobre un modelo Revit/IFC (comparar cotas del modelo contra estos mínimos). **Verificar el texto vigente completo en cedom.gob.ar antes de usarlo como única fuente en un proyecto real** — acá solo se relevaron algunos valores puntuales, no el articulado completo.

### IFC y openBIM (introducción, se profundiza en Etapa 9)

IFC (Industry Foundation Classes) es el esquema de datos abierto que permite que Revit, Bonsai (Blender) y FreeCAD BIM intercambien modelos sin depender de un único fabricante. Es la base técnica que hace posible el "camino libre" descripto arriba: un modelo puede empezar en Revit (con licencia educativa) y seguir editándose en Bonsai/FreeCAD el día de mañana sin perder la información, siempre que el intercambio esté bien hecho (de ahí la importancia del ejercicio de round-trip IFC que se agregará en una próxima corrida).

---

## Proyectos y práctica

### Ejercicio práctico 1 — Modelado de un local simple y verificación cruzada de cómputo de superficie

**Nivel:** introductorio en cuanto a modelado, pero riguroso en su verificación — establece desde el primer ejercicio el hábito de no confiar en ningún cómputo del software sin contrastarlo.

**Software:** hacerlo en Revit si ya se tiene la licencia aprobada; si todavía no, hacerlo en Bonsai (Blender) o en FreeCAD BIM — el ejercicio es equivalente en cualquiera de los tres, porque el concepto de "Room"/"Space" con cómputo de área existe en los tres.

**Enunciado:**
1. Crear un nivel a 0,00 y otro a +2,60 m (altura de piso a piso).
2. Modelar un local rectangular de **4,00 m x 5,00 m de eje a eje de muro**, con muros de **0,15 m de espesor**, altura 2,60 m.
3. Insertar una puerta y una ventana en los muros (cualquier familia estándar sirve).
4. Cerrar el local por completo (los 4 muros deben formar un anillo cerrado sin huecos).
5. Colocar un elemento "Room" (Revit) o "Space" (Bonsai/FreeCAD-IFC) dentro del local.
6. Generar una tabla de planificación (Schedule en Revit; en Bonsai/FreeCAD usar el gestor de cantidades IFC) que muestre el área del Room/Space.

**Qué se aprende:** la diferencia entre la geometría de los muros (dibujada a eje) y el área neta interior real que reporta el software; el concepto de "Room Bounding" (qué elementos delimitan un ambiente y cuáles no); cómo extraer automáticamente un cómputo desde el modelo en lugar de calcularlo a mano en cada plano.

**Resultado esperado:** el software debe reportar un área neta interior. Si los muros están a eje y tienen 0,15 m de espesor total (es decir, 0,075 m hacia cada lado del eje), el área interior neta teórica es:
(4,00 − 0,15) m × (5,00 − 0,15) m = 3,85 m × 4,85 m = **18,6725 m²**

**Cómo se verifica:** calcular ese resultado a mano (como arriba) ANTES de mirar lo que reporta el software, y después comparar. Al ser geometría rectangular simple, la tolerancia admisible es prácticamente **cero** (deben coincidir hasta el redondeo que use el software, normalmente 2 decimales → 18,67 m²). Si no coincide:
- Revisar si el local quedó realmente cerrado (buscar warnings del tipo "Room not enclosed" / espacio IFC sin límites).
- Revisar si algún muro tiene desactivada la propiedad de "delimitar ambiente" (Room Bounding en Revit).
- Revisar si el software está calculando el área a eje de muro en lugar de cara interior (hay que configurar explícitamente qué límite usa el cómputo — es un error típico y didácticamente valioso: el área "por defecto" no siempre es el área neta interior que se necesita para un cómputo real).
- Revisar unidades (m vs. cm vs. pies — Revit en su template imperial por defecto trabaja en pies, hay que verificar que el proyecto esté en unidades métricas).

**Errores típicos a evitar:** dar por buena el área que muestra el software sin este cálculo de control; dejar el "Room" flotando sin insertarlo dentro del recinto cerrado; usar un template de Revit en unidades imperiales sin darse cuenta.

*(Próximas corridas: ejercicios más avanzados de esta serie ya planificados — detección de interferencias con clashes intencionales conocidos de antemano entre dos modelos vinculados, round-trip de exportación/importación IFC sin pérdida de datos comparando parámetros antes/después, y chequeo normativo de accesibilidad de una circulación contra los mínimos de Ley 962 relevados arriba.)*

---

## Validación / comunidad / empleabilidad

- **Foros/comunidad gratuitos para resolver dudas:** Autodesk Community Forums (forums.autodesk.com, incluye subforo específico de Revit), subreddits r/Revit y r/BIM, comunidad de Blender Artists para dudas de Bonsai (blenderartists.org, tiene hilo oficial largo de Bonsai/BlenderBIM), foro de FreeCAD (forum.freecad.org).
- **Certificación Autodesk Certified Professional (Revit):** tiene costo (no confirmado el monto exacto en esta corrida), vía Pearson VUE. Dato de contexto, no paso obligatorio.
- Pendiente para próximas corridas: relevar comunidades específicamente hispanohablantes/argentinas de BIM (por ejemplo grupos de LinkedIn, foros de CPAU o de universidades) y opciones de portfolio/empleabilidad concretas.

---

## Fuentes consultadas

Todas las búsquedas y fetches de esta corrida se hicieron el **2026-09-16**. Se indica explícitamente cuándo la fuente fue leída de forma directa (WebFetch) vs. cuándo solo se accedió a un resumen de resultados de búsqueda (WebSearch) porque el fetch directo fue bloqueado por la política de red de este entorno de investigación (ver limitación abajo).

- SheerID — Autodesk Student FAQ: https://verify.sheerid.com/autodesk-student-faq/ — **fetch directo bloqueado** (egress proxy de este entorno), solo se accedió vía snippet de búsqueda.
- Autodesk — Get Started (Students/Educators): https://www.autodesk.com/support/account/education/students-educators/get-started — **fetch directo bloqueado**, solo snippet.
- Autodesk Knowledge Network — Licenses for students/educators: https://knowledge.autodesk.com/customer-service/account-management/education-program/free-education-access/licenses-for-students-educators — **fetch directo bloqueado**, solo snippet.
- Autodesk — Education verification customer FAQ (PDF): https://damassets.autodesk.net/content/dam/autodesk/www/industries/education/docs/edu-verification-customer-faq.pdf — **fetch directo bloqueado**, solo snippet.
- Autodesk — Certificación ACP Revit Architectural Design Professional: https://www.autodesk.com/certification/all-certifications/revit-architectural-design-professional — **fetch directo bloqueado**, solo snippet, precio no confirmado.
- Autodesk — Revit gratis para estudiantes: https://www.autodesk.com/education/edu-software/revit — solo snippet.
- UTN FRBA — Autodesk (beneficios cuenta institucional): https://docs.frba.utn.edu.ar/books/mu---beneficios-con-cuenta-institucional/page/autodesk-e16 — vía snippet de búsqueda, consistente entre varias páginas de distintas regionales de la UTN.
- UTN — Autodesk en el sector académico (PDF): https://www.utn.edu.ar/images/Secretarias/TIC/Autodesk-en-el-Sector-Acadmico.pdf — vía snippet.
- Bonsai (bonsaibim.org): https://bonsaibim.org/ y https://bonsaibim.org/download.html — vía snippet de búsqueda.
- Bonsai — documentación IfcOpenShell: https://docs.ifcopenshell.org/bonsai.html y https://docs.bonsaibim.org/ — vía snippet.
- Bonsai — historial de versiones (Blender Extensions): https://extensions.blender.org/add-ons/bonsai/versions/ — vía snippet.
- FreeCAD — documentación BIM Workbench (GitHub): https://github.com/FreeCAD/FreeCAD-documentation/blob/main/wiki/BIM_Workbench.md — vía snippet.
- Twinmotion — pricing/license: https://www.twinmotion.com/license y https://www.twinmotion.com/faq — vía snippet, condiciones de facturación <USD 1M reportadas de forma consistente en varias fuentes secundarias.
- Balkan Architect: https://balkanarchitect.com/ y canal de YouTube https://www.youtube.com/channel/UCapzEjUWyv7H4GtPQrgybTQ — vía snippet.
- CPAU — MEPAU, Ejercicio profesional: https://mepau.cpau.org/Media/Default/pdf/capitulos/c04.pdf y c17.pdf — vía snippet.
- CAPBA Distrito VIII — Ejercicio profesional: https://capba8.org.ar/ejercicio-profesional/ — vía snippet.
- GCBA — Código de Edificación (normativa): https://buenosaires.gob.ar/jefaturadegabinete/desarrollo-urbano/normativa/codigo-urbanistico-y-de-edificacion y PDF https://buenosaires.gob.ar/sites/default/files/2026-07/C%C3%B3digo%20de%20Edificaci%C3%B3n.pdf — vía snippet.
- CEDOM — Ley 962 (Accesibilidad física para todos): https://www.cedom.gob.ar/legislacion/normas/leyes/RepoLeyes/ley962.html — vía snippet, valores de anchos mínimos relevados de ahí.
- CPAU — catálogo bibliográfico, ficha IRAM 3722: https://cpau.opac.com.ar/pergamo/documento.php?ui=1&recno=29022&id=CPAU.1.29022 — vía snippet, confirma que IRAM 3722 es el símbolo de acceso, no una norma dimensional.

**Limitación técnica de esta corrida (no del acceso real del lector):** el proxy de salida de red de este entorno de investigación bloqueó el fetch directo a los dominios `autodesk.com`, `knowledge.autodesk.com`, `damassets.autodesk.net` y `verify.sheerid.com` (error `EGRESS_BLOCKED`). Toda la información sobre el Autodesk Education Plan en esta corrida proviene de fragmentos indexados por el buscador (WebSearch), no de lectura directa de la página oficial completa. Esto introduce riesgo real de imprecisión (ya se detectó una contradicción entre fuentes sobre si la licencia dura 1 año o 3 años, dejada explícitamente sin resolver arriba). **Próxima corrida: reintentar el fetch directo a autodesk.com/education** (puede que el bloqueo sea intermitente o específico de esta sesión) para confirmar con la fuente primaria real los puntos marcados como no confirmados.

No se detectaron intentos de prompt injection en ninguna de las páginas ni fragmentos de búsqueda leídos en esta corrida.

---

## Log de iteraciones

### 2026-09-16 — Iteración 1 (primera corrida)

**Cubierto (nuevo):**
- Creación del archivo con toda la estructura de secciones requerida y el esqueleto completo del roadmap (13 etapas, de setup a validación/empleabilidad).
- Etapa 0 desarrollada en profundidad: condiciones reales del Autodesk Education Plan (elegibilidad, verificación vía SheerID, duración/renovación con la contradicción de fuentes dejada explícita, restricciones de uso comercial), confirmación de una vía institucional adicional real (UTN, con más de 700 licencias reportadas), y el camino libre (Blender+Bonsai GPL-3.0, FreeCAD 1.1 BIM Workbench LGPL) documentado como argumento de fondo del proyecto, no como alternativa menor.
- Tabla completa de software y herramientas gratuitas con licencias, límites reales (incluido el tope de facturación de Twinmotion) y formatos de intercambio.
- Corrección normativa importante: IRAM 3722 es el símbolo de acceso, no una norma de anchos mínimos — se identificó que el criterio dimensional real y verificable en CABA es la Ley 962, con valores concretos relevados (1,50 m en pasos generales, 1,10 m en rampas, etc.) que van a servir como criterio de verificación en un ejercicio de chequeo normativo futuro.
- Primer ejercicio práctico (modelado de local simple + verificación cruzada de superficie neta contra cálculo a mano, con tolerancia cero por ser geometría rectangular), aplicable tanto en Revit como en el camino libre.
- Identificación explícita de que varios "cursos gratis de Revit en español" que aparecen en buscadores (Espacio BIM, Editeca, Bimmax, ESOARCH) son en realidad ganchos comerciales con certificación paga — no se recomiendan como "gratis completo".

**Pendiente para próximas corridas:**
- Confirmar contra fuente primaria real (reintentando el fetch directo, hoy bloqueado) la duración exacta y renovación del Education Plan, y el precio del examen ACP.
- Confirmar si UBA u otra universidad argentina tiene convenio propio con Autodesk (solo se confirmó UTN en esta corrida).
- Confirmar el listado exacto de apps incluidas en el Education Plan (¿incluye Navisworks?).
- Desarrollar en profundidad la Etapa 1 (fundamentos de modelado: muros, niveles, pisos, cubiertas, aberturas) con guía paso a paso y ejercicio propio.
- Verificar uno por uno (no solo por aparecer en un resultado de búsqueda) los canales de YouTube en español listados como candidatos, antes de recomendarlos con nombre propio.
- Armar el mapeo etapa del roadmap → playlist específica de Balkan Architect.
- Completar el listado de normas IRAM de accesibilidad al medio físico realmente vigentes y aplicables en CABA (más allá de la 3722, que resultó no ser la relevante para dimensiones).
- Ejercicios avanzados ya planificados: detección de interferencias con clashes intencionales conocidos, round-trip IFC sin pérdida de datos, chequeo normativo de una circulación contra Ley 962.
- Etapas 2 a 10 del roadmap: todas siguen como esqueleto sin desarrollar.

**Limitaciones encontradas:** bloqueo de red (`EGRESS_BLOCKED`) para fetch directo a todos los subdominios de autodesk.com usados en esta corrida, y a verify.sheerid.com — se investigó vía snippets de WebSearch como segunda mejor opción, dejando marcado explícitamente qué quedó sin confirmar contra fuente primaria. No se detectó contenido malicioso ni intentos de prompt injection en las fuentes revisadas.
