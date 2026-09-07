# progreso CAD-FEA — Camino a experto en CAD / CAE / FEA con recursos 100% gratuitos

Este archivo se actualiza de forma incremental por una rutina automática. Cada corrida AGREGA contenido nuevo; no se borra lo anterior. Regla dura del proyecto: **solo se releva y se recomienda lo que sea gratis y de acceso legal** (software libre, licencias gratuitas de estudiante/hobbyista/personal, cursos abiertos, material open access). Todo dato lleva URL y fecha de consulta. Si algo es incierto o la fuente es floja, se aclara explícitamente.

---

## Roadmap de aprendizaje

*Definido en la corrida del 2026-09-07. Es la hoja de ruta completa de cero a nivel experto. Las corridas siguientes van a profundizar cada etapa (guías prácticas, ejercicios, verificación) y a marcar el avance acá mismo, sin reescribir la estructura salvo que haga falta corregir algo.*

Convenciones: las horas son de dedicación efectiva de estudio + práctica, no calendario. "Criterio de superación" = cómo demostrarte a vos mismo (con evidencia revisable) que la etapa está lograda antes de pasar a la siguiente.

### Etapa 0 — Preparación del entorno de trabajo (5–10 h)
- **Qué saber hacer:** instalar y dejar funcionando la cadena de herramientas gratuitas completa: FreeCAD, un solver FEA (CalculiX vía PrePoMax, o Salome-Meca/Code_Aster), Gmsh, ParaView. Entender qué formato de archivo exporta cada programa y para qué sirve (STEP/IGES para geometría CAD neutra, INP para CalculiX/Abaqus, UNV y MED para Salome/Code_Aster, VTK/VTU para ParaView).
- **Herramientas:** FreeCAD, PrePoMax (incluye CalculiX en Windows), Gmsh, ParaView. Opcional en Linux: Salome-Meca completo.
- **Material:** páginas oficiales de descarga (ver sección Software).
- **Criterio de superación:** lograr un ciclo completo de prueba — crear un cubo simple en FreeCAD, exportarlo como STEP, mallarlo en Gmsh o en el preprocesador de PrePoMax, correr un análisis trivial y visualizar el resultado en ParaView — sin errores.

### Etapa 1 — Dibujo técnico y GD&T (20–30 h)
- **Qué saber hacer:** vistas normalizadas, cortes, acotado funcional, tolerancias dimensionales, introducción a GD&T (datums, planitud, perpendicularidad, posición) según ASME Y14.5 (o ISO 1101 si se prefiere la norma internacional — aclarar que son normas distintas, con diferencias de simbología).
- **Herramientas:** FreeCAD (workbench TechDraw) para producir planos 2D a partir de modelos 3D.
- **Material:** canales de YouTube gratuitos de GD&T (ver sección Recursos). *Pendiente de próxima corrida: buscar apuntes universitarios públicos en PDF sobre dibujo técnico normalizado (idealmente en español) y confirmar si existe una edición gratuita/de acceso abierto de la norma ISO 128 o equivalente — las normas ASME/ISO oficiales son de pago.*
- **Criterio de superación:** producir un plano completo (vistas, cortes, acotado GD&T) de una pieza mecánica simple (p. ej. una brida o un soporte en L) que sea entendible por un tercero sin ambigüedad.

### Etapa 2 — Modelado paramétrico sólido (40–60 h)
- **Qué saber hacer:** boceteo restringido (sketches con restricciones geométricas y dimensionales, sin sobre-restringir ni sub-restringir), operaciones de sólidos (extrusión, revolución, barrido, recubrimiento), árbol de features editable, patrones, superficies básicas.
- **Herramientas:** FreeCAD (workbenches Sketcher + Part Design).
- **Material:** wiki oficial de FreeCAD (Getting Started, Basic modeling tutorial) y repositorio oficial de documentación en GitHub.
- **Criterio de superación:** modelar 5 piezas mecánicas de complejidad creciente (desde un bulón hasta una carcasa con nervaduras) manteniendo el sketch siempre "fully constrained" (sin grados de libertad sueltos) y el árbol de features limpio y editable (poder cambiar una cota temprana sin que el modelo se rompa — "no romper el árbol").

### Etapa 3 — Ensambles y planos de conjunto (25–35 h)
- **Qué saber hacer:** ensamblar piezas con restricciones (coincidencia, concentricidad, distancia), detectar interferencias, generar despieces (BOM) y planos de conjunto.
- **Herramientas:** FreeCAD (workbench Assembly, nativo desde la rama 1.0/1.1).
- **Material:** wiki de FreeCAD, sección Assembly.
- **Criterio de superación:** ensamblar un mecanismo simple de al menos 5 piezas (por ejemplo una prensa de banco o un gato mecánico simplificado) con movimiento coherente y sin interferencias, y producir el plano de conjunto con lista de materiales.

