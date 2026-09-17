# Camino a experto en Revit / BIM (arquitectura y diseño de interiores) — 100% gratis y legal

Proyecto de investigación continua para construir, corrida a corrida, la ruta completa hacia un nivel **experto** en Autodesk Revit y en metodología BIM aplicada a arquitectura y diseño de interiores, sin pagar nada, para un lector argentino que arranca **desde cero**.

Regla dura del proyecto: todo lo recomendado tiene que ser gratis y legal. La licencia educativa de Autodesk cuenta como gratuita y legal siempre que se respeten sus condiciones reales (uso estrictamente no comercial, vencimiento, verificación de condición de estudiante). **Nunca se recomiendan cracks, keygens ni "versiones full" pirateadas de Revit/Autodesk.**

Este documento se actualiza agregando contenido en cada corrida, nunca borrando ni resumiendo lo ya escrito. Ver el **Log de iteraciones** al final para el estado de avance.

---

## Roadmap de aprendizaje

Estructura general (se irá detallando etapa por etapa en corridas sucesivas; lo marcado como "cubierto en profundidad" ya tiene guía práctica más abajo, lo demás es esqueleto pendiente de desarrollo):

**Etapa 0 — Acceso legal a la herramienta (CUBIERTO EN PROFUNDIDAD en esta iteración, 2026-09-16)**
Conseguir Revit gratis y legal vía Autodesk Education Plan, entender sus condiciones reales, e instalar en paralelo el camino libre (Blender+Bonsai / FreeCAD BIM) que no caduca.

**Etapa 1 — Fundamentos de modelado arquitectónico (CUBIERTO EN PROFUNDIDAD en esta iteración, 2026-09-17)**
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
| **Navisworks** (Simulate/Manage) | — | **Confirmado en esta corrida (2026-09-17) vía snippets de búsqueda consistentes**: Navisworks figura explícitamente en el listado de software incluido en el Autodesk Education Plan, junto con AutoCAD, Civil 3D, Inventor, Fusion, 3ds Max, Maya, entre otros. Sigue sin poder confirmarse contra el fetch directo de la página oficial (bloqueado, ver limitaciones), pero la consistencia entre varios resultados de búsqueda independientes da razonable confianza. | Coordinación multidisciplinaria y detección de interferencias (clash detection) | NWC/NWD |

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

**Duración y renovación — contradicción de la corrida anterior resuelta parcialmente el 2026-09-17:** en esta iteración se repitió la búsqueda específicamente sobre este punto y **todas las fuentes encontradas ahora son consistentes en la cifra de 1 año**: "Access to the Autodesk Education plan will expire at the end of one year and can renew annually as long as the eligibility requirements are still met" (fraseo consistente entre la página oficial "Renewing Access" — autodesk.com/support/account/education/students-educators/renew —, el artículo "How to Renew Education Access" de Autodesk Knowledge Network, y varias fuentes secundarias). El proceso de renovación se puede iniciar hasta 30 días antes del vencimiento desde un botón "Renew Now" en el Autodesk Education Community, y típicamente pide volver a probar la condición de estudiante (credencial vigente, constancia, etc.). La cifra de "licencias por 3 años" mencionada en la corrida anterior por una única fuente secundaria no volvió a aparecer en esta búsqueda y se descarta como probable error o confusión con otro producto — **se mantiene igual la recomendación de revisar la fecha de vencimiento real dentro de la propia cuenta**, porque esto se relevó vía snippets de búsqueda (WebFetch directo a autodesk.com sigue bloqueado, ver limitaciones), no por lectura directa del texto legal completo.

**Dato adicional relevado hoy, no crítico para el lector individual pero relevante para el contexto institucional:** al menos una fuente indica que **a partir de marzo de 2026 Autodesk dejaría de ofrecer licencias nuevas de red/multi-puesto (network licenses)**, recomendando migrar a "Institution subscriptions". Esto podría afectar el mecanismo por el cual facultades como UTN o UBA-FADU distribuyen licencias a sus estudiantes (ver más abajo) — no se pudo profundizar en esta corrida qué tan vigente o específico es este cambio; queda anotado como algo a vigilar en corridas futuras si el lector reporta problemas con la vía institucional.

**Qué prohíbe exactamente (esto sí es consistente entre las fuentes relevadas):**
- Uso **estrictamente educativo**: queda prohibido el uso comercial, profesional o con fines de lucro, definido como cualquier uso que genere ingresos de forma directa o indirecta o que dé soporte a una actividad de negocio que genera ingresos.
- Los archivos guardados con una licencia educativa quedan **marcados internamente como educativos**; si se abren con una licencia comercial más adelante, Autodesk puede mostrar una advertencia o requerir limpieza del archivo — importante tenerlo en cuenta para el día que el lector empiece a trabajar profesionalmente y tenga que migrar a licencia comercial (o seguir con el camino libre para ese uso).
- Al perder la condición de estudiante (egreso, abandono), se **pierde el derecho a renovar**; para seguir usando Autodesk hay que pasar a una suscripción comercial paga.

