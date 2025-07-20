## Taller Guiado: Trabajando con Cadenas de Caracteres en Python

Este taller está diseñado para practicar el uso de cadenas de caracteres en Python. Cada ejercicio tiene instrucciones claras y una explicación de cómo resolverlo.

------


### **Ejercicio 1: Contando caracteres**

#### **Instrucción:**

Escribe un programa que solicite al usuario una frase y muestre:

1. La cantidad total de caracteres en la frase.
2. La cantidad de espacios en la frase.

#### **Guía:**

1. La función `len()` permite conocer cuántos caracteres hay en total (incluyendo letras, espacios y símbolos).
2. El método `.count(" ")` cuenta cuántos espacios en blanco hay dentro del texto ingresado.

#### **Código:*

```python
frase = input("Escribe una frase: ")
total_caracteres = len(frase)
espacios = frase.count(" ")

print(f"La frase tiene {total_caracteres} caracteres en total.")
print(f"La frase tiene {espacios} espacios.")
```

------

### **Ejercicio 2: Validando nombres**

#### **Instrucción:**

Crea un programa que solicite al usuario su nombre completo y verifique:

1. Que solo contenga letras.
2. Que comience con mayúscula.

#### **Guía:**

1. Para verificar que el nombre tiene solo letras (sin símbolos o números), puedes eliminar los espacios y luego aplicar `isalpha()`.
2. Para asegurarte de que cada palabra empieza en mayúscula, usa `istitle()`, que valida ese formato de nombres propios.

#### **Código:**

```python
nombre = input("Escribe tu nombre completo: ")

if nombre.replace(" ", "").isalpha():
    if nombre.istitle():
        print("El nombre es válido.")
    else:
        print("El nombre debe comenzar con mayúscula.")
else:
    print("El nombre solo debe contener letras.")
```

------

### **Ejercicio 3: Invirtiendo palabras**

#### **Instrucción:**

Escribe un programa que pida al usuario una palabra y muestre la palabra invertida.

#### **Guía:**

1. Para invertir el orden de los caracteres de una cadena, puedes usar `[::-1]`, una forma rápida de recorrer la cadena desde el final hasta el inicio.

#### **Código:**

```python
palabra = input("Escribe una palabra: ")
invertida = palabra[::-1]
print(f"La palabra invertida es: {invertida}")
```

------

### **Ejercicio 4: Cifrando texto**

#### **Instrucción:**

Crea un programa que solicite al usuario una frase y reemplace todas las vocales por un carácter especial (*).

#### **Guía:**

1. Aplica el método `.replace()` para cambiar cada vocal por un asterisco.
2. Repite el proceso tanto para minúsculas como para mayúsculas, para cubrir todos los casos.

#### **Código:**

```python
frase = input("Escribe una frase: ")

frase_cifrada = frase.replace("a", "*").replace("e", "*").replace("i", "*").replace("o", "*").replace("u", "*")
frase_cifrada = frase_cifrada.replace("A", "*").replace("E", "*").replace("I", "*").replace("O", "*").replace("U", "*")

print(f"La frase cifrada es: {frase_cifrada}")
```

------

### **Ejercicio 5: Contador de vocales**

#### **Instrucción:**

Escribe un programa que cuente cuántas vocales hay en una frase ingresada por el usuario.

#### **Guía:**

1. Usa el método `.count()` para contar cada vocal por separado.
2. Suma los resultados de todas las vocales para obtener el total general.

#### **Código:**

```python
frase = input("Escribe una frase: ")

a = frase.count("a") + frase.count("A")
e = frase.count("e") + frase.count("E")
i = frase.count("i") + frase.count("I")
o = frase.count("o") + frase.count("O")
u = frase.count("u") + frase.count("U")

total_vocales = a + e + i + o + u

print(f"La frase tiene {total_vocales} vocales.")
```

------

### **Ejercicio 6: Formateando cadenas**

#### **Instrucción:**

Escribe un programa que tome un número de teléfono ingresado por el usuario (10 dígitos) y lo formatee como `(XXX) XXX-XXXX`.

#### **Guía:**

1. Usa `slicing` para separar el número en tres partes: los primeros tres dígitos, los siguientes tres y los últimos cuatro.
2. Luego organiza esas partes usando `f-strings` para dar el formato deseado.

#### **Código:**

```python
telefono = input("Escribe un número de teléfono de 10 dígitos: ")
if len(telefono) == 10 and telefono.isdigit():
    telefono_formateado = f"({telefono[:3]}) {telefono[3:6]}-{telefono[6:]}"
    print(f"El número formateado es: {telefono_formateado}")
else:
    print("El número debe tener exactamente 10 dígitos.")
```

------

### **Ejercicio 7: Detectando palíndromos**

#### **Instrucción:**

Escribe un programa que determine si una palabra ingresada por el usuario es un palíndromo (se lee igual al derecho y al revés).

#### **Guía:**

1. Convierte la palabra a minúsculas para que la comparación no se vea afectada por las mayúsculas.
2. Inviértela con `[::-1]` y compárala con la original para saber si es un palíndromo.

#### **Código:**
