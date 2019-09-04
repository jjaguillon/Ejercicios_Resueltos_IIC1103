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

El bloque **elif** es otra condición que se quiere observar, **solo si la primera no se cumple**.

*Si mide más de 1.30m. Debe pasar a la montaña rusa con un adulto*. Su equivalente en Python:

```python
ESTATURA = 1.4

if ESTATURA > 1.5:
	print("Puede pasar a la montaña rusa")
elif ESTATURA > 1.3:
    print("Puede pasar acompañado de un adulto")
```

Puedes llamar más bloques **elif** de ser necesarios, estas condiciones se revisan cuando **las anteriores no se cumplen**.

*Si mide más de 1.30m. Debe pasar a la montaña rusa con un adulto.*

```python
ESTATURA = 1.4
ADULTO = False

if ESTATURA > 1.5:
	print("Puede pasar a la montaña rusa")
elif ESTATURA > 1.3 and ADULTO:
    print("Puede pasar a la montaña rusa, sientese al lado del adulto")
elif ESTATURA > 1.3:
    #and not ADULTO(?)   No será necesario, pues ya se revisó en el bloque anterior
    print("No puede pasar solo, debe ser acompañado de un adulto")
```

Finalmente, el bloque **else** es aquel que se ejecuta si **ninguna de las condiciones anteriores** se cumple. 

```python
ESTATURA = 1.4
ADULTO = False

if ESTATURA > 1.5:
	print("Puede pasar a la montaña rusa")
elif ESTATURA > 1.3 and ADULTO:
    print("Puede pasar a la montaña rusa, sientese al lado del adulto")
elif ESTATURA > 1.3:
    #and not ADULTO(?)   No será necesario, pues ya se revisó en el bloque anterior
    print("No puede pasar solo, debe ser acompañado de un adulto")
else:
    print("No puede pasar a la montaña rusa")
```



### Diferencia entre bloques if-elif-else vs. if-if-if

Un clásico error es usar bloques con sólo **ifs**, pensando que funcionará de igual manera que el bloque **if-elif-else**.

Si la lógica es correcta al escribir las condiciones, puede que la ejecución y el resultado sea el mismo.

Entonces. **¿En qué se diferencia? ¿Por qué debería usar uno en vez de otro?** 

El bloque **if-if** revisa las condiciones de todos los bloques, independiente si la anterior se cumple o no. 

Ambos bloques son útiles dependiendo del contexto. Por ejemplo:

*En una empresa repartidora necesitan enviar la mayor cantidad de encomiendas. Para eso te piden que clasifiques los envíos en según tipo. De ser **cajas** deben ser enviadas en camiones y vagonetas dependiendo de su masa. De masar menos de 15kg. debe ser enviado en vagonetas, si masa más de 13kg. se debe enviar mediante camiones. Cualquier otro caso, debe ser enviado en bicicletas* 

```python
ENCOMIENDA = "CAJAS"
MASA_kg = 13

# Condiciones donde los bloques if-elif-else corresponde
if ENCOMIENDA == "CAJAS":
    # Condiciones donde los bloques if-if corresponde
    if MASA_kg < 15:
        print("Se envia por vagoneta")
    if MASA_kg > 12:
        print("Se envia por camion")
else:
    print("Se envia por bicicleta")
```

Por ejemplo, en este caso, se imprimirá que puede enviarse tanto por vagoneta, como por camión.

**Todavía no entiendo cual usar cuando.** Puede dirigirse al anexo A02 - Teoría de conjuntos