# FitopatIA

La clínica de plantas y el laboratorio de fitopatología en tu navegador. Aplicación web de un solo fichero que acompaña la asignatura de **Fitopatología** (Carrera de Agropecuaria, Universidad Politécnica Estatal del Carchi) y sirve a cualquier estudiante de agronomía o protección vegetal.

**Usar la app:** https://fborrasumh.github.io/fitopatia/

**Idiomas:** español (por defecto), inglés y portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Sigue el sílabo de Fitopatología (0811BF4UP-AJ2025, nivel 4, PAO 2026 B): caracterizar agentes fitopatógenos, identificar signos y síntomas y su relación con el agente causal, y aplicar principios preventivos y de control. Todo funciona sin clave de IA salvo donde se indica. Cada estudiante escribe un código o alias y recibe sus propias hojas, problemas y datos; con el mismo código se reproducen los mismos ejercicios.

- **Agentes (parcial 1).** Triángulo de la enfermedad interactivo; importancia económica (pérdidas mundiales estimadas por Savary y col., 2019); fichas de hongos, oomicetos, bacterias, virus y viroides, fitoplasmas, nematodos y plantas parásitas (tamaño, estructura, penetración, dispersión, signos, diagnóstico y ejemplos andinos); «¿qué agente es?» y una línea del tiempo de la historia de la fitopatología para ordenar.
- **Signos y síntomas.** Atlas de ocho patrones dibujados por el código (mancha con halo, anillos concéntricos, roya, oídio, mosaico, tizón con esporulación, agallas, antracnosis); «¿qué ves?» con dibujos nuevos en cada ronda; clasificación de 25 observaciones como signo o síntoma (necrótico, hipoplásico, hiperplásico, de color o marchitez).
- **Clínica de plantas.** Diez casos de campo de cultivos andinos (papa, fréjol, haba, quinua, tomate de árbol, maíz), incluido un daño abiótico por helada: se inspecciona por partes, se decide el grupo de agente, el diagnóstico (entre 18) y la prueba de confirmación; pistas graduadas y tutor socrático con IA opcional. Ordenar los postulados de Koch.
- **Patometría.** Entrenador de severidad: hojas con lesiones cuya severidad mide el código punto a punto (la misma geometría que se dibuja), con error medio, sesgo y concordancia de Lin, con y sin escala diagramática. Problemas individualizados de incidencia, severidad media, índice de McKinney y ABCPE (trapecios); si la respuesta es errónea, el código recalcula los errores típicos (olvidar el grado máximo o los ceros, no dividir entre 2, porcentaje de sanas…) y dice cuál se cometió.
- **Dinámica poblacional.** Simulador monomolecular, logístico y de Gompertz con saneamiento (menos inóculo inicial) y resistencia o fungicida (menos r), con ABCPE y día del 50 %; ajuste de los tres modelos por linealización (R²) a datos propios de cada estudiante; problemas de tasa de infección aparente y del retraso por saneamiento (Van der Plank); riesgo de tizón tardío por clima con umbrales editables (criterio tipo «periodo de Smith»).
- **Ciclo y defensa (parcial 2).** Ordenar el ciclo de la enfermedad; monocíclicas y policíclicas; matriz de vías de penetración por agente; clasificación de 16 defensas (preexistentes o inducidas, estructurales o bioquímicas); gen a gen de Flor con variedades y razas generadas.
- **Manejo integrado.** Plan con 23 tácticas por principio (exclusión, erradicación, protección, resistencia, evasión, terapia, monitoreo) y categoría; el código avisa de tácticas que no actúan contra ese tipo de agente, de planes solo químicos o sin monitoreo. Programa de aplicaciones con grupo FRAC y riesgo de 18 productos: el código revisa objetivo (oomicetos frente a hongos verdaderos), mezclas del mismo grupo, productos de riesgo alto sin multisitio, más de dos aplicaciones seguidas del mismo grupo y más de un tercio del programa con un grupo de riesgo alto. Proyecto de aula (ABP) exportable a Word.
- **Lecturas, Simulacro y Progreso.** Lectura crítica de artículos (texto pegado, PDF o Word) con IA; simulacro de 15 preguntas por parcial barajadas por estudiante desde un banco de 37, corregido con la clave y con aciertos por tema; progreso por módulo exportable a Word, CSV y JSON (importable).

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude; se guarda solo en el navegador. La IA se usa solo en dos funciones y no calcula, no corrige ni pone notas:

- **Tutor de casos:** recibe lo inspeccionado y el razonamiento del estudiante, nunca la solución, y responde con preguntas. El código borra cualquier frase que nombre una enfermedad, un género o una sigla de la lista de diagnósticos, o que señale una opción.
- **Ficha de lectura:** cada punto lleva una cita literal; el código comprueba que aparece en el texto (✓ o ⚠) y avisa de las cifras que no están en él.

## Privacidad

Todo se procesa y se guarda en el navegador (IndexedDB). Solo sale texto hacia el proveedor de IA al usar sus dos funciones, con correos, números de identificación y teléfonos enmascarados y tras un aviso previo con una muestra de lo que sale. El JSON exportado no contiene la clave. Se recomienda usar un alias como código.

## Límites

- Es material de repaso elaborado a partir del sílabo: puede contener errores u omisiones. Mandan el profesor, el sílabo, el laboratorio y la etiqueta registrada de cada producto.
- Los dibujos son esquemas didácticos, no fotografías; los casos están simplificados y su descripción guía el diagnóstico más que en el campo.
- Las reglas del programa de aplicaciones son guías generales anti-resistencia; la lista de productos y su grupo FRAC es orientativa y no indica dosis, registro ni plazos de seguridad.
- Los umbrales de riesgo climático por defecto proceden de un criterio desarrollado fuera de los Andes; en la zona se usan sistemas adaptados.
- La lectura crítica de ejemplo usa un texto ficticio.

Probado con IA simulada de los tres proveedores (incluida una IA que chiva el diagnóstico, inventa una cita y una cifra y devuelve un error de saldo), en español, inglés y portugués, en escritorio y móvil. La severidad medida se contrastó con una estimación de Monte Carlo independiente y con el recuento de píxeles del dibujo; los problemas (McKinney, ABCPE, tasa logística y retraso) se compararon con fórmulas independientes en 400 variantes cada uno. **No se ha probado con una clave de API real.**

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Carlos David Herrera Ramírez (Universidad Politécnica Estatal del Carchi).

Sigue el sílabo de Fitopatología (0811BF4UP-AJ2025, nivel 4, Carrera de Agropecuaria, PAO 2026 B) del profesor Carlos David Herrera Ramírez.

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Carlos David Herrera Ramírez [0000-0001-6155-905X](https://orcid.org/0000-0001-6155-905X)

## Cómo citar

Borrás Rocher, F. y Herrera Ramírez, C. D. (2026). *FitopatIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
