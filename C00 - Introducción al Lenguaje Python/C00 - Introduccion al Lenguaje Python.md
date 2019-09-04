# Introducción al Lenguaje Python

Python es un lenguaje cuya sintaxis busca ser lo más legible posible, es decir, que su escritura y lectura se parezca mucho al lenguaje hablado (el inglés en este caso).



## Tipo de datos básicos

Para poder este viaje por el mundo de la programación, debemos entender los tipos de datos básicos que podemos utilizar dentro de Python.

- **int**: números enteros: 1, 10, -32
- **float**: números flotantes, o decimales: 1.2, 0.9, 21.323
- **string**: conjunto de caracteres: "Hola Mundo"
- **bool**: valor lógico, representa si algo es verdadero o falso: True

```python
entero = 123
flotante = 12.32
string = "Hola Mundo"
logico = True
```



## Interacción con un usuario

Por este momento, entiéndase como **usuario** a un humano que ejecute un programa que usted haya escrito (puede ser usted este usuario).

Para que el programa tenga interacción con el usuario, debemos entender el funcionamiento de dos tipos de funciones básicas.

- **input(** *string* **)**: función que permite recibir un **string** por parte del usuario. Puedes colocar un *string* de referencia, para que el usuario sepa que debe ingresar.

```python
entrada = input("Ingresa tu nombre: ")
```

- **print(** *string* **)**: función que permite entregar en pantalla un *string*.

```python
print("Hola Universo") #Me canse de dirigirme solo al mundo.
```

Gracias a **input()** y a **print( )** podemos entregar y recibir información de lo que ocurre dentro del programa.



## Operatoria básica: Aritmética

#### Datos numéricos

Cuando tenemos variables del tipo **int** o **float**, podemos realizar las siguientes operaciones básicas para obtener nuevos valores.

```python
X = 10
Y = 12

FUNCION = (X**2) - 2*Y + 1
```

La variable **FUNCION** contiene el valor obtenido <img align="center" src="https://tex.s2cms.ru/svg/f(x%2C%20y)%3Dx%5E2%20-%202y%20%2B%201" alt="f(x, y)=x^2 - 2y + 1" /> 

Hay ciertas operaciones a las cuales hay que tomar ciertas consideraciones:

- división **/** : tal cual la conocemos, con todo y decimales
- división entera: **//** : este tipo de división donde solo se mantiene el valor entero y obvia los decimales.
- resto **%** : el resto obtiene la cantidad que sobra de la división, cuyo valor no es 0 cuando la división no es exacta.

```python
DIVISION = 13/5 			#2.6
D_ENTERA = 13//5 			#2
RESTO = 13%5 				#3
```

**Sigues con dudas de esto?**: Dirígete al anexo A00 - Aritmética

## Operatoria básica: Comparadores

Cuando trabajamos con variables de tipo **int** o **float**, podemos utilizar comparadores numéricos para obtener valores **bool** que indiquen el cumplimiento de la comparación.

```python
X = 10
Y = 20

print(X == Y)
```

Entiéndase el siguiente lenguaje utilizado: un valor **se cumple** cuando su variable es **True**. Por el contrario,  un valor **no se cumple** cuando su variable es **False**

Los comparadores numéricos son:

- Igualdad **==** : **se cumple** si ambos valores son **iguales**.
- Diferencia **!=** : **se cumple** si los valores son **diferentes**.
- Mayor (o igual) a **>**(**=**) : **se cumple** si el primer valor **es mayor** (**o igual**) que el segundo.
- Menor (o igual) a **<**(**==**) : **se cumple** si el primer valor **es menor** (**o igual**) que el segundo.

```python
X = 10
Y = 20

EQ  = X == Y #False (10 == 20)
NEQ = X != Y #True  (10 != 20)
GRT = X > Y  #False (10 > 20)
LEQ = X <= Y #True  (10 <= 20)
```



## Operatoria básica: Lógica

Cuando trabajamos con variables de tipo **bool**, podemos realizar operaciones lógicas, muy ligadas al lenguaje humano lógico.

Entiéndase el siguiente lenguaje utilizado: un valor **se cumple** cuando su variable es **True**. Por el contrario,  un valor **no se cumple** cuando su variable es **False**

- **not** : niega el valor booleano, cambiando su valor.

- **and** : esta operación nos permite condicionar que **dos valores** booleanos **se cumplan siempre**.
- **or** : esta operación **se cumple** cuando **al menos, uno de los valores** booleanos **se cumpla**.

```python
COND_1 = True
COND_2 = False

NOT_F = not(COND_2)			#True
AND_1 = COND_1 and COND_2	#False
AND_2 = COND_1 and NOT_F	#True
OR_1  = COND_1 or COND_2	#True
```

**Sigues con dudas de esto?**: Dirígete al capítulo A01 - Compuertas Lógicas



## Operatoria básica: strings

Al trabajar con variables **string**, una de sus operaciones básicas es **concatenar**.

#### ¿Qué es concatenar?

Es simplemente, unir dos strings mediante el comando **+**.

```python
STR_1 = "Hola"
STR_2 = "Universo"

FRASE = STR_1 + " " + STR_2  #Hola Universo
```

#### Cuidado con los tipos

Un error común es concatenar dos variables de diferente tipo. Por ejemplo:

```python
EDAD = 12

FRASE = "Hola. Soy Rocio y tengo " + EDAD    #TypeError
```

Esto se soluciona mediante la conversión de tipos

```python
EDAD = 12

FRASE = "Hola. Soy Rocio y tengo " + str(EDAD)  #Hola. Soy Rocio y tengo 12
```

**¿Más cosas con strings?**: Dirígete al capítulo C02 - Strings