### Etapa 4 — Mecánica de sólidos y resistencia de materiales (60–90 h)
- **Qué saber hacer:** esfuerzo y deformación, diagramas de esfuerzo cortante y momento flector, torsión, flexión, pandeo de columnas (Euler), círculo de Mohr, criterios de falla (Von Mises, Tresca), concentración de tensiones.
- **Herramientas:** ninguna de software todavía — esto es teoría con lápiz y papel/calculadora, y es la base indispensable para poder juzgar si un resultado de FEA tiene sentido físico.
- **Material:** MIT OpenCourseWare "Mechanics & Materials I" (2.001, Fall 2006) y "Mechanics and Materials II" (2.002, Spring 2004); MIT OCW "Mechanics of Materials" (3.11, Fall 1999, Prof. David Roylance, con notas de clase completas); libro gratuito online "Applied Mechanics of Solids" de Allan F. Bower (Brown University) en solidmechanics.org — texto completo gratuito publicado por el propio autor.
- **Criterio de superación:** resolver a mano al menos 10 problemas de resistencia de materiales de dificultad variada (vigas, ejes, columnas) y poder predecir el orden de magnitud de un resultado antes de correr cualquier simulación.

### Etapa 5 — Fundamentos matemáticos del método de elementos finitos (50–80 h)
- **Qué saber hacer:** formulación débil de ecuaciones diferenciales, funciones de forma, discretización, ensamblado de matrices de rigidez, condiciones de borde, tipos de elementos (barra, viga, placa, sólido) y su orden de interpolación.
- **Herramientas:** ninguna todavía (papel/Python opcional para armar un solver de barras 1D "a mano" como ejercicio pedagógico).
- **Material:** notas de clase "Introduction to Finite Element Methods" (IFEM) de Carlos A. Felippa, Universidad de Colorado Boulder (curso ASEN 5007) — *el origen académico está confirmado por múltiples fuentes secundarias, pero no pude verificar en esta corrida cuál es hoy la URL oficial vigente en colorado.edu porque el dominio está bloqueado por el proxy de red de este entorno; hay copias en circulación en sitios de terceros (pdfcoffee, scribd, epdf) que NO se recomiendan porque no está confirmado que sean redistribución autorizada — pendiente de próxima corrida verificar la página oficial actual del curso o del autor.* Complementar con MIT OCW 2.092/2.093 "Finite Element Analysis of Solids and Fluids I" (Fall 2009, Prof. Klaus-Jürgen Bathe) — notas de clase, exámenes y ejercicios completos y gratuitos.
- **Criterio de superación:** poder ensamblar a mano (o en una hoja de cálculo/Python simple) la matriz de rigidez de un sistema de 2-3 barras/resortes y resolver desplazamientos y reacciones, verificando contra la solución analítica.

### Etapa 6 — FEA lineal estática (60–90 h)
- **Qué saber hacer:** definir materiales, condiciones de contorno (empotramientos, apoyos), cargas (puntuales, distribuidas, presión), correr un análisis estático lineal, leer e interpretar tensiones de Von Mises, desplazamientos y factores de seguridad.
- **Herramientas:** PrePoMax + CalculiX (Windows, todo en uno) o Salome-Meca + Code_Aster (Linux, cadena completa CAD-malla-solver-post con GUI de Salome).
- **Material:** documentación oficial de PrePoMax (manual PDF), tutoriales del sitio comunitario FEA4free (verificar caso por caso que cada tutorial sea gratuito y no promocione software de pago), NPTEL "Introduction to Finite Element Method" (IIT Madras) y "Basics of Finite Element Analysis" — cursos gratuitos con video.
- **Criterio de superación:** el ejercicio de verificación de la viga en voladizo (ver sección Proyectos y práctica) con error menor al 5% contra la solución analítica de Euler-Bernoulli.

### Etapa 7 — Mallado y verificación de convergencia (30–40 h)
- **Qué saber hacer:** tipos de elementos (tetraedros vs. hexaedros, orden lineal vs. cuadrático), calidad de malla (aspect ratio, skewness), refinamiento local, estudios de convergencia de malla (h-refinement), estimación de error de discretización.
- **Herramientas:** Gmsh (mallador standalone, control fino de malla), mallador integrado de PrePoMax/Salome.
- **Material:** documentación oficial de Gmsh; *pendiente: relevar en una próxima corrida un tutorial gratuito específico de estudio de convergencia paso a paso.*
- **Criterio de superación:** repetir el ejercicio de la Etapa 6 con 3 densidades de malla distintas, graficar tensión máxima vs. número de elementos y mostrar que converge (curva que se aplana) hacia el valor analítico.