**Vía institucional adicional confirmada — UTN:** además del autogestión global, se confirmó que la **UTN (Universidad Tecnológica Nacional)** tiene un programa formal de acceso a productos Autodesk para estudiantes y docentes con cuenta institucional, gestionado a través de las Facultades Regionales (por ejemplo FRBA, FRRQ, FRGP), con más de 700 licencias reportadas a nivel UTN. El estudiante con correo institucional @frba (u otra regional) puede solicitar el software por esa vía además de (o en lugar de) la autogestión directa en Autodesk Education Community.

**Vía institucional adicional confirmada — UBA / FADU (nuevo hallazgo, 2026-09-17):** se confirmó que la **Facultad de Arquitectura, Diseño y Urbanismo (FADU-UBA)** tiene un convenio de colaboración tecnológica propio con Autodesk (reportado inicialmente en un artículo de La Nación) para instalar el software en las computadoras de la institución con soporte técnico y actualizaciones permanentes, con una cifra reportada de aproximadamente **11.000 estudiantes de FADU beneficiados**, y un ahorro estimado por Autodesk de unos USD 2.000/año por estudiante durante los 5 años de la carrera. **Esto se relevó solo vía snippets de búsqueda de fuentes secundarias (un medio periodístico), no se pudo confirmar contra una página oficial de FADU ni de Autodesk con el detalle operativo (cómo se tramita, si es exactamente el mismo Education Plan o un acceso institucional distinto)** — el estudiante de FADU debería consultar la vía interna de la facultad (por ejemplo a través de campusgrado.fadu o del área de informática) para el procedimiento exacto, en vez de asumir que es idéntico al trámite de autogestión individual.

**Conclusión práctica para el lector:**
- Si es estudiante de la UTN o de FADU-UBA: preguntar primero por el circuito institucional de la propia facultad (potencialmente más simple, cuenta ya verificada institucionalmente) antes de tramitar la vía individual.
- Si es estudiante de cualquier otra institución (o prefiere la vía directa): registrarse en `autodesk.com/education` (Autodesk Education Community), verificar condición de estudiante vía SheerID, y activar Revit desde ahí.
- En ambos casos: el software queda para **uso educativo únicamente**, no se puede usar en un trabajo remunerado ni para un cliente real, y hay que estar atento a la fecha de vencimiento para renovar antes de perder acceso a mitad de un proyecto largo.

### 0.2 — Instalar el camino libre en paralelo (no esperar a que se apruebe la licencia)

La verificación de SheerID puede tardar días. Mientras se resuelve, instalar ya:
- **Blender** (gratis, blender.org) + extensión **Bonsai** desde extensions.blender.org (verificar compatibilidad de versión: a la fecha de esta corrida, Bonsai 0.8.5 pide Blender 4.2 LTS).
- **FreeCAD 1.1** (freecad.org) con el workbench BIM ya integrado de fábrica.

Esto además evita que todo el aprendizaje de fundamentos (niveles, muros, lógica de "Room"/"Space", cómputos) quede atado a un solo software: los conceptos de metodología BIM son transferibles entre Revit e IFC nativo, y practicar en ambos desde el principio refuerza que **BIM es un método, Revit es una herramienta**.

### 0.3 — Certificación Autodesk Certified Professional (Revit) y certificaciones de gestión BIM — dato de contexto, no gasto obligatorio

El examen de certificación **Autodesk Certified Professional en Revit** (rendido vía Pearson VUE / Certiport) **tiene costo**. En esta corrida (2026-09-17) se relevó, vía snippets de búsqueda (no fuente oficial directa, WebFetch a pearsonvue.com y autodesk.com no se probó pero autodesk.com sigue bloqueado), una cifra aproximada de **entre USD 180 y USD 200**, con la aclaración explícita de varias fuentes de que **el precio varía por país/región y puede tener impuestos adicionales** — el lector debe confirmar el monto exacto en su región directamente en certiport.com o pearsonvue.com antes de inscribirse, no tomar esta cifra como definitiva. Existen certificaciones separadas por disciplina (Revit Architectural, Structural, Mechanical, Electrical Design), cada una con su propio examen y costo. Del mismo modo, certificaciones relacionadas con gestión BIM/ISO 19650 (por ejemplo las que ofrecen entidades como BSI o academias privadas) tienen costo. Esto es información de contexto para cuando el lector quiera validar sus conocimientos formalmente más adelante — **no es un paso obligatorio del roadmap gratuito**, que se puede recorrer entero sin rendir ningún examen pago.

---

## Etapa 1 en profundidad: fundamentos de modelado arquitectónico

Esta etapa es la base de todo lo demás: si los conceptos de esta sección quedan mal entendidos, cualquier ejercicio posterior (documentación, interiores, familias, BIM colaborativo) hereda el error. El orden sugerido abajo no es arbitrario — cada bloque depende del anterior tal como está pensado el flujo real de modelado en Revit (y de forma equivalente en Bonsai/FreeCAD BIM, donde la jerarquía Project → Storeys/Niveles → elementos hosteados es la misma idea con otro nombre).

### 1.1 — Interfaz y estructura de un proyecto

