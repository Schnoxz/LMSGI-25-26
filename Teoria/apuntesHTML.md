html 05/05 apuntes
funciones css MIN (x, y) CLAMP (x, y, z)
Tecnicas responsive:

Relative padding (En funcion del relleno de texto por ejemplo)

.container{
	padding: 5em;
}

MEJOR USAR:
.container{
	padding: min(5em, 8%); // Calculará un padding relativo al dispositivo
}

Responsive fount size (usar mejor rem y no px)

h1{
	font-size: clamp(1.8ram, 10vw, 5rem); // Valor minimo, valor preferido, valor maximo
}

Con el vw no podriamos hacer zoom en el encabezado de la web, para solucionarlo cambiamos el 10vw por un calc(7vw + 1ram)


Responsive images

img{
	max-width: 100%;
	height: auto;
	aspect-ratio: 16/9; // Resolucion 
	object-fit: contain; // Si usamos una determinada resolucion y el dispositivo es distinto, con object-fit se mantiene el contenedor de una imagen con huecos blancos, con object-fit: cover; intenta cubrir todos los huecos, haciendo zoom.
}


HTML 07/05 apuntes

linear-gradient si le añades un 1 al final en un border image en vez de difuminar un pixel, difuminas todo el bloque

Dentro de position "absolute" puedes implementar inset "top, right, bottom, left" en ese orden

Overflow: sirve para que no se superposicione bloques entre si, si ponemos "overflow: scroll" aparecerá una barra de desplazamiento en cada bloque, con un overflow-y, en eje vertical. Si ponemos hidden no aparecerán

 