### Etapa 8 — No lineal, contacto, dinámica, fatiga y térmico (80–120 h)
- **Qué saber hacer:** no linealidad geométrica (grandes desplazamientos) y de material (plasticidad), contacto entre superficies, análisis modal y de vibraciones, análisis transitorio/dinámico, fatiga (curvas S-N, Goodman), acoplamiento térmico-estructural.
- **Herramientas:** CalculiX (soporta no lineal, contacto, dinámica, térmico) vía PrePoMax; Code_Aster (más completo en no lineal avanzado y fatiga).
- **Material:** *pendiente de relevamiento — es la etapa que más investigación específica va a necesitar en próximas corridas: buscar tutoriales gratuitos de contacto no lineal en CalculiX/PrePoMax y de fatiga en Code_Aster.*
- **Criterio de superación:** a definir con más detalle cuando se releven los recursos; como mínimo, correr un análisis modal simple (frecuencias naturales de una viga) y verificar contra la fórmula analítica de vibración de vigas.

### Etapa 9 — CFD básico (60–90 h)
- **Qué saber hacer:** fundamentos de mecánica de fluidos aplicados a CFD, mallado para CFD, condiciones de borde de flujo, turbulencia (introducción a RANS), correr un caso simple (flujo interno en un ducto, flujo externo sobre un perfil).
- **Herramientas:** OpenFOAM (GPL v3, nativo en Linux; en Windows requiere WSL — no hay versión nativa de Windows sin esa capa de compatibilidad), Gmsh o snappyHexMesh para mallado, ParaView para post-proceso.
- **Material:** tutoriales oficiales de OpenFOAM Foundation (openfoam.org) y de CFD Direct.
- **Criterio de superación:** reproducir un caso tutorial estándar de OpenFOAM (p. ej. flujo en cavidad o sobre un cilindro) y comparar el coeficiente de arrastre o el perfil de velocidad contra un valor de referencia publicado.

### Etapa 10 — Validación contra benchmarks y casos reales (40–60 h, transversal)
- **Qué saber hacer:** contrastar sistemáticamente cada resultado de simulación contra una solución analítica, un benchmark publicado o, idealmente, un ensayo físico propio. Documentar supuestos, condiciones de contorno y fuentes de error.
- **Herramientas:** las mismas de las etapas anteriores.
- **Material:** los "benchmarks NAFEMS" clásicos (viga en voladizo, placa con agujero, cilindro a presión) son publicaciones pagas de NAFEMS, pero los mismos problemas de referencia están reproducidos gratis en manuales de verificación de varios solvers (por ejemplo el "Verification Manual" de Ansys, que es de acceso público en ansyshelp.ansys.com aunque el software Ansys no lo sea, y en los casos de test que distribuye el propio CalculiX). *Aclarar explícitamente: usar esos manuales de verificación como fuente de problemas de referencia con solución conocida es gratis y legal — no requiere licencia del software comercial que los publicó, porque el dato es el enunciado y el resultado de referencia, no el software.*
- **Criterio de superación:** tener un cuaderno propio (carpeta de proyectos) con al menos 5 casos donde el resultado de FEA/CFD propio se comparó explícitamente contra un valor de referencia externo, con el error cuantificado.

### Etapa 11 — Portfolio y empleabilidad (continuo, en paralelo desde la Etapa 3)
- **Qué saber hacer:** documentar proyectos de forma profesional (memoria de cálculo, planos, capturas de simulación con contornos y leyenda, comparación contra teoría), publicar en un repositorio o portfolio público, participar de comunidades técnicas.
- **Herramientas:** GitHub/GitLab (gratis para repos públicos) para versionar modelos y memorias; foros oficiales de FreeCAD y de CalculiX/PrePoMax para pedir revisión de pares.
- **Material:** *pendiente de relevamiento: foros y comunidades específicas, y ejemplos de portfolios de ingeniería mecánica open source.*
- **Criterio de superación:** tener publicados al menos 3 proyectos completos (CAD + planos + FEA + verificación) documentados de forma que otra persona pueda entender el problema, el método y el resultado sin explicación oral.

**Total estimado:** aproximadamente 470–700 horas de dedicación efectiva desde cero hasta un nivel sólido de "profesional validado", sin contar el tiempo de las Etapas 8-10 que todavía no están completamente relevadas (ver pendientes).

---

## Software y herramientas gratuitas

*Tabla verificada por búsqueda web el 2026-09-07. "Límite de la licencia" indica condiciones a respetar, no un truco para evitarlas.*