Antes de dibujar nada, hay que entender **dónde vive cada cosa** en Revit:
- **Project Browser** (panel izquierdo): árbol de todas las vistas, hojas (sheets), familias y grupos del proyecto. Es la forma de navegar entre plantas, cortes, 3D y hojas de documentación — no hay "un archivo por plano" como en AutoCAD, hay **un único modelo** con múltiples vistas de ese modelo.
- **Properties Palette** (panel derecho, o flotante): propiedades del elemento seleccionado (o de la vista activa si no hay nada seleccionado). Acá se cambia el nivel base de un muro, el tipo de puerta, el "View Range" de una planta, etc.
- **Ribbon**: organizado por pestañas de disciplina (Architecture, Structure, Systems, Insert, Annotate, View, Manage). Los comandos de modelado arquitectónico del día a día están casi todos en la pestaña **Architecture**.
- **View Control Bar** (barra al pie de cada vista): escala de vista, nivel de detalle (Coarse/Medium/Fine), estilo visual (Wireframe/Hidden Line/Shaded/Realistic), y el ícono clave de **Temporary Hide/Isolate** para aislar elementos mientras se modela sin borrar nada del modelo.
- **Concepto central que distingue Revit de un CAD:** cada elemento (muro, puerta, room) tiene **parámetros** (instancia y tipo) además de su geometría. Modelar bien en Revit es, en gran parte, decidir con qué parámetros describir cada elemento, no solo dibujarlo.

**Ejercicio de reconocimiento (no es el ejercicio de la corrida, es un calentamiento):** abrir un proyecto nuevo con el template arquitectónico métrico por defecto (`DefaultMetric.rte` o equivalente), y ubicar en la interfaz real: dónde se cambia el nivel de una vista de planta activa, dónde se ve la lista de niveles del proyecto, y dónde se agrega una vista 3D nueva.

### 1.2 — Niveles y grillas

- **Niveles (Levels):** solo se pueden crear o editar desde una **vista de sección o de elevación** — es un error clásico de principiante buscar el comando "Level" en una vista de planta y no encontrarlo. Cada nivel define una altura de referencia (ej: Nivel 0.00, Nivel +2.60) y, al crearlo, Revit ofrece generar automáticamente una vista de planta asociada a ese nivel (tildar "Make Plan View" si se necesita la planta).
- Buena práctica: nombrar los niveles con la altura real o un nombre funcional consistente con la documentación que se va a generar después (ej. "PB", "P1", "Cubierta") en vez de dejar "Level 1", "Level 2" por defecto — esto se hereda directamente en los rótulos de las hojas más adelante.
- **Grillas (Grids):** líneas de referencia estructural (ejes A, B, C.../1, 2, 3...), se crean en planta y se propagan automáticamente a todas las vistas verticales asociadas. No son obligatorias para un proyecto de interiorismo chico, pero son el estándar de coordinación cuando el proyecto se vincula con estructura — conviene practicarlas igual desde ahora porque en Etapa 6 (BIM colaborativo) son la referencia común entre disciplinas.
- **Error típico:** mover un nivel arrastrándolo en una vista de sección sin darse cuenta de que eso **cambia la altura de todo lo que está host-eado a ese nivel** (pisos, muros con "Base Constraint" en ese nivel). Si se necesita cambiar solo el nombre o la vista, no arrastrar la línea.

### 1.3 — Muros

- **Wall: Basic** (muro simple con capas: revoque, ladrillo, aislación, etc. definidas en "Edit Structure" del tipo de muro) vs. **Stacked Wall** (apilar varios muros básicos, ej. zócalo distinto del resto) vs. **Curtain Wall** (paños vidriados con mullions, típico de fachadas — se retoma en profundidad más adelante).
- **Location Line:** define si el muro se dibuja a eje, a cara exterior, a cara interior o al núcleo (core). Esto es exactamente lo que se probó en el Ejercicio 1 (ver más abajo) y es la causa más común de que un cómputo de superficie no cierre.
- **Constraints clave de un muro:** Base Constraint / Base Offset (a qué nivel arranca y con qué desfasaje) y Top Constraint / Top Offset o Unconnected Height (hasta dónde llega). Un error muy común de principiante es dejar todos los muros con altura fija ("Unconnected Height") en vez de vincularlos al nivel superior — si después se cambia la altura de piso a piso, los muros con altura fija **no se siguen** y hay que corregir uno por uno.
- **Wall Joins:** cuando dos muros se cruzan en una esquina, Revit intenta resolver el remate automáticamente; a veces hay que forzarlo con el comando "Edit Wall Joins" cuando quedan capas mal resueltas en la esquina (típico con muros de distinto espesor o distinta composición de capas).

### 1.4 — Pisos (Floors)

- Se dibujan como un contorno cerrado (sketch) sobre un nivel, con un tipo de piso que define sus capas (carpeta, contrapiso, etc.) y su espesor total.
- **Error típico:** dibujar el piso con el contorno **a eje de muro** en lugar de a cara interior — el piso queda "metido" dentro del espesor del muro o, al revés, deja un hueco. Conviene usar la herramienta "Pick Walls" con el offset correcto (normalmente hacia adentro, a cara interior del muro) en vez de dibujar líneas sueltas a mano.
- El piso también participa en el cómputo de "Room Bounding" si su borde coincide con el límite del Room — no es indispensable para que el Room calcule área (los muros ya delimitan en planta), pero sí es indispensable para cómputos de volumen o para secciones que muestren el piso terminado.

