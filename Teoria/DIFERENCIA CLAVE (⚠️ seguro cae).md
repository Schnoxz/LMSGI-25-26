DIFERENCIA CLAVE (⚠️ seguro cae)
Pseudo-clase (:) → estado o posición del elemento
👉 cómo está
Pseudo-elemento (::) → parte concreta del elemento
👉 qué parte
🔹 2. PSEUDO-CLASES MÁS PREGUNTADAS
Interacción
:hover → ratón encima
:active → clicando
:focus → foco (clic/teclado)
:focus-visible → foco solo con teclado ♿
Enlaces
:link → no visitado
:visited → visitado
Formularios
:required / :optional
:valid / :invalid
:checked → checkbox/radio
:disabled / :enabled
:placeholder-shown
Estructura (DOM) ⚠️
:first-child / :last-child
:only-child
:nth-child(n)
:first-of-type
:nth-of-type(n)
🔹 3. PSEUDO-CLASES LÓGICAS (muy de teoría)
:not() → excluye
:is() → agrupa selectores
:where() → como :is pero especificidad 0
:has() → selecciona si contiene algo (muy importante)
🔹 4. OTRAS IMPORTANTES
:root → <html> (variables CSS)
:empty → sin texto ni hijos
:target → id = hash URL
🔹 5. PSEUDO-ELEMENTOS CLAVE
Contenido generado
::before
::after
⚠️ Necesitan content
Texto
::first-letter
::first-line
::selection
Formularios / listas
::placeholder
::marker
::file-selector-button
🔹 6. SINTAXIS (pregunta típica)
Pseudo-clase → selector:pseudo
Pseudo-elemento → selector::pseudo
🔹 7. TRUCO DE EXAMEN
Estado = :
Parte del elemento = ::