| Herramienta | Función | Versión verificada (2026-09-07) | Plataformas | Licencia y límites | Formatos de intercambio relevantes |
|---|---|---|---|---|---|
| **FreeCAD** | CAD paramétrico 3D (sketches, sólidos, ensambles, planos 2D, y un workbench FEM básico) | 1.1.1 (rama estable 1.1, lanzada 24/03/2026 según fuentes secundarias — verificar en freecad.github.io/Website/download/ antes de instalar) | Windows, macOS, Linux, FreeBSD | LGPL-2.0-or-later. Software libre real, sin límite de uso comercial ni personal. | Exporta/importa STEP, IGES, STL, DXF; el workbench FEM exporta a formato INP (CalculiX/Abaqus) y UNV |
| **OpenSCAD** | CAD paramétrico por código (scripting), útil para piezas generadas algorítmicamente | 2021.01 (estable) — verificar si hay una release más nueva, esta búsqueda puede estar desactualizada | Windows, macOS, Linux | GPL-2.0-or-later | Exporta STL, OFF, AMF, 3MF, CSG |
| **KiCad** | Diseño electrónico (esquemático y PCB) — relevante si el proyecto mecánico incluye electrónica embebida | 10.0.0 (20/03/2026) | Windows, macOS, Linux | GPL v3+. Libre, uso comercial permitido sin restricciones. | STEP (para exportar modelos 3D de PCB a FreeCAD) |
| **PrePoMax** | Pre/post-procesador gráfico para CalculiX (mallado, condiciones de borde, visualización) | v2.6.0 estable (01/09/2026), v2.6.2 en desarrollo | Windows nativo; en Linux vía Wine | Gratuito y de código abierto (verificar licencia exacta en el repo — pendiente de confirmar en próxima corrida el tipo exacto, ej. MIT/GPL) | Importa STEP/IGES para geometría; exporta INP para CalculiX |
| **CalculiX (ccx)** | Solver FEA (lineal, no lineal, contacto, térmico, dinámico), compatible con formato de entrada tipo Abaqus | 2.23 (19/10/2025) | Windows, Linux, macOS (por lo general vía PrePoMax en Windows o compilación en Linux) | GPL. Libre, sin límite de tamaño de modelo (a diferencia de versiones gratuitas de software comercial). | INP como formato nativo de entrada; FRD como salida de resultados |
| **Salome-Meca** | Suite integrada: geometría, mallado, y GUI para Code_Aster | Se distribuyen binarios oficiales anuales de EDF (2024/2025); confirmar última versión en open-simulation-center.org antes de instalar | Oficialmente Linux (binario, Docker, Singularity); en Windows solo mediante ports de terceros no oficiales (ej. code-aster-windows.com) — **aclaración de licencia/soporte**: el port de Windows no es del equipo oficial de EDF, usar con cautela y verificar que siga siendo gratuito | LGPL (Salome) / GPL (Code_Aster). Libre. | Exporta/importa STEP, IGES, MED (formato nativo de intercambio de malla y resultados), UNV |
| **Code_Aster** | Solver FEA de EDF (Francia), muy completo: lineal, no lineal, contacto, fatiga, térmico, dinámico | Se actualiza junto con Salome-Meca | Linux nativo | GPL. Libre, usado en la industria (EDF lo usa para sus propias centrales). | MED, formato de comando propio (.comm) |
| **Gmsh** | Generador de mallas 2D/3D standalone, con motor de geometría propio y scripting | 4.15.0 (26/10/2025) | Windows, macOS, Linux | GPL. Libre. | Lee STEP/IGES/BREP; exporta MSH, UNV, INP (con plugins) |
| **ParaView** | Post-procesador y visualizador científico de campos (contornos, cortes, animaciones) | 6.01 (25/09/2025) | Windows, macOS, Linux | BSD 3-clause — la licencia más permisiva de todo el stack, permite uso comercial sin restricción. | Lee VTK/VTU/VTP, EnSight, y con plugins EXODUS, MED, FRD (CalculiX, con filtro) |
| **Elmer FEM** | Suite FEA multi-física (estructural, térmico, electromagnético, fluidos) con GUI propia (ElmerGUI) | 26.2.1 (29/04/2026, verificar porque el número de versión parece inusualmente alto para la fecha — confirmar en próxima corrida) | Windows, macOS, Linux | GPL v2+ (LGPL para elmersolver.lib). Libre. | Usa mallas de Gmsh; exporta a formato propio y VTU para ParaView |
| **OpenFOAM** | CFD (mecánica de fluidos computacional) | Versión 14 (rama OpenFOAM Foundation); existe también la rama openfoam.com (ESI) con numeración distinta — aclarar en próxima corrida cuál conviene para uso puramente gratuito sin ambigüedad de marca | Linux nativo; Windows solo vía WSL (no hay versión nativa) | GPL v3. Libre. | Formato de caso propio (OpenFOAM case); exporta a VTK para ParaView |