### 1.5 — Cubiertas / techos (Roof)

- **Roof by Footprint:** se dibuja el perímetro (normalmente heredado de los muros exteriores con "Pick Walls") y se asignan pendientes por tramo de borde (definiendo ángulo o, alternativamente, altura en la cumbrera). Es el método más usado para techos a dos aguas, un agua, etc.
- **Roof by Extrusion:** se dibuja un perfil en una vista de alzado y se extruye — útil para geometrías más irregulares que no parten de un perímetro cerrado.
- Techo plano transitable (terraza) suele modelarse en realidad como un "Floor" con pendiente (Shape Editing) en vez de como "Roof", porque estructuralmente y en documentación se lo suele tratar como una losa, no como cubierta inclinada — esta distinción conceptual conviene tenerla clara antes de elegir la herramienta.
- **Error típico:** dejar el offset de la cubierta respecto a los muros mal configurado, generando un alero de 0 cm sin darse cuenta, o dejar la cubierta "flotando" sin conectarla a los muros que debería apoyar.

### 1.6 — Puertas y ventanas

- Son familias **host-based**: no existen "sueltas", necesitan insertarse sobre un muro (o, en el caso de tragaluces, sobre un techo). Si se borra el muro anfitrión, la puerta/ventana se borra con él.
- La biblioteca por defecto de Revit trae tipos genéricos (dimensiones estándar) que casi nunca coinciden con carpintería real de catálogo argentino — para un proyecto real conviene, más adelante (Etapa 4, familias paramétricas), crear o descargar familias con las dimensiones comerciales reales que se van a especificar en obra. Para esta etapa alcanza con los tipos genéricos, ajustando ancho/alto por tipo o por instancia.
- **Tags (etiquetas):** las puertas y ventanas suelen numerarse automáticamente con un tag que referencia el "Mark" del tipo — esto es la base de la tabla de planificación de aberturas que se arma en Etapa 2 (documentación).

### 1.7 — Escaleras y barandas

- **Stair by Component:** el método moderno de Revit, arma automáticamente pisada, contrahuella y descansos a partir de definir el nivel base, el nivel de llegada, y ajustando la cantidad de escalones o la pisada/contrahuella deseada (Revit calcula el valor libre a partir de los otros dos y la altura entre niveles).
- Cuando se conecta correctamente entre dos niveles, Revit avisa si sobran o faltan escalones para llegar exacto al nivel superior — este aviso ("Multistory..." o el contador de "risers created / remaining") es en sí mismo una primera verificación automática de que la altura piso a piso es consistente con la contrahuella elegida (más abajo, en el ejercicio, esto se cruza además contra el código de edificación).
- **Barandas (Railings):** se generan automáticamente al crear la escalera con un tipo de baranda por defecto, pero conviene revisar su altura y separación de balaustres contra normativa de seguridad más adelante (Etapa 11, transversal).

### 1.8 — Rooms y Áreas

- Ya introducido en el Ejercicio 1: un **Room** es un elemento no geométrico que "lee" el cerramiento formado por muros (u otros elementos delimitantes) para calcular área, perímetro y volumen, y para alojar parámetros propios (nombre, número, acabados — clave para Etapa 3, interiores).
- **Room vs. Area:** "Area" es un esquema alternativo y más simple (usado típicamente para cómputos normativos de superficie, ej. FOT/superficie cubierta total) que se dibuja con líneas de área en vez de depender de muros — se retoma cuando se trabaje cómputo normativo (Etapa 10 / Etapa 11).
- Un Room que no está dentro de un recinto cerrado por elementos "Room Bounding" queda con área 0 o con un warning — este es, otra vez, el error más común y el que motiva el hábito de verificación del Ejercicio 1.

### 1.9 — Vistas y organización de proyecto

- Cada vista de planta tiene un **View Range** (rango de corte: nivel de corte, tope, y plano de vista inferior) que determina qué se ve y qué no en esa planta — un error clásico es no ver el dintel de una ventana alta, o ver de más el piso de arriba, por un View Range mal configurado.
- **View Templates:** permiten estandarizar cómo se ve una categoría de vistas (todas las plantas con la misma escala, mismo nivel de detalle, misma visibilidad de capas) — se retoma en Etapa 2 cuando se arma la documentación completa para imprimir.
- Organización recomendada desde el día uno del Project Browser: agrupar vistas de trabajo (borradores, vistas 3D de estudio) separadas de las vistas que van a terminar en una hoja, para no mezclar "vistas de trabajo interno" con "vistas de documentación final".

### Recursos gratuitos mapeados a esta etapa

