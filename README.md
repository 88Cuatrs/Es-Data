# Es-Data

Este repositorio reúne el desarrollo de un lenguaje de análisis de datos cuya sintaxis está expresada de forma nativa en español. La propuesta busca reducir la barrera que puede producir una sintaxis basada en palabras clave en inglés y hacer más comprensibles los pasos habituales de preparación, transformación y análisis de información. No pretende eliminar la necesidad de aprender lógica o conceptos de programación: busca que la sintaxis sea más cercana para quienes piensan y trabajan en español.

## Enfoque

La meta es que un análisis pueda describir con claridad qué datos se cargan, qué transformaciones se aplican, qué cálculos se realizan y cómo se obtiene un resultado reproducible. El proyecto combina una sintaxis española con una implementación de runtime nativo y herramientas para trabajar con arreglos, tablas y estadísticas.

## Implementación y rendimiento

El núcleo está implementado principalmente en C17. La eficiencia de ejecución es uno de los objetivos de diseño, con la aspiración de ofrecer una alternativa rápida para tareas de análisis de datos frente a soluciones dinámicas como Python. Esa ventaja no se presenta como un resultado universal ya demostrado: depende de la carga, el entorno y las mediciones comparables. El repositorio incluye benchmarks y pruebas, pero toda afirmación de superioridad requiere publicar y reproducir comparaciones equivalentes.

## Desarrollo actual

El código contiene componentes de análisis léxico, parser, árbol sintáctico, validación semántica y runtime. El flujo canónico está integrado para varias rutas de ejecución, aunque la consolidación de todas las capacidades continúa en curso y todavía coexisten componentes de compatibilidad y módulos experimentales.

Entre las capacidades ya implementadas y probadas se encuentran:

- Creación y operaciones sobre arreglos numéricos, incluidas reducciones y estadísticas descriptivas.
- Carga de datos tabulares desde CSV, declaración de tipos de columna, limpieza de valores nulos y duplicados, filtros, columnas calculadas, agrupaciones, resúmenes y combinaciones de datos.
- Exportación de resultados y reportes en JSON.
- Perfiles estadísticos, histogramas y análisis como normalidad, correlación, Poisson, Wilcoxon, chi-cuadrado, riesgo relativo y odds ratio.
- Funciones iniciales para algunos análisis actuariales y cálculos financieros sencillos.
- Lectura secuencial de CSV para ciertos resúmenes con presupuestos explícitos de filas, memoria temporal y recursos. Algunas rutas admiten agrupación acotada y uso de almacenamiento temporal; no todas las operaciones tabulares funcionan en modo flujo.
- Una suite amplia de pruebas de componentes, validación del parser y ejecución de programas de ejemplo.

## Etapas experimentales y límites

Hay prototipos de bytecode, máquina virtual y compilación nativa para subconjuntos escalares acotados. No representan soporte completo del lenguaje ni permiten compilar cualquier programa. Las construcciones no cubiertas deben rechazarse explícitamente; no se presentan como capacidades terminadas.

El proyecto todavía no ofrece procesamiento distribuido, ejecución en clúster, garantías de latencia fija ni una ruta de streaming para todas las operaciones. Las funciones de alto nivel, la unificación completa del pipeline y la distribución de paquetes continúan evolucionando. Los paquetes y manifiestos de distintas plataformas requieren gates adicionales de publicación e instalación limpia; la existencia de scripts de empaquetado no significa que la instalación pública esté disponible.

## Compilación y pruebas

El repositorio incluye un sistema de construcción con Make. En un entorno compatible con C17, las comprobaciones generales se pueden ejecutar con:

```sh
make
make test
```

La validación automatizada cubre principalmente entornos Linux y Windows. La compatibilidad específica de Android/Termux requiere pruebas en el dispositivo y no debe inferirse solo de una compilación de escritorio.

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo `LICENSE` para ver sus términos.