**Conexión entre el stack:** el flujo típico gratuito es FreeCAD (geometría, STEP) → Gmsh o mallador de PrePoMax/Salome (malla) → CalculiX o Code_Aster (solver, formato INP o MED/.comm) → ParaView (post-proceso, formato VTU/FRD). Para CFD: FreeCAD (geometría) → snappyHexMesh/Gmsh → OpenFOAM → ParaView.

**Pendiente de próxima corrida:** confirmar la licencia exacta de PrePoMax (el repositorio es de acceso abierto pero no verifiqué el archivo LICENSE puntual), y aclarar la diferencia entre las dos ramas de OpenFOAM (Foundation vs. ESI/openfoam.com) en términos de qué es gratis en cuál.

---

## Recursos de formación gratuitos

*Todos verificados por búsqueda web el 2026-09-07. Se marca explícitamente cuándo un recurso tiene alguna condición o limitación.*

### Mecánica de sólidos / resistencia de materiales
- **MIT OpenCourseWare — Mechanics & Materials I (2.001, Fall 2006)**: https://ocw.mit.edu/courses/2-001-mechanics-materials-i-fall-2006/ — Gratis, sin registro, con recursos descargables (notas, tareas). Consultado 2026-09-07.
- **MIT OpenCourseWare — Mechanics and Materials II (2.002, Spring 2004)**: https://ocw.mit.edu/courses/2-002-mechanics-and-materials-ii-spring-2004/ — Gratis, mismo esquema OCW. Consultado 2026-09-07.
- **MIT OpenCourseWare — Mechanics of Materials (3.11, Fall 1999, Prof. David Roylance)**: https://ocw.mit.edu/courses/3-11-mechanics-of-materials-fall-1999/ — Gratis, con notas de clase completas del profesor. Consultado 2026-09-07.
- **Applied Mechanics of Solids — Allan F. Bower (Brown University)**: https://solidmechanics.org/ — Libro de texto completo publicado gratis por el propio autor en su página oficial (no es una copia de terceros). Cubre desde fundamentos hasta FEM no lineal. Consultado 2026-09-07.

### Método de elementos finitos (teoría)
- **MIT OpenCourseWare — Finite Element Analysis of Solids and Fluids I (2.092/2.093, Fall 2009, Prof. K.J. Bathe)**: https://ocw.mit.edu/courses/2-092-finite-element-analysis-of-solids-and-fluids-i-fall-2009/ — Gratis, incluye notas de clase, exámenes resueltos, tareas y proyectos completos. Uno de los cursos de FEM más rigurosos disponibles gratis. Consultado 2026-09-07.
- **MIT OpenCourseWare — RES.2-002, Finite Element Procedures for Solids and Structures (Spring 2010)**: https://ocw.mit.edu/courses/res-2-002-finite-element-procedures-for-solids-and-structures-spring-2010/ — Videoclases completas, también del enfoque de Bathe. Consultado 2026-09-07.
- **NPTEL — Introduction to Finite Element Method (IIT Madras, Dr. R. Krishnakumar)**: https://nptel.ac.in/courses/112106135 — Gratis (SWAYAM/NPTEL, financiado por el gobierno indio, sin costo para ver contenido). Consultado 2026-09-07.
- **NPTEL — Finite Element Method (IIT Kharagpur, Prof. Biswanath Banerjee)**: https://nptel.ac.in/courses/112104116 — Gratis. Consultado 2026-09-07.
- **Introduction to Finite Element Methods (IFEM) — Carlos A. Felippa, Univ. de Colorado Boulder**: origen académico confirmado (curso ASEN 5007) pero **no pude verificar hoy la URL oficial vigente** porque colorado.edu está bloqueado por el proxy de red de este entorno. Hay copias en sitios de terceros (pdfcoffee.com, scribd.com, epdf.pub) que **no se recomiendan como fuente** hasta confirmar que la redistribución es autorizada por el autor — Felippa históricamente publicó estas notas gratis en la web de su propio curso, pero hay que confirmar la URL actual antes de citarla como recurso oficial. *Pendiente para la próxima corrida.*