- **Balkan Architect — mini-curso gratuito para principiantes** (`balkanarchitect.com/p/project-1-beginner-to-intermediate-level-course-2-01`): cubre, según su propia estructura de categorías relevada en esta corrida, exactamente los bloques de arriba (niveles, muros — incluyendo location line, tipos y capas, muros apilados —, techos, escaleras, cotas básicas). Es el recurso gratuito más sólido identificado hasta ahora para esta etapa específica.
- **Playlist completa de YouTube de Balkan Architect** (`youtube.com/playlist?list=PL1n-0H6b0FkVukVOsK0hM59edtQDKhh0A`): más de 400 videos organizados por categoría — para esta etapa, priorizar las categorías "Walls", "Roofs", "Stairs", "Massing and Modeling" antes que las de renderizado o presentación (que corresponden a etapas posteriores del roadmap).
- Recordar que Balkan Architect es un canal en **inglés**; para un lector que recién empieza con Revit y no domina el vocabulario técnico en inglés, puede convenir tener a mano un glosario español-inglés de términos de Revit (level=nivel, wall=muro, floor=piso/losa, roof=cubierta/techo, room=ambiente, stair=escalera, railing=baranda) antes de arrancar.

---

## Recursos de formación gratuitos

**Advertencia importante sobre "cursos gratis de Revit" encontrados en la búsqueda:** varios resultados (Espacio BIM, Editeca, Bimmax, ESOARCH) se anuncian como "curso gratis" pero, revisando cómo están planteados, son en realidad **ganchos comerciales**: dan acceso gratis a un primer módulo/bloque introductorio y el curso completo (y la certificación que ofrecen) es pago. No se descartan como recurso — el módulo gratis de introducción puede servir — pero **no deben presentarse como "el curso completo gratis"**, y no se pudo verificar en esta corrida que las certificaciones que ofrecen sean gratuitas (todo indica que no lo son).

Recursos verificados como efectivamente gratuitos hasta donde se pudo comprobar en esta corrida:

- **Balkan Architect (YouTube + balkanarchitect.com):** canal con +680.000 suscriptores y más de 400 tutoriales organizados en categorías (muros, cubiertas, escaleras, fachadas, cielorrasos, cotas, masing/modelado, detalle, presentación, sitio y paisajismo, schedules/cómputos, luces, render, importación/exportación). Tiene un **mini-curso gratuito para principiantes**, confirmado con URL propia: `https://balkanarchitect.com/p/project-1-beginner-to-intermediate-level-course-2-01` (título de la página: "Autodesk Revit - Free Beginner Mini-Course"), además del canal/playlist completo de YouTube gratis: `https://www.youtube.com/playlist?list=PL1n-0H6b0FkVukVOsK0hM59edtQDKhh0A`. El curso pago estructurado ("Beginner to Intermediate Level") es un producto aparte — el mini-curso y el canal de YouTube son gratis en sí mismos. Ver el mapeo etapa→categoría de tutoriales en la sección "Etapa 1 en profundidad" más abajo.
- **Learning Revit Online (learningrevitonline.com):** curso autoguiado con **10 módulos** enfocados en modelar un proyecto residencial simple desde cero, orientado a principiantes. Se relevó como aparentemente legítimo (sitio con varios años de antigüedad, sin señales de estafa según un verificador externo), pero **no se pudo abrir el sitio de forma directa en esta corrida** (WebFetch bloqueado para todo dominio probado, ver limitaciones) para confirmar de primera mano que el contenido completo es gratis y no solo un adelanto — queda marcado como candidato razonable pero no 100% verificado, a confirmar accediendo directamente antes de invertir mucho tiempo.
- **Autodesk (oficial):** se encontró una página llamada "Revit Fundamentals" (`autodesk.com/campaigns/education/revit-fundamentals`), descripta como curso gratuito autoguiado de 18 horas — pero el propio snippet de búsqueda indica que está pensado **para docentes de la India** ("training educators... in India"), por lo que no aplica directamente como recurso general para un estudiante argentino. No se encontró otro recurso "self-paced" oficial de Autodesk con alcance general confirmado en esta corrida — sigue pendiente, y sigue bloqueado el fetch directo a autodesk.com para revisar el catálogo completo de webinars/tutoriales dentro de la Education Community.
- **Canales/playlists en español encontrados por búsqueda pero NO verificados todavía uno por uno** (autoría, vigencia de versión de Revit, calidad): en esta corrida se repitió la búsqueda y aparecieron nuevos candidatos (ej. playlists tituladas "Curso Revit Completo 2026: De Principiante a Experto", "Curso básico Revit 2026 en español", entre otras) pero **de nuevo no se pudieron verificar** porque el fetch directo a YouTube tampoco fue posible en esta corrida (bloqueo total de WebFetch, ver limitaciones). **Se reitera: no se recomiendan todavía como fuente confiable por su sola aparición en resultados de búsqueda.** Quedan anotadas para intentar verificación (duración, fecha de publicación, calidad real del contenido, si son realmente completos o ganchos) en una corrida donde WebFetch esté disponible, o accediendo el propio lector y reportando cuáles resultaron útiles.

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

### Ejercicio práctico 2 — Vivienda unifamiliar de dos niveles: cómputo de superficie cubierta total y verificación normativa de la escalera

**Nivel:** avanzado dentro de la Etapa 1 — integra niveles, muros, pisos, cubierta, escalera, Rooms y vistas en un solo modelo, y agrega una verificación normativa (no solo geométrica) sobre un elemento del modelo.

**Software:** Revit (o, en el camino libre, Bonsai/FreeCAD BIM — la escalera "by component" de Revit no tiene equivalente 1:1 exacto en herramientas libres, así que si se hace en Bonsai/FreeCAD alcanza con modelar la escalera con la geometría de pisada/contrahuella ya calculada a mano, sin depender del asistente automático).

**Enunciado:**
1. Crear tres niveles: **PB (0,00 m)**, **P1 (+2,80 m)** y **Cubierta (+5,60 m)** — dos plantas de 2,80 m de piso a piso.
2. En PB, modelar el perímetro exterior de una vivienda simple de **8,00 m x 10,00 m de eje a eje**, muros exteriores de **0,20 m de espesor**, con al menos una puerta de acceso y dos ventanas.
3. Dividir el interior de PB en al menos **3 ambientes** (por ejemplo: estar-comedor, cocina, un local de servicio) con muros interiores de **0,10 m de espesor**, cada uno con su Room insertado.
4. Modelar una **escalera de dos tramos** que conecte PB con P1, salvando los 2,80 m de desnivel, usando el asistente "Stair by Component" (o el cálculo manual equivalente en el camino libre).
5. Replicar en P1 un esquema de ambientes simple (puede ser más simple que en PB, por ejemplo un único gran ambiente + el hueco de la escalera) y colocar los Rooms correspondientes.
6. Modelar una cubierta a dos aguas sobre el nivel Cubierta con "Roof by Footprint", apoyada en el perímetro de P1.
7. Generar una tabla de planificación (Schedule) de Rooms que totalice el área por nivel y el área total del proyecto.

**Qué se aprende:** a encadenar niveles-muros-pisos-escalera-cubierta como un modelo único y coherente (no como piezas sueltas); la diferencia entre modelar "una planta" y modelar "un edificio de varios niveles" donde cada nivel depende geométricamente de los constraints del anterior; cómo la escalera obliga a que la altura de piso a piso y la cantidad de escalones sean matemáticamente consistentes; y a usar una tabla de planificación como herramienta de cómputo agregado (no solo de un ambiente, sino de todo un nivel o todo el proyecto).

**Resultado esperado y cómo se verifica (dos verificaciones independientes, no una sola):**

1. **Cómputo de superficie — cruzado a mano contra la tabla de planificación.** Con muros exteriores de 0,20 m a eje y perímetro de 8,00 m x 10,00 m, el área bruta interior teórica (asumiendo por simplicidad que los tabiques interiores de 0,10 m restan superficie de circulación pero no del perímetro exterior) es:
   (8,00 − 0,20) m × (10,00 − 0,20) m = 7,80 m × 9,80 m = **76,44 m² de superficie bruta interior por nivel** (a cara interior de muro exterior, antes de descontar el espesor de los tabiques interiores).
   Sumar manualmente el área de cada Room individual que reporta la tabla de planificación de PB y compararla contra este valor: la suma debe ser **menor** a 76,44 m² (por el espesor de los tabiques interiores que consumen superficie), pero la diferencia debe ser explicable — calcular a mano cuántos m² deberían perderse por metro lineal de tabique interior de 0,10 m (longitud de tabiques interiores × 0,10 m) y verificar que 76,44 − (suma de Rooms) ≈ esa cifra, con una tolerancia razonable de un par de décimas de m² por redondeos de esquinas. Si la diferencia no se explica con ese cálculo, hay un Room mal delimitado o un muro con la propiedad "Room Bounding" desactivada.

2. **Verificación normativa de la escalera contra el Código de Edificación de CABA y contra la regla de confort de Blondel.** Con 2,80 m de desnivel entre PB y P1, si se elige por ejemplo una contrahuella de 0,175 m, la cantidad de escalones necesaria es 2,80 / 0,175 = **16 contrahuellas exactas** (15 huellas/pisadas intermedias más el escalón de llegada al nivel superior, que no lleva pisada propia). Verificar contra dos criterios objetivos independientes:
   - **Código de Edificación CABA (escaleras secundarias, dato confirmado en esta corrida contra fuente oficial CEDOM):** contrahuella máxima 0,20 m, pedada (huella) mínima 0,23 m, máximo 21 escalones consecutivos por tramo. Con 16 escalones en dos tramos de 8 cada uno, se cumple el máximo de 21 por tramo, y con contrahuella de 0,175 m se cumple el máximo de 0,20 m. **Nota importante para el lector:** este valor confirmado corresponde específicamente a "escaleras secundarias"; no se pudo confirmar en esta corrida el valor exacto para "escalera principal" de una vivienda unifamiliar (que podría tener un mínimo de pedada distinto) — antes de dar por válido el ejercicio contra un proyecto real, revisar el artículo específico del Código de Edificación vigente para el tipo de escalera que corresponda.
   - **Regla de Blondel (fórmula de confort, universal, no normativa argentina):** 2 × contrahuella + pedada debe estar aproximadamente entre 0,60 y 0,64 m. Con contrahuella 0,175 m, despejando una pedada de 0,28 m: 2×0,175 + 0,28 = 0,63 m → dentro del rango de confort.
   Con la pedada elegida (0,28 m en el ejemplo) y 8 contrahuellas por tramo, cada tramo tiene 7 huellas/pisadas propias (la octava contrahuella de cada tramo llega directamente al descanso o al nivel superior, que ya tienen piso, y no necesitan huella propia). Calcular el desarrollo horizontal de cada tramo (7 huellas × 0,28 m = 1,96 m) y verificar que ese desarrollo entra en la longitud de local disponible en el modelo — si no entra, hay que ajustar cantidad de escalones por tramo, agregar un descanso más largo, o revisar la pedada elegida, **antes** de aceptar lo que el asistente de Revit generó por defecto.

