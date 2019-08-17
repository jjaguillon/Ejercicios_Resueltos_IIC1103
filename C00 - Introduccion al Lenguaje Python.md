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