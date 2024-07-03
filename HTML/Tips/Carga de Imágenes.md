## Carga de imágenes por formato

Esta característica nos permite cargar la imagen del primer formato de imagen soportado por el navegador. Una buena práctica es intentar cargar primero aquellos formatos que son más ligeros u óptimos para la web como el formato WEBP o AVIF.

Fuente [Midudev](https://x.com/midudev/status/1757072464088109063)

```
<picture>
	<!-- Avif format -->
	<source srcset="image.avif" type="image/avif">
	<!-- WebP format for modern browsers -->
	<source srcset="image.webp" type="image/webp">
	<!-- JPEG format as a fallback -->
	<img src="image.jpg" alt="Your image description">
</picture>
```

Donde:

- El atributo *srcset* indica el *path* del archivo.
- El atributo *type* indica el formato de imagen.
- El elemento *img* se utiliza como recurso por defecto si los anteriores formatos no son soportados.
## Carga de imágenes por tamaño

Esta característica nos permite cargar la imagen que cumpla con las restricciones de tamaño, lo que nos permite cargar imágenes más pequeñas en dispositivos con pantallas pequeñas.

Fuente [MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

```
<img
    srcset="elva-fairy-480w.jpg 480w, elva-fairy-800w.jpg 800w"
    sizes="(max-width: 600px) 480px,800px"
    src="elva-fairy-800w.jpg"
    alt="Elva dressed as a fairy" />
```

Donde:

- El atributo *srcset* contiene la lista de *paths* a los diferentes archivos de imagen, adicionalmente se especifica el ancho intrínseco de la imagen.
- El atributo *sizes* contiene la lista con las restricciones a aplicar para elegir las imágenes, se indica la *media query* que debe cumplir la imagen seguido del ancho en pixeles que debe tener.

**Nota: El elemento *source* soporta de igual forma los atributos *srcset* y *sizes*.**
## Recursos

Estos recursos nos permiten cambiar el formato y tamaño de una imagen de forma gratuita y sencilla:

- [Squoosh](https://squoosh.app/)
- [Imgto.xyz](https://imgto.xyz/)