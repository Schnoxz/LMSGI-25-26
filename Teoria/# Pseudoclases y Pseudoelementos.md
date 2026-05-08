# Pseudoclases y Pseudoelementos

Este conjunto de selectores CSS permite aplicar estilos basándose en estados específicos o partes concretas de un elemento, sin necesidad de modificar el HTML añadiendo clases manualmente.

## 1. Pseudoclases

### Definición
Una **pseudoclase** es un selector que marca los elementos que están en un **estado específico**. Actúan como si se hubiera aplicado una clase en una parte determinada del documento cuando se cumple cierta condición (por ejemplo, cuando el cursor pasa por encima).

Ayudan a reducir el exceso de clases en el HTML y proporcionan un marcado más flexible y mantenible.

### Sintaxis
Las pseudoclases son palabras clave que comienzan con **dos puntos** (`:`):

:nombre-pseudoclase

### Ejemplos de uso y utilidad

* **Estilizar el primer elemento (`:first-child`)**: Permite seleccionar, por ejemplo, el primer párrafo dentro de un artículo sin necesidad de añadirle una clase `.first`.
    
    article p:first-child {
      font-size: 120%;
      font-weight: bold;
    }
    
    *Esto es útil si el contenido se genera dinámicamente (CMS) y no se puede editar el HTML.*

* **Interacción del usuario (Pseudoclases de acción)**:
    * `:hover`: Se aplica cuando el usuario pasa el cursor sobre un elemento (comúnmente enlaces).
    * `:focus`: Se aplica cuando el elemento es seleccionado mediante el teclado o clic.
    
    a:hover {
      color: hotpink;
    }

## 2. Pseudoelementos

### Definición
Un **pseudoelemento** actúa como si se hubiera añadido un **elemento HTML totalmente nuevo** en el marcado o permite seleccionar una parte específica de un elemento existente (como la primera línea de un texto), en lugar de aplicar una clase a todo el elemento.

### Sintaxis
Los pseudoelementos comienzan con **doble dos puntos** (`::`):

::nombre-pseudoelemento

*> **Nota:** Algunos navegadores soportan la sintaxis antigua de un solo dos puntos (`:`) para ciertos pseudoelementos por compatibilidad, pero la norma actual es `::`.*

### Ejemplos de uso y utilidad

* **Estilizar la primera línea (`::first-line`)**: Selecciona la primera línea de un bloque de texto. Es dinámico: si el ancho de la pantalla cambia y las palabras de la primera línea varían, el estilo se actualiza automáticamente.
    
    article p::first-line {
      font-size: 120%;
      font-weight: bold;
    }

* **Generar contenido (`::before` y `::after`)**: Se utilizan junto con la propiedad `content` para insertar texto o formas decorativas antes o después del contenido de un elemento, sin tocar el HTML.
    
    .box::before {
      content: "★ ";
      color: gold;
    }
    
    *Usos comunes: añadir iconos, flechas, o elementos estéticos vacíos.*

## 3. Diferencias Clave

| Característica | Pseudoclases (`:`) | Pseudoelementos (`::`) |
| :--- | :--- | :--- |
| **Función Principal** | Seleccionan elementos en un **estado** específico (ej. activo, visitado). | Seleccionan **partes** de un elemento o crean elementos virtuales. |
| **Similitud** | Actúan como si se aplicara una **clase** al elemento. | Actúan como si se insertara un **nuevo elemento** HTML (ej. un `<span>`). |
| **Sintaxis** | Un solo signo de dos puntos (`:hover`). | Doble signo de dos puntos (`::after`). |
| **Alcance** | Afecta a todo el elemento seleccionado. | Afecta a una sub-parte del elemento o añade contenido extra. |

## 4. Referencia de Selectores

### Tabla de Pseudoclases (Selección)

| Selector | Descripción |
| :--- | :--- |
| `:active` | Selecciona un elemento cuando está siendo activado (ej. al hacer clic). |
| `:checked` | Selecciona un `input` (radio o checkbox) marcado. |
| `:disabled` | Selecciona elementos de interfaz desactivados. |
| `:empty` | Selecciona elementos que no tienen hijos (ni texto ni etiquetas). |
| `:first-child` | Selecciona el elemento que es el primer hijo de su padre. |
| `:focus` | Selecciona el elemento que tiene el foco del teclado. |
| `:hover` | Selecciona el elemento sobre el que se pasa el cursor. |
| `:invalid` | Selecciona un `input` con contenido no válido según su tipo. |
| `:last-child` | Selecciona el elemento que es el último hijo de su padre. |
| `:not()` | Selecciona elementos que **no** coinciden con el selector dentro del paréntesis. |
| `:nth-child()` | Selecciona elementos basándose en su posición numérica en la lista de hermanos. |
| `:required` | Selecciona elementos `input` que tienen el atributo `required`. |
| `:visited` | Selecciona enlaces que el usuario ya ha visitado. |

### Tabla de Pseudoelementos

| Selector | Descripción |
| :--- | :--- |
| `::after` | Crea un elemento virtual justo **después** del contenido del elemento seleccionado. |
| `::before` | Crea un elemento virtual justo **antes** del contenido del elemento seleccionado. |
| `::first-letter` | Selecciona únicamente la **primera letra** del bloque de texto. |
| `::first-line` | Selecciona únicamente la **primera línea** del bloque de texto. |
| `::selection` | Selecciona la parte del documento que ha sido resaltada/seleccionada por el usuario (ej. con el ratón). |
| `::marker` | Selecciona el marcador de un elemento de lista (el punto o número en `<ul>` o `<ol>`). |