ºz# **Lenguaje de Marcas y CSS** 

## **1\. Evolución de los Lenguajes de Marca**

* **GML (1960)** Fue el primer sistema en separar el contenido de su formato mediante etiquetas descriptivas generales.  
* **SGML (1980)** Es un metalenguaje internacional que define las reglas para crear otros lenguajes de marcas.  
* **HTML (1990)** Aplicación de SGML con etiquetas fijas creada para estructurar documentos en la World Wide Web.  
* **XML (1990)** Metalenguaje estricto diseñado para el almacenamiento y transporte de datos permitiendo definir etiquetas propias.  
* **XHTML (2000)** Adaptación de HTML bajo las reglas sintácticas estrictas y bien formadas de XML.  
* **HTML5 (2010)** Estándar actual que elimina la dependencia de SGML y añade etiquetas semánticas y multimedia nativas.

## **2\. Posicionamiento en CSS** 

* **static:** Es el valor por defecto. El elemento sigue el orden natural del HTML.  
* **relative:** Se mueve respecto a su posición original usando top/bottom/left/right sin afectar a los vecinos.  
* **absolute:** Se posiciona respecto a su ancestro más cercano que tenga una posición distinta a static. Sale del flujo normal.  
* **fixed:** Se queda pegado en una posición fija de la ventana del navegador, no se mueve al hacer scroll.  
* **sticky:** El elemento se desplaza normalmente hasta que llega a un punto del scroll (ej. top: 0\) y se queda fijado ahí.  
* **z-index:** Controla la profundidad. Un número mayor pone el elemento por encima de otros. Solo funciona en elementos posicionados (non-static).

## **3\. Especificidad y la regla \!important**

Cuando hay conflicto de estilos, el navegador suma puntos para ver qué regla gana:

* **Estilo en línea (dentro del HTML):** 1000 puntos.  
* **IDs (\#ejemplo):** 100 puntos.  
* **Clases, atributos y pseudo-clases (.clase, :hover):** 10 puntos.  
* **Elementos y pseudo-elementos (h1, ::before):** 1 punto.  
  **Ejemplo:** div\#menu (101 puntos) gana a div.navegacion (11 puntos).  
  **\!important:** Es una regla que rompe la puntuación. Si se añade al final de un valor, esa regla ganará siempre a cualquier otra, sin importar los puntos. color: red \!important;

## **4\. Reglas-Arroba (@-rules)**

* **@media:** Aplica estilos según el tamaño de la pantalla (Responsive Design).  
* **@keyframes:** Define los pasos de una animación.  
* **@font-face:** Permite usar fuentes descargadas de internet.  
* **@import:** Se usa para cargar un archivo CSS dentro de otro.

## **5\. Pseudo-clases (:) y Pseudo-elementos (::)**

**Pseudo-clases:** Seleccionan elementos según su estado o posición.

* :hover: Cuando pasas el ratón por encima.  
* :not(.clase): Selecciona todo lo que NO tenga esa clase.  
* :is(h1, h2): Agrupa varios selectores de forma simplificada.  
* :has(img): Selecciona un elemento si contiene una imagen dentro.  
* **Ejemplo:** a:hover { color: green; }

**Pseudo-elementos:** Seleccionan una parte específica del contenido.

* ::before: Inserta algo antes del contenido del elemento.  
* ::after: Inserta algo después del contenido del elemento.  
* ::first-letter: Da estilo solo a la primera letra de un texto.  
* **Ejemplo:** p::after { content: " \- Leer más"; color: blue; }