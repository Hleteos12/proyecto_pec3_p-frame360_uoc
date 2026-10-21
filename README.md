# Star Wars 360º con A-Frame

*Hace mucho tiempo, en una galaxia muy, muy lejana....*

Práctica de panorámicas 360º con A-Frame. Son dos escenas de realidad virtual metidas con iframes en `index.html`: una con imagen fija (`a-sky`) y otra con vídeo (`a-videosphere`). He seguido el [tutorial de panorámicas 360º](https://gitlab.com/webxr/tutorial_a-frame_360/wikis/home), pero le he puesto temática de Star Wars.

## Episodio I: Tatooine (tatooine.html)

El fondo es una foto 360º de un desierto a la que le añadí el segundo sol y dos lunas para que pareciera Tatooine. Por el cielo da vueltas un Ala-X hecho con primitivas (cajas, cono y cilindros) y con una textura de chapa.

## Episodio II: La Estrella de la Muerte (video.html)

El fondo es un vídeo 360º de un vuelo por dentro de un fractal (la esponja de Menger). Lo pasé a gris metálico y así parecen los pasillos de la Estrella de la Muerte. Delante de la cámara va un caza TIE, orientado hacia donde avanza el vídeo, así que da la sensación de ir volando detrás de él. Lleva la misma textura de chapa que el Ala-X y otra para las alas. También hay dos luces rojas que parpadean y un botón de PLAY/PAUSA, porque en algunos navegadores el vídeo no arranca solo.

## Pasos del tutorial

1. Meter la imagen o el vídeo en `<a-assets>`. El vídeo va con `autoplay` y `loop="true"`.
2. Usar `<a-sky>` con `radius` y `src` para la imagen, y `<a-videosphere>` para el vídeo.
3. Añadir objetos con textura, animaciones y la cámara con cursor.
4. Juntar las dos escenas en un HTML con iframes y publicarlo en GitHub Pages.

En vez de la versión 0.6.1 del tutorial uso A-Frame 1.8.0. Por eso las animaciones están hechas con el componente `animation`, ya que `<a-animation>` ya no existe. El vídeo está en mp4 y no en ogg, que es lo que recomienda el enunciado.

## Archivos

```
index.html          página principal
tatooine.html       escena con a-sky
video.html          escena con a-videosphere
assets/
  tatooine360.jpg   imagen 360 (4096x2048)
  deathstar360.mp4  vídeo 360 (1920x960, 35 s)
  alax.png          textura de chapa
  tie.png           textura de las alas del TIE
```

## Uso de IA

Para este proyecto he usado una herramienta de IA (Claude) como ayuda. Me ha ayudado con:

- Buscar la imagen y el vídeo 360º con licencia libre.
- Editar la imagen (los soles y las lunas) y el vídeo (recorte, color y conversión a mp4).
- Generar las texturas.
- Montar el código de las escenas.

Las ideas de la temática y de cómo tenía que quedar cada escena las he decidido yo, y los cambios los he ido revisando y probando.

## Créditos

Homenaje a Star Wars (marca de Lucasfilm Ltd.). No hay imágenes ni vídeos de las películas.

- Imagen: "[Goegap](https://polyhaven.com/a/goegap)" de Poly Haven (CC0), modificada.
- Vídeo: "[Flug durch die Menger-Schwamm-Welt in VR (360 Grad)](https://commons.wikimedia.org/wiki/File:Flug_durch_die_Menger-Schwamm-Welt_in_VR_(360_Grad)_und_8K_OHNE_TON_4320p50.webm)" de PantheraLeo1359531, Wikimedia Commons (CC BY 4.0), recortado, recoloreado y pasado a mp4.
- Texturas `alax.png` y `tie.png`: hechas para este proyecto.
