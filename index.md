## Contexto

Trabajo en un equipo que se encarga de que la parte del checkout de una tienda online funcione siempre.
Un día tuvimos una gran campaña de descuentos, con mucha más gente comprando de lo normal y surgio un problema.

## El problema

A las pocas horas de empezar la campaña, algunos usuarios no podían terminar de pagar: la página se quedaba trabada o mostraba un error.
Al revisar, vimos que el sistema que procesa los pagos se iba quedando sin memoria como cuando a una computadora "le falta espacio" y empieza a ir lenta y se reiniciaba solo cada tanto. Esto pasaba justo en el momento de más ventas del mes, así que perdimos compras y usuarios enojados.

## Qué hicimos

Apenas se calmó la situación, nos juntamos como equipo a analizar qué pasó. solo buscando entender que paso y mejorar. Seguimos estos pasos:

1. Reconstruimos paso a paso qué había pasado y en qué momento.
2. Buscamos la causa: encontramos que una parte del código guardaba información en la memoria de la computadora cada vez que alguien pagaba, pero nunca la borraba. Con el tiempo, esa memoria se llenaba hasta que el sistema colapsaba.
3. Corregimos ese error para que la información se borre correctamente después de cada pago.
4. Agregamos avisos automáticos que nos alertan antes si la memoria empieza a llenarse, para poder actuar antes de que afecte a los usuarios.

## Qué aprendimos

- Este tipo de errores que la memoria se llene de a poco, es difícil de ver a simple vista, así que ahora lo revisamos con más cuidado antes de lanzar cambios nuevos.
- Es mejor tener avisos tempranos que esperar a que algo falle.
- Analizar los errores en equipo, sin culpar a nadie, ayuda a encontrar mejores soluciones y a que todos se animen a hablar con honestidad sobre lo que salió mal.

## Evidencia de los cambios realizados

- Cambios en el código: https://github.com/alejandrocasciano/blog-tecnico-postmortem-/commits/main/
- Revisión de esos cambios: *(acá va el enlace al Pull Request)*

## Reflexión sobre la honestidad al dar feedback

Durante la reunión de análisis, dije de forma directa pero respetuosa que el error había pasado una revisión anterior sin que nadie lo notara, incluyéndome a mí.
No lo escondí ni le busqué la vuelta: lo dije como un hecho, para que sirviera de aprendizaje y no como una crítica a una persona en particular. Eso ayudó a que el resto del equipo también se animara a contar sus propios errores,y entre todos armamos una forma de revisar el código más cuidadosa.