**Errores típicos a evitar:** dejar que el asistente de escalera elija automáticamente una contrahuella que da un número no entero de escalones (Revit permite igual generar la escalera con un remate irregular en el último escalón si no se verifica el conteo); no verificar el "Multistory Top Level" si se quiere que la escalera se replique en niveles superiores; olvidar volver a correr el cómputo de superficie después de mover un tabique (la tabla de planificación se actualiza sola, pero el cálculo a mano de control hay que rehacerlo si cambia la geometría); confundir la contrahuella máxima permitida (un techo, "no debe superar") con un valor objetivo a alcanzar (no hace falta llegar exactamente a 0,20 m, alcanza con no superarlo).

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

**Limitación técnica de la corrida del 2026-09-16:** el proxy de salida de red bloqueó el fetch directo a los dominios `autodesk.com`, `knowledge.autodesk.com`, `damassets.autodesk.net` y `verify.sheerid.com` (error `EGRESS_BLOCKED`).

**Limitación técnica de esta corrida (2026-09-17) — el bloqueo resultó ser MÁS AMPLIO de lo pensado:** se probó `WebFetch` contra `autodesk.com`, `education.autodesk.com`, `verify.sheerid.com`, `balkanarchitect.com` **y hasta `en.wikipedia.org`** (como control, para descartar que fuera un bloqueo específico de dominios de Autodesk) — **los cinco fueron rechazados con el mismo error `EGRESS_BLOCKED`**. Esto indica que en esta corrida la herramienta `WebFetch` estuvo bloqueada de forma general para el entorno de investigación (no es una restricción específica contra Autodesk/SheerID como se había supuesto la corrida anterior), y que toda la información nueva de esta corrida proviene **exclusivamente de fragmentos indexados por `WebSearch`**, sin ninguna lectura directa de página completa. Esto es más limitante que la corrida anterior y se deja constancia explícita: los datos marcados como "confirmados" en esta corrida lo están por **consistencia entre múltiples resultados de búsqueda independientes**, no por lectura de la fuente primaria completa. Sigue siendo preferible a no verificar nada, pero el lector debería confirmar personalmente cualquier dato crítico (fecha de vencimiento de su propia licencia, precio exacto del examen ACP) contra la fuente primaria completa, a la que sí tiene acceso normal.

**Próxima corrida:** reintentar `WebFetch` (puede que el bloqueo sea intermitente, ligado a la sesión o a una política temporal del entorno) para poder finalmente leer de forma directa `autodesk.com/education`, el Código de Edificación de CABA completo (para confirmar el valor de "escalera principal" que quedó sin resolver en el Ejercicio 2), y al menos uno de los canales de YouTube en español pendientes de verificación.

Nuevas fuentes consultadas en esta corrida (2026-09-17), todas vía `WebSearch` (snippets), por el bloqueo total de `WebFetch` explicado arriba:
- Autodesk — Renewing Access (Students/Educators): https://www.autodesk.com/support/account/education/students-educators/renew — vía snippet, confirma duración de 1 año renovable.
- Autodesk Knowledge Network — How to Renew Education Access: https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/How-to-Renew-Education-Access.html — vía snippet.
- Autodesk Knowledge Network — Extend Autodesk educational licenses: https://knowledge.autodesk.com/customer-service/account-management/education-program/renew-education-licenses — vía snippet.
- Pearson VUE — Autodesk Certification Exams: https://www.pearsonvue.com/us/en/autodesk.html — vía snippet, precio aproximado del examen ACP (no cifra oficial exacta confirmada).
- Autodesk — All Certifications, Revit Architectural Design Professional: https://www.autodesk.com/certification/all-certifications/revit-architectural-design-professional — vía snippet.
- La Nación — nota sobre convenio Autodesk/FADU-UBA: https://www.lanacion.com.ar/arquitectura/autodesk-nid208978/ — vía snippet, fuente periodística secundaria, no oficial de FADU ni de Autodesk — usar con cautela, confirmar procedimiento exacto por vía institucional de FADU.
- FADU-UBA — Información administrativa para estudiantes: https://www.fadu.uba.ar/informacion-administrativa-para-estudiantes/ — vía snippet, no se confirmó el detalle operativo del convenio Autodesk ahí.
- Autodesk — Revit Fundamentals (campaña educadores India): https://www.autodesk.com/campaigns/education/revit-fundamentals — vía snippet, descartado como recurso general por estar dirigido a docentes de India.
- Balkan Architect — Free Beginner Mini-Course: https://balkanarchitect.com/p/project-1-beginner-to-intermediate-level-course-2-01 — vía snippet (fetch directo bloqueado, ver limitación).
- Balkan Architect — playlist YouTube: https://www.youtube.com/playlist?list=PL1n-0H6b0FkVukVOsK0hM59edtQDKhh0A — vía snippet.
- Learning Revit Online: https://learningrevitonline.com/ y https://learningrevitonline.wordpress.com/revit-beginner-course/ — vía snippet, junto con verificación externa de legitimidad en ScamAdviser (https://www.scamadviser.com/check-website/learningrevitonline.com) — vía snippet, no verificado de primera mano.
- CEDOM — Código de la Edificación (escaleras, dimensiones): http://www2.cedom.gob.ar/es/legislacion/normas/codigos/edifica/index3.html — vía snippet, valores de contrahuella/pedada de escaleras secundarias relevados de ahí (0,20 m contrahuella máx., 0,23 m pedada mín., 21 escalones máx. por tramo).

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

### 2026-09-17 — Iteración 2

**Cubierto (nuevo):**
- **Etapa 1 desarrollada en profundidad** (interfaz y estructura de proyecto, niveles y grillas, muros —tipos, location line, constraints—, pisos, cubiertas por footprint/extrusión, puertas y ventanas como familias host-based, escaleras por componente y barandas, Rooms vs. Areas, vistas/View Range/View Templates), con recursos gratuitos mapeados específicamente a esta etapa (mini-curso gratuito de Balkan Architect confirmado con URL propia, playlist completa de YouTube).
- **Ejercicio práctico 2** (avanzado): modelado de una vivienda unifamiliar de dos niveles completa (niveles, muros exteriores/interiores, escalera de dos tramos, cubierta a dos aguas, Rooms en ambos niveles), verificado con **dos criterios objetivos independientes**: cómputo de superficie cruzado a mano contra la tabla de planificación (con explicación de la diferencia esperada por espesor de tabiques interiores) y verificación normativa de la escalera contra el Código de Edificación de CABA (contrahuella/pedada de escaleras secundarias, confirmado contra CEDOM) combinada con la regla de confort de Blondel.
- **Contradicción de la corrida anterior resuelta:** la duración de la licencia educativa de Autodesk se confirmó como 1 año renovable (no 3 años), con fuentes ahora consistentes; se relevó también el detalle del proceso de renovación (ventana de 30 días antes del vencimiento).
- **Navisworks confirmado** como incluido en el Autodesk Education Plan (antes quedaba pendiente).
- **Nueva vía institucional confirmada: FADU-UBA** tiene convenio de colaboración tecnológica propio con Autodesk (~11.000 estudiantes beneficiados según nota de La Nación) — con la salvedad explícita de que esto viene de una fuente periodística secundaria, no de una página oficial de FADU/Autodesk, y de que el procedimiento operativo exacto no se confirmó.
- Precio aproximado (no oficial, variable por región) del examen ACP Revit: USD 180–200.
- Dos nuevos recursos de formación evaluados: Learning Revit Online (candidato razonable, no verificado de primera mano) y la página "Revit Fundamentals" de Autodesk (descartada para este lector por estar dirigida a docentes de India).
- Se repitió la búsqueda de canales de YouTube en español y aparecieron nuevos candidatos, pero **se reitera la misma cautela de la corrida anterior**: no se recomiendan por nombre propio sin poder verificar su contenido real.

**Pendiente para próximas corridas:**
- Confirmar contra fuente primaria completa (cuando `WebFetch` esté disponible) el valor exacto de contrahuella/pedada para "escalera principal" en el Código de Edificación CABA (usado en el Ejercicio 2 con el valor de "escalera secundaria" como aproximación válida pero no exacta).
- Verificar de primera mano (no solo por snippet) el contenido real de Learning Revit Online y del mini-curso de Balkan Architect.
- Confirmar el detalle operativo del convenio FADU-UBA/Autodesk contra una fuente oficial de la facultad, no solo la nota periodística.
- Seguir sin poder verificar uno por uno los canales de YouTube en español — sigue pendiente desde la corrida anterior.
- Completar el listado de normas IRAM de accesibilidad al medio físico vigentes en CABA — sigue pendiente desde la corrida anterior.
- Ejercicios avanzados ya planificados y aún no desarrollados: detección de interferencias con clashes intencionales conocidos, round-trip IFC sin pérdida de datos, chequeo normativo de una circulación contra Ley 962.
- Etapa 2 (documentación técnica y planos) es la siguiente candidata natural para la próxima corrida, siguiendo el orden del roadmap.
- Etapas 3 a 10 del roadmap: todas siguen como esqueleto sin desarrollar.

**Limitaciones encontradas:** el bloqueo de red resultó ser **más amplio de lo identificado en la corrida anterior** — se comprobó con una prueba de control (fetch a en.wikipedia.org, sin relación con Autodesk) que `WebFetch` estuvo bloqueado de forma general en todo el entorno de esta corrida, no solo contra dominios de Autodesk/SheerID. Toda la información nueva de hoy proviene de snippets de `WebSearch`, con el riesgo de imprecisión que eso conlleva explícitamente señalado en cada punto donde aplica. No se detectó contenido malicioso ni intentos de prompt injection en las fuentes revisadas (fragmentos de búsqueda) de esta corrida.
