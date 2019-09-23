# Control de Flujo: Ciclos

Ya vimos que los lenguajes de programación poseen **condiciones de ejecución**, los cuales permiten controlar como se ejecutará el programa bajo ciertas condiciones. Sin embargo, existen otro tipo de condiciones que permiten que el programa repita su ejecución, estas son conocidas como **condiciones de reiteración**.



### Flujo de programa

En Python existe la sintaxis del **while** para condiciones de ciclo booleanas, y el **for** para las condiciones numéricas.

#### while

El comportamiento de este bloque funciona igual que la condición del lenguaje humano:

*Mientras no sean las 17:00 hrs. Seguiré trabajando*. Su equivalente en Python sería:

```python
HORA = 8

while HORA < 17:
    print("Son las: " + str(HORA) + ":00")
    print("Trabajo muy duro. Como un esclavo")
    HORA = HORA + 1
    
print("Yahu! Se acabó el trabajo")
```

Algo que hay que observar es la importancia del `HORA = HORA + 1`. Pues permite que la condición de reiteración tenga término.

Si la condición no tiene término, entra en el error conocido como **CICLO INFINITO**. 

```python
while True:
    print("El fin nunca es el fin.")
    
print("Jaja. Nunca me ejecutaré.")
```

**Quiero más información**. Puede dirigirse al anexo A03 - Cuantificación Universal y Existencial.



#### for

Este bloque es útil sólo cuando conoces la cantidad de repeticiones que deben ocurrir, para eso deberás utilizar la función `range()`.

`range()` puede recibir hasta 3 parámetros, conocidos como  `start`, `stop` y `step`, que te permitirán generar diferentes números en cada repetición, aquí tres ejemplos de uso.

*Imprima todos los números del 0 al 15*. Se usa solo el `stop`.

```python
for i in range(16): #Fijarse que el número stop es 1 más
    print(i)
```

*Imprima todos los números del 5 al 10*. Se usa el `start` y el `stop`

```python
for i in range(5, 11):
    print(i)
```

*Imprima de manera inversa los números del 10 al 1*. Se requieren todos los parámetros.

```python
for i in range(10, 0, -1): #Fijarse que el número stop es step veces mas
    print(i)
```

Esto permite que los pasos a ocurrir sean un número fijo, y que el número asociado al paso (en este caso `i`), pueda ser utilizado.

**Para más información**: Puede dirigirse al anexo A04 - Tipos de For.