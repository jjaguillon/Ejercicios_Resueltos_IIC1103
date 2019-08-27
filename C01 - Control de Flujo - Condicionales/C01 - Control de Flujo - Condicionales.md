# Control de Flujo: Condicionales

Una herramienta de los lenguajes de programación es su capacidad de dar **condiciones de ejecución**. Esto significa, que si se cumple ciertas condiciones, el programa realiza el resto de las operaciones.

Esto es mejor visto en un diagrama de flujo:

<img style="-webkit-user-select: none;margin: auto;" src="https://www.laserfiche.com/wp-content/uploads/2014/03/engineering-flow-chart.png" width = "600">

Esto en programación, se conoce como **flujo de programa**.



### Flujo de programa

Es una forma de observar el comportamiento de un programa y como este funciona bajo ciertas condiciones.

Ahí entra en juego la sintaxis del **if**, **elif** y **else** en Python.

El comportamiento de estos bloques funcionan igual que los condicionales del lenguaje humano:

*Si mide más 1.50m. Puede pasar a la montaña rusa*. Su equivalente en Python sería:

```python
ESTATURA = 1.8

if ESTATURA > 1.5:
    print("Puede pasar a la montaña rusa")
```

El bloque **elif** es otra condición que puede observar 

