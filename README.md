# Modelo e idea principal
# DEPV: Decaimiento Exponencial para Predicción de Vistas

$V(t) = V_{f}\cdot(1-e^{-t/\tau})$

Utilizando los datos históricos de los videos subidos se puede encontrar el valor de $\tau$ y el de $V_{f}$.

* $\tau$: Constante de tiempo del sistema. Cuando $t = 5\tau$, se considera que la cantidad de visitas no variará más ya que

  $V(5\tau) = V_{f}\cdot(1-e^{-5\tau/\tau}) = V_{f}\cdot(1-e^{-5}) \approx V_{f}$

  Cuando $t = \tau$, la cantidad de visitas representa el 63.21% de la cantidad de visitas final.
* $V_{f}$: Cantidad de vistas final.

Hay dos acercamientos posibles:

* Un solo modelo que tome en cuenta el promedio de todos los datos pasados.
* Un modelo por video y promediar sus salidas.

En este contexto, entrenar el modelo es encontrar (calcular) los parámetros $V_{f}$ y $\tau$.

Cosas importantes sobre $\tau$:

* La constante de tiempo depende de la dinámica del sistema, es decir, la rapidez de la difusión del video. Esto tiene que ver con la cantidad y rapidez con la que se comparte el video o le llega al feed de los demás usuarios.

Cosas importantes sobre $V_{f}$:

* Depende básicamente del alcance que tenga tu cuenta.
