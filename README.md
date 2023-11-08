# Filtro de Minecraft - Imitación

En esta práctica, se implementó un filtro inspirado en el siguiente filtro de Instagram: [Video de ejemplo](https://www.youtube.com/watch?v=6g3vc9BM_MM). El objetivo es crear un filtro que siga los movimientos faciales, especialmente los de las cejas y la boca, y aplique efectos de sonido según estos movimientos.

## Descripción

El filtro se desarrolló utilizando un detector de caras DNN en el modo de 68 puntos. Este modo permite rastrear los movimientos faciales y calcular la diferencia en la altura de los puntos pertenecientes a las cejas y la boca. Esta diferencia se utiliza para activar los efectos de sonido.

## Funcionamiento

El filtro funciona de la siguiente manera:

1. El detector de caras DNN se utiliza para detectar la cara en el fotograma de la cámara.
2. Se rastrean 68 puntos clave en la cara, que incluyen puntos en las cejas y la boca.
3. Se calcula la diferencia en altura entre estos puntos en fotogramas sucesivos.
4. Si la diferencia en altura de las cejas supera un umbral predefinido, se reproduce un efecto de sonido, como el sonido de afirmación "yes".
5. Si la diferencia en altura de la boca supera otro umbral, se reproduce un efecto de sonido de "idle" o inactividad.

## Requisitos

- Python 3.x
- OpenCV (para el procesamiento de imágenes)
- Bibliotecas de terceros para el procesamiento de audio (por ejemplo, SoundFile y SoundDevice)

## Uso

1. Ejecuta el programa que implementa este filtro.
2. Apunta la cámara web hacia tu rostro.
3. Selecciona con las letras D y E para seleccionar el modo DNN con 68 puntos.
4. Pulsa M para activar la máscara.
5. Mueve las cejas hacia arriba para activar un sonido aleatorio de la categoría "yes".
6. Abre la boca para activar un sonido de la categoría "idle".


