# Apuntes DAW: Lenguajes de Marcas y CSS

## 1. Evolución de los Lenguajes de Marca

* **GML (Década 1960):** Diferencia: Primer sistema en separar contenido de formato mediante etiquetas descriptivas para procesar documentos en distintos sistemas.
* **SGML (Década 1980):** Diferencia: Metalenguaje internacional (ISO 8879) que establece las reglas gramaticales para definir otros lenguajes mediante un DTD.
* **HTML (Década 1990):** Diferencia: Aplicación de SGML con etiquetas fijas diseñada para estructurar e intercambiar documentos científicos mediante hipervínculos.
* **XML (Década 1990):** Diferencia: Metalenguaje estricto simplificado de SGML para transporte y almacenamiento de datos que permite definir etiquetas personalizadas.
* **XHTML (Década 2000):** Diferencia: Versión de HTML 4.01 bajo reglas sintácticas de XML, obligando a un marcado punitivo y bien formado.
* **HTML5 (Década 2010):** Diferencia: Estándar actual independiente de SGML que introduce semántica avanzada, APIs y soporte multimedia nativo.

## 2. Diferencias Críticas y Formatos Relacionados

* **CSS:** Lenguaje de hojas de estilo, no de marcas. Describe la estética y presentación, no la estructura o semántica.
* **Markdown:** Lenguaje de marcas ligero centrado en la legibilidad humana que se convierte a HTML.
* **YAML:** Formato de serialización de datos basado en indentación; no es un lenguaje de marcas al no usar etiquetas.
* **SVG:** Aplicación de XML para describir gráficos vectoriales mediante texto y formas geométricas escalables.
| Característica | Lenguaje de Marca (XML/HTML) | Formato de Datos (JSON) | Estilo (CSS) |
| :--- | :--- | :--- | :--- |
| Sintaxis | Etiquetas `<tag>...</tag>` | Pares clave-valor `{"id": 1}` | Selectores y propiedades |
| Objetivo | Estructurar contenido | Intercambio de datos | Presentación visual |
| Extensibilidad | Alta (en XML) | Alta | Limitada |

## 3. Posicionamiento CSS (Property: position)

* **static:** Valor por defecto. El elemento sigue el flujo natural del documento.
* **relative:** Desplazamiento respecto a su posición original sin afectar al espacio de los demás elementos.
* **absolute:** Posicionamiento respecto al ancestro posicionado más cercano. Sale del flujo normal del documento.
* **fixed:** Posicionado respecto al viewport (ventana). Permanece visible independientemente del scroll.
* **sticky:** Comportamiento híbrido; se mueve con el scroll hasta alcanzar un umbral fijado (ej. top: 0).
* **z-index:** Controla la profundidad en el eje Z. Solo funciona en elementos con posición distinta a static.

## 4. Especificidad y la regla !important

El navegador resuelve conflictos de estilo sumando puntos según el tipo de selector:

* **Estilo en línea (Inline):** 1000 puntos.
* **ID (#id):** 100 puntos.
* **Clases, atributos y pseudo-clases (.clase, :hover):** 10 puntos.
* **Elementos y pseudo-elementos (p, ::after):** 1 punto.
* **!important:** Sobrescribe cualquier cálculo de especificidad anterior. Se debe usar con extrema precaución.

## 5. Reglas-Arroba (@-rules)

* **@media:** Estilos condicionales basados en características del dispositivo (Responsive Design).
* **@keyframes:** Define los fotogramas de una animación.
* **@font-face:** Permite cargar fuentes tipográficas externas.
* **@import:** Incluye una hoja de estilo externa dentro de otra.

## 6. Pseudo-clases (:) y Pseudo-elementos (::)

**Pseudo-clases (Estado o posición):**

* `:hover`: Elemento bajo el puntero del ratón.
* `:not()`: Excluye elementos que coincidan con el selector indicado.
* `:is()` / `:where()`: Agrupación de selectores para reducir redundancia.
* `:has()`: Selecciona un elemento basándose en su contenido (parent selector).
**Pseudo-elementos (Partes específicas):**
* `::before` / `::after`: Inserta contenido virtual antes o después del elemento (requiere `content`).
* `::first-letter`: Estiliza la letra inicial de un bloque de texto.
* `::selection`: Estiliza la parte del documento resaltada por el usuario.