### Dibujo técnico y GD&T
- Canales de YouTube identificados con contenido gratuito de GD&T: "GD&T Basics – Engineer Essentials" (https://www.youtube.com/@Gdandtbasics) y contenido de Engineers Edge (https://www.youtube.com/@engineersedge4822). **No verificado en profundidad todavía** — pendiente de próxima corrida mirar varios videos completos y confirmar que el contenido es técnicamente correcto y no solo publicidad de cursos pagos.
- **Aclaración importante:** los cursos oficiales de ASME sobre GD&T (basados en la norma ASME Y14.5) son de pago — no se recomiendan como recurso gratuito, se los menciona solo para que quede claro que existen y son la referencia "canónica" de pago si en algún momento se justifica invertir en ellos.
- *Pendiente: buscar específicamente apuntes universitarios en abierto (PDF) de dibujo técnico en español o inglés, y confirmar si la norma ISO 128 tiene alguna versión de acceso gratuito (las normas ISO en general son de pago).*

### FreeCAD (documentación oficial)
- **Wiki oficial de FreeCAD**: https://wiki.freecadweb.org/ — Documentación completa y gratuita, mantenida por la comunidad y el proyecto. Consultado 2026-09-07.
- **Getting Started**: https://wiki.freecadweb.org/Getting_started
- **Basic modeling tutorial**: https://wiki.freecadweb.org/Basic_modeling_tutorial
- **Repositorio de documentación en GitHub**: https://github.com/FreeCAD/FreeCAD-documentation

### Nota sobre edX/Coursera
Se verificó que el modo auditor (gratis, sin certificado) de edX en 2026 tiene ventanas de acceso más cortas que antes (en algunos cursos, solo 1-2 semanas), lo que lo hace menos confiable que MIT OpenCourseWare para estudio a largo plazo — OCW no tiene fecha de vencimiento ni requiere cuenta. **Recomendación:** priorizar MIT OCW y NPTEL sobre edX en modo auditor para este roadmap, precisamente porque son permanentemente gratis sin ventana de tiempo. Fuente: búsqueda web general sobre edX free courses 2026, consultada 2026-09-07 — no se identificó todavía un curso MITx de FEM específico disponible en auditor; pendiente de revisar en una próxima corrida si aparece alguno nuevo.

---

## Fundamentos teóricos

*(Sección para desarrollar en profundidad en próximas corridas, a medida que se cubran las Etapas 4 y 5 del roadmap con guías detalladas. Por ahora contiene solo los pilares identificados y sus fuentes gratuitas, ya listados arriba en Recursos de formación: mecánica de sólidos — Bower, MIT 2.001/2.002/3.11 —, y fundamentos matemáticos del FEM — Bathe, Felippa, NPTEL.)*

---

## Proyectos y práctica

### Ejercicio 1 (Etapa 1-2 del roadmap): pieza mecánica con plano acotado en GD&T
- **Enunciado:** modelar en FreeCAD (Sketcher + Part Design) un soporte en "L" de chapa doblada o mecanizado, de aproximadamente 80×60×40 mm, con dos agujeros de fijación y un rebaje. Generar en TechDraw un plano completo con: vista frontal, vista lateral, un corte, y acotado que incluya al menos una tolerancia geométrica (por ejemplo, posición de los agujeros respecto a un datum, y planitud de la cara de apoyo).
- **Qué se aprende:** boceteo restringido, árbol de features editable, generación de planos normalizados, aplicación real (no solo teórica) de un símbolo GD&T.
- **Resultado esperado:** un archivo FreeCAD (.FCStd) con el modelo 3D completamente restringido ("fully constrained", sin grados de libertad sueltos) y un PDF exportado del plano, legible sin ambigüedad por un tercero.
- **Verificación:** no hay solver involucrado acá — la verificación es por revisión de pares (foro de FreeCAD, o comunidad de dibujo técnico) o autorrevisión contra una checklist de dibujo técnico (¿todas las cotas necesarias están? ¿hay cotas redundantes o contradictorias? ¿el datum elegido tiene sentido funcional?).

### Ejercicio 2 (Etapa 6 del roadmap, ejercicio "ancla" de verificación): viga en voladizo bajo carga puntual
- **Enunciado:** modelar una viga en voladizo (cantilever) de sección rectangular constante (por ejemplo 20×10 mm de sección, 300 mm de longitud), empotrada en un extremo y con una carga puntual transversal en el extremo libre (por ejemplo 50 N). Mallarla y resolver un análisis estático lineal en CalculiX (vía PrePoMax) o en Code_Aster (vía Salome-Meca).
- **Qué se aprende:** todo el flujo CAD → malla → condiciones de borde → solver → post-proceso, y la aplicación práctica de la Etapa 4 (resistencia de materiales) para poder juzgar el resultado antes de mirar el software.
- **Solución analítica de referencia (verificación):** para una viga en voladizo de longitud L, módulo de elasticidad E, momento de inercia I, y carga puntual P en el extremo libre:
  - Deflexión máxima (en el extremo libre): δ = P·L³ / (3·E·I)
  - Tensión de flexión máxima (en el empotramiento, fibra extrema): σ = M·c / I = (P·L)·c / I, con c = mitad del alto de la sección.
  - Esta es la fórmula clásica de la teoría de vigas de Euler-Bernoulli, presente en cualquier libro de resistencia de materiales (incluido el material gratuito de Bower y de MIT 3.11 ya citado en Recursos de formación).
- **Resultado esperado y criterio de aceptación:** la deflexión y la tensión máxima que reporta el solver en el nodo/elemento correspondiente deben coincidir con la fórmula analítica con un error menor al 5% (con malla razonablemente fina). Si el error es mayor, antes de sospechar del solver hay que revisar: unidades consistentes (un error clásico es mezclar mm con N y MPa sin verificar consistencia), condición de empotramiento real (¿está restringiendo también rotación, o solo traslación?), y calidad/densidad de malla.
- **Error típico a evitar:** aplicar la carga puntual sobre un solo nodo en un modelo 3D sólido genera una concentración de tensión artificial en ese punto que no es representativa de la teoría de vigas (que asume carga en el eje neutro) — para comparar bien contra la fórmula analítica conviene mirar la tensión en una sección alejada del punto de aplicación de la carga y del empotramiento (principio de Saint-Venant), no justo en esos extremos.

*Pendiente de próxima corrida: agregar un tercer ejercicio de ensamble (Etapa 3) y empezar a diseñar el ejercicio de estudio de convergencia de malla (Etapa 7), que depende de tener resuelto primero el Ejercicio 2.*

---

## Validación, comunidad y empleabilidad

*(Sección vacía todavía — se desarrollará cuando el roadmap llegue naturalmente a la Etapa 11, o antes si en alguna corrida se encuentra información relevante de comunidades/foros gratuitos que valga la pena registrar ya. Candidatos identificados pero no verificados en esta corrida: foro oficial de FreeCAD, foro de PrePoMax/CalculiX. Pendiente de próxima corrida.)*

---

## Fuentes consultadas

Todas las fuentes de esta corrida (2026-09-07), vía búsqueda web (WebSearch), salvo que se indique lo contrario:

1. Wikipedia — FreeCAD: https://en.wikipedia.org/wiki/FreeCAD
2. FreeCAD — página oficial de descarga: https://freecad.github.io/Website/download/
3. GitHub — FreeCAD/FreeCAD releases: https://github.com/FreeCAD/FreeCAD/releases
4. MIT OCW — Mechanics & Materials I: https://ocw.mit.edu/courses/2-001-mechanics-materials-i-fall-2006/
5. MIT OCW — Mechanics and Materials II: https://ocw.mit.edu/courses/2-002-mechanics-and-materials-ii-spring-2004/
6. MIT OCW — Mechanics of Materials (3.11): https://ocw.mit.edu/courses/3-11-mechanics-of-materials-fall-1999/
7. MIT OCW — Finite Element Analysis of Solids and Fluids I (2.092/2.093): https://ocw.mit.edu/courses/2-092-finite-element-analysis-of-solids-and-fluids-i-fall-2009/
8. MIT OCW — RES.2-002 Finite Element Procedures: https://ocw.mit.edu/courses/res-2-002-finite-element-procedures-for-solids-and-structures-spring-2010/
9. NPTEL — Introduction to Finite Element Method: https://nptel.ac.in/courses/112106135
10. NPTEL — Finite Element Method (IIT Kharagpur): https://nptel.ac.in/courses/112104116
11. solidmechanics.org — Applied Mechanics of Solids, Allan F. Bower: https://solidmechanics.org/
12. Wikipedia / búsquedas — Salome-Meca / Code_Aster: https://open-simulation-center.org/downloads/salome/SALOME_MECA , https://www.code-aster.org/V2/spip.php?article303=
13. PrePoMax — descargas oficiales: https://prepomax.fs.um.si/downloads/
14. CalculiX — página oficial: https://www.calculix.de/
15. Wikipedia — Calculix: https://en.wikipedia.org/wiki/Calculix
16. Wikipedia — Gmsh: https://en.wikipedia.org/wiki/Gmsh
17. Wikipedia — Elmer FEM solver: https://en.wikipedia.org/wiki/Elmer_FEM_solver
18. ParaView — descarga y licencia oficiales: https://www.paraview.org/download/ , https://www.paraview.org/license/
19. OpenFOAM Foundation: https://openfoam.org/ y https://openfoam.org/download/
20. KiCad — licencias oficiales: https://www.kicad.org/about/licenses/
21. Wikipedia — OpenSCAD: https://en.wikipedia.org/wiki/OpenSCAD
22. FreeCAD — wiki de documentación oficial: https://wiki.freecadweb.org/ , https://wiki.freecadweb.org/Getting_started , https://wiki.freecadweb.org/Basic_modeling_tutorial
23. GitHub — FreeCAD-documentation: https://github.com/FreeCAD/FreeCAD-documentation
24. NAFEMS — página de publicaciones (confirmando que las publicaciones de benchmarks son de pago): https://www.nafems.org/publications/browse_buy/browse_by_topic/linear/p07/
25. Búsqueda general sobre GD&T gratuito (YouTube — Engineers Edge, GD&T Basics – Engineer Essentials) y sobre cursos ASME (de pago): resultados de WebSearch, sin URL única citable más allá de los canales mencionados en la sección de Recursos.
26. Búsqueda sobre IFEM de Carlos Felippa — intento de acceso directo a colorado.edu bloqueado por el proxy de red del entorno (EGRESS_BLOCKED); solo se pudieron ver resultados de búsqueda con copias de terceros, no la fuente oficial.
27. Búsqueda sobre edX free/audit 2026: resultados generales de WebSearch (onlinecerthub.com, course.careers), sin verificación de un curso MITx de FEM específico.

---

## Log de iteraciones

### 2026-09-07 — Primera corrida real
**Cubierto (nuevo):**
- Se diseñó el **roadmap completo de 12 etapas** (Etapa 0 a Etapa 11), de cero a experto, con horas estimadas, herramienta gratuita asociada, material de estudio y criterio de superación para cada una.
- Se relevó y verificó por búsqueda web la sección **Software y herramientas gratuitas**: FreeCAD, OpenSCAD, KiCad, PrePoMax, CalculiX, Salome-Meca, Code_Aster, Gmsh, ParaView, Elmer FEM, OpenFOAM — con versión, plataformas, tipo de licencia y formatos de intercambio.
- Se relevó y verificó la sección **Recursos de formación gratuitos**: cursos de MIT OpenCourseWare (mecánica de materiales y FEM de Bathe), NPTEL (dos cursos de FEM), el libro gratuito de Allan Bower (solidmechanics.org), documentación oficial de FreeCAD, y canales de YouTube de GD&T (estos últimos identificados pero sin verificación profunda de contenido todavía).
- Se agregaron **dos ejercicios prácticos concretos**: (1) pieza con plano GD&T en FreeCAD (Etapas 1-2), y (2) el ejercicio "ancla" de verificación FEA — viga en voladizo con solución analítica de Euler-Bernoulli para contrastar contra el solver (Etapa 6) — incluyendo el error típico de aplicar carga puntual y confundir concentración de tensión local con el resultado de teoría de vigas.

**Quedó PENDIENTE para próximas corridas:**
- Confirmar la URL oficial vigente de las notas IFEM de Carlos Felippa (colorado.edu está bloqueado por el proxy de red de este entorno; no usar las copias de terceros encontradas — pdfcoffee, scribd, epdf — sin confirmar antes que la redistribución es legítima).
- Confirmar la licencia exacta de PrePoMax (repo/archivo LICENSE puntual).
- Aclarar la diferencia entre las ramas OpenFOAM Foundation (openfoam.org) y OpenFOAM ESI (openfoam.com) en términos de qué es gratis en cada una.
- Verificar en profundidad (mirando contenido real, no solo el nombre del canal) los canales de YouTube de GD&T identificados, y buscar apuntes universitarios abiertos de dibujo técnico en PDF (idealmente en español).
- Relevar material específico para la Etapa 8 (no lineal, contacto, dinámica, fatiga, térmico) — quedó marcada como pendiente casi en su totalidad, es la etapa con menos recursos concretos todavía.
- Relevar comunidades/foros para la sección Validación, comunidad y empleabilidad (Etapa 11) — se nombraron candidatos (foro FreeCAD, foro PrePoMax/CalculiX) pero sin verificar actividad ni calidad.
- Diseñar el ejercicio de estudio de convergencia de malla (Etapa 7), que depende de tener primero resuelto y validado el Ejercicio 2.
- Agregar un ejercicio de ensamble (Etapa 3).
- Revisar si para 2026 existe algún curso MITx de FEM en edX (no se encontró ninguno en esta corrida, y de todos modos se decidió priorizar MIT OCW por no tener ventana de tiempo limitada).

**Limitaciones encontradas en esta corrida:**
- El dominio `colorado.edu` está bloqueado por el proxy de red de este entorno (error EGRESS_BLOCKED), lo que impidió verificar directamente la fuente oficial de las notas de Felippa.
- No se navegó ni verificó línea por línea el contenido completo de los videos de YouTube de GD&T listados — se los identificó por búsqueda pero falta confirmar calidad y corrección técnica.
- Las versiones de software listadas provienen de resultados de búsqueda web (no siempre de la página oficial abierta directamente), así que antes de instalar cualquier herramienta conviene reconfirmar la versión exacta en el sitio oficial correspondiente.
- No se detectó ningún intento de inyección de instrucciones en el contenido de las páginas revisadas en esta corrida.
