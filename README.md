# Carrusel 3D

Un carrusel circular en 3D construido con **HTML y CSS puro**, sin librerías ni JavaScript.
Las imágenes se disponen formando un anillo que rota de forma automática y continua,
creando una sensación de profundidad real mediante transformaciones 3D.

🔗 **Demo en vivo:** [https://rodrieme.github.io/carrusel3D/]

<img width="1198" height="658" alt="carrugif" src="https://github.com/user-attachments/assets/50979112-2d28-44bd-94fa-d0f6d898874e" />


---

## ¿Cómo funciona?

El efecto se consigue sin imágenes 3D ni librerías, solo con CSS:

- El contenedor usa `transform-style: preserve-3d`, que mantiene a sus hijos en un
  espacio tridimensional real.
- Cada tarjeta se coloca en el anillo combinando una rotación (`rotateY`) con un
  desplazamiento en profundidad (`translateZ`). El ángulo de cada una se calcula de forma
  automática a partir de su posición y del número total de tarjetas, usando una propiedad
  personalizada (`--quantity`) y `calc()`. Así, cambiar el número de imágenes recoloca todo
  el anillo solo.
- Una animación con `@keyframes` rota el anillo completo 360° de forma continua y a
  velocidad constante (`linear`).

## Tecnologías

- HTML5
- CSS3 (transformaciones 3D, `@keyframes`, propiedades personalizadas con `calc()`)

## Uso

Al no tener dependencias, basta con abrir el archivo en el navegador:

1. Clona el repositorio.
2. Abre `index.html` directamente en cualquier navegador moderno.

Para cambiar las imágenes, sustituye los archivos de la carpeta `IMAGENES/` y ajusta el
valor de `--quantity` en el HTML si modificas la cantidad.

---

Pequeño proyecto creado para practicar transformaciones 3D en CSS.
