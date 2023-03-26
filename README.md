# Reto_7

## Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
```
if __ name__ == "__ main__":
    x = float(1) #inicializa a n en 1
    while x <= 100:
        
        """Mientras el valor de x sea menor o igual a 100, se
        va a repertir el print y se le sumara 1 a x cada vez
        que se repita el ciclo"""
        
        print("El cuadrado del número ",x," es", x**2) #se eleva el numero dentro del print
        x +=1 #se le suma 1 a n cada ciclo
```

## Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.

### para numeros impares

```print("para numeros impares:")
for x in range(1, 1000, 2):
    print(x) 
```  


### para numeros pares
```

print("para numeros pares:")
for x in range(2, 1001, 2):
    print(x)
    
```

## Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado

```

n = int(input("Ingrese un número natural n mayor o igual a 2: "))

if n >= 2:
    print("Los números pares menores o iguales a", n, "en orden descendente son:")
    for i in range(n, 1, -1):
        if i % 2 == 0:
            print(i)
else:
    print("El número ingresado no es válido. Por favor, ingrese un número natural mayor o igual a 2.")
```

## En 2022 el país A tendrá una población de 25 millones de habitantes y el país B de 18:9 millones. Las tasas de crecimiento anual de la población serán de 2% y 3% respectivamente. Desarrollar un algoritmo para informar en que año la población del país B superará a la de A.

```

if __name__ == "__main__" :
    A = 25000000 #inicializa A en 25000000
    B = 18900000 #inicializa B en 18900000
    año = 2022 #inicializa año en 2022
    while A>=B : #mientras PA sea mayor o igual que PB
        print("Poblacion del pais A ",A," mientas que el pais B tiene ",B," en el año ",año)
        A *= 1.02  #se le aumenta el 2 % cada ciclo
        B *= 1.03 #se le aumenta el 3 % cada cilco
        año += 1 #suma 1 al valor de año
    print("Poblacion del pais A ",A," mientas que el pais B tiene ",B," en el año ",año) 
    """ se ejecuta al terminar el ciclo 
    con los valores finales de PA,PB y año"""
```
## Imprimir el factorial de un número natural n dado.

```

def calcular_factorial(n):
    """Función que calcula el factorial de un número natural n"""
    if n == 0:
        return 1
    else:
        return n * calcular_factorial(n - 1)

#Programa principal
n = int(input("Introduce un número natural para calcular su factorial: "))
if n < 0:
    print("El factorial no está definido para números negativos.")
else:
    factorial = calcular_factorial(n)
    print(f"El factorial de {n} es {factorial}.")
    
```

## Implementar un algoritmo que permita adivinar un número dado de 1 a 100, preguntando en cada caso si el número es mayor, menor o igual.

```

def adivinar_numero():
    """Función que adivina un número de 1 a 100"""
    minimo = 1
    maximo = 100
    respuesta = None
    
    while respuesta != "=":
        if minimo > maximo:
            print("¡Ha ocurrido un error! El número que has pensado no se encuentra en el rango de 1 a 100.")
            return
        numero = (minimo + maximo) // 2
        respuesta = input(f"¿Es {numero} mayor (>), menor (<) o igual (=) al número que has pensado? ")
        if respuesta == ">":
            minimo = numero + 1
        elif respuesta == "<":
            maximo = numero - 1
    
    print(f"¡He adivinado el número! El número es {numero}.")

#Programa principal
print("Piensa en un número del 1 al 100, yo trataré de adivinarlo.")
adivinar_numero()

```

## Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.
```

if __name__ == "__main__" :
    n = int(input("ingrese un valor del 2 al 50 ")) #se ingresa el valor de n
    i = 1 #se establece un contador
    while i <= n : #mientras i sea menor o igual n
        if n%i == 0 : #si n es divisible por i por residuo igual a 0
            print(i) #se imprime i
        i +=1 #se le suma 1 en cada ciclo
        
```

## Implementar el algoritmo que muestre los números primos del 1 al 100. nota: use funciones

```

def es_primo(n):
    """Función que verifica si un número es primo"""
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

#Main program
print("Los números primos del 1 al 100 son:")
for i in range(1, 101):
    if es_primo(i):
        print(i)

```
  
