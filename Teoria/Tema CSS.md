# Guía Técnica de CSS: Posicionamiento, Especificidad y Selectores Avanzados

## 1. Posicionamiento (CSS Position)

Define el método de posicionamiento utilizado para un elemento.

* **static:** Valor por defecto. El elemento se posiciona siguiendo el flujo normal de la página. No responde a propiedades top, bottom, left o right.
* **relative:** Se posiciona relativo a su posición normal. Los desplazamientos (top, left, etc.) lo mueven sin afectar el espacio que ocupaba originalmente.
* **fixed:** Se posiciona relativo al viewport (ventana del navegador). No se mueve al hacer scroll y sale del flujo normal del documento.
* **absolute:** Se posiciona relativo al ancestro posicionado (non-static) más cercano. Si no existe, usa el cuerpo del documento. También sale del flujo normal.
* **sticky:** Alterna entre relativo y fijo según la posición de scroll del usuario. Se queda "pegado" al alcanzar un umbral definido.

## 2. Control de Profundidad (z-index)

Especifica el orden de apilamiento de los elementos en el eje Z.

* Solo funciona en elementos que tienen una propiedad `position` distinta a `static`.
* Los valores pueden ser positivos, negativos o cero.
* A mayor valor numérico, el elemento se dibuja más cerca del usuario (encima de los demás).
* Si dos elementos tienen el mismo z-index, se muestra encima el que aparece más tarde en el código HTML.

## 3. Especificidad de Selectores

Es el conjunto de reglas que el navegador utiliza para decidir qué valores de propiedad CSS son más relevantes para un elemento.

* **Puntuación por categorías:**
1. **Estilos en línea:** Atributo `style` dentro del HTML (1000 puntos).
2. **IDs:** Selectores como `#header` (100 puntos).
3. **Clases, Atributos y Pseudo-clases:** Selectores como `.menu`, `[type="text"]` o `:hover` (10 puntos).
4. **Elementos y Pseudo-elementos:** Selectores como `h1`, `div` o `::before` (1 punto).


* El selector con la suma total más alta gana. A igualdad de puntos, gana el que esté escrito más abajo en el archivo CSS.

## 4. La Regla !important

Se utiliza para invalidar cualquier otra declaración de estilo previa sobre una propiedad específica.

* No afecta a la puntuación de especificidad, sino que la ignora por completo.
* Solo se puede sobrescribir con otra regla que también contenga `!important` y que tenga una especificidad mayor o que esté situada después en el código.
* Su uso debe limitarse a casos donde sea imposible modificar la especificidad del selector original.

## 5. Reglas-Arroba (@-rules)

Instrucciones que indican al navegador cómo debe procesar o aplicar el código CSS.

* **@media:** Define reglas de estilo para diferentes tipos de dispositivos o tamaños de pantalla.
* **@keyframes:** Establece los pasos y estados de una animación CSS.
* **@font-face:** Permite importar y utilizar tipografías personalizadas desde archivos externos.
* **@import:** Importa reglas de estilo desde otra hoja de estilos externa.
* **@charset:** Especifica la codificación de caracteres utilizada en la hoja de estilos.
* **@supports:** Comprueba si el navegador es compatible con una característica específica de CSS.

## 6. Pseudo-elementos (::)

Se utilizan para dar estilo a partes específicas de un elemento o generar contenido decorativo.

* **::before / ::after:** Inserta contenido antes o después del contenido de un elemento. Requiere la propiedad `content`.
* **::first-letter:** Aplica estilos únicamente a la primera letra de un texto.
* **::first-line:** Aplica estilos a la primera línea visible de un párrafo.
* **::marker:** Selecciona el marcador de los elementos de una lista (el punto o número).
* **::selection:** Estiliza la parte del texto que el usuario ha seleccionado/resaltado.
* **::placeholder:** Selecciona el texto de ayuda dentro de elementos de entrada (`input` o `textarea`).