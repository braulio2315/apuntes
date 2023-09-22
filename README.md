# apuntes
# Listas (se conocen como conecciones)
# datos mutables y inmutables
```
def suma(a,b):
    return a+b

def resta(a,b):
    return a-b

def multiplicacion(a,b):
    return a*b

def division(a,b):
    return a/b

operaciones=[suma,resta,multiplicacion,division]
print(operaciones[0](1,2))  
print(operaciones[1](1,2))
print(operaciones[2](1,2))
print(operaciones[3](1,2))
for operacion in operaciones:
    print(operacion(1,2)) 
lista=[1,2,3,4,5,True,1.2,'hola',[1,2,3]]
```
# la lista es indexable (todos los elementos tienen un indice)
# la lista es mutable porque se puden modificar los valores
```
 lista[8]
```
```
lista[8]='braulio'
print(lista)
```
```
#slices
print(lista)
print(lista[:]) # es lo mismo. los dos puntos indican el inicio y el final
```
```
def funciones(a,b):
    return [a+b,a-b,a*b,a/b]
respuesta=funciones(3,4)
print(respuesta)
w,x,y,z = funciones(3,4)
print(w)
```
# tuple (se puede meter cualquieer tipo de dato), es inmutable(no se puede cambiar), pero si le pudes agregar valores
```
tupla_funciones=(suma,resta,multiplicacion,division)
print(tupla_funciones[1](5,4))
tupla=(1,2,3,4,5,True,1.2,'hola',[1,2,3])
```
```
def suma(a: int, b:int) -> int:
    return a+b

def operacion(a:int, b:int) -> (int,int):
    return(a+b,a-b)

(a,b)=operacion(5,6)
a,b=operacion(5,6)
print(a,b)
```
```
numeros_pares=range(2,11,2)
for par in numeros_pares:
    print(par,end=" ")
```
```
lista = [3,6,7,40,34,67,89]
max(lista)
min(lista)
sum(lista)
sorted(lista)
lista.sort(reverse=True)
lista
# metodo, hace las cosas pero no las regresa(no las imprime)
```
# set conjuntos (lleva parentesis y se puede poner cualquier tipo de datos pero al momento de imprimir no acepta valores repetidos)

```
mi_set={1,2,3,3,3,2,2,1,1,1}
mi_set

data=[1,2,1,3,4,5,2,1,3,4,6,9,7,8]
list(set(data)) #  el set ordena los valores
```
```
# diccionarios
mi_dict = {'llave': 'valor'}
mi_dict['llave'] ```
```
```
dia_semana = {
    'lunes':      1,
    'martes':     2,
    'miercoles':  3,
    'jueves':     4,
    'viernes':    5,
    'sabado':     6,
    'domingo':    7,
}

for e in mi_set:
    print(e)

for key in dia_semana.keys():
    print(key,end=" ")

for key,value in dia_semana.items():
    print(key,value)

for value
```
# funcion pura = tiene argumentos, no producen efectos secundarios, retorna siempre el mismo valor con la misma entrada
# ejemplo funcion pura = Math.sqrt(49)-> 7

## funcion impura = no tiene argumentos, puede retornar valores distintos, 
# ejemplo funcion impura= Math.random() -> 0.05
#                         Math.random() -> 3 
""" 
```
while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")

    opcion = input("Selecciona una opción: ")

    if opcion >= '5':
        print("¡Hasta luego!")
        break

    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))

    if opcion == '1':
        print("Resultado:", num1 + num2)
    elif opcion == '2':
        print("Resultado:", num1 - num2)
    elif opcion == '3':
        print("Resultado:", num1 * num2)
    elif opcion == '4':        
        if num2 != 0:
            print("Resultado: ", num1 / num2)
        else:
            print("No se puede dividir entre cero")
    else:
        print("¡Gracias por usar Mi Calculadora!") """
 
""" class MiCalculadora:
    def _init_(self):
        pass

    def suma(self, a, b):
        return a + b

    def resta(self, a, b):
        return a - b

    def multiplicacion(self, a, b):
        return a * b

    def division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "No se puede dividir entre cero"

calculadora = MiCalculadora()

while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")

    opcion = input("Selecciona una opción: ")

    if opcion == '5':
        print("¡Gracias por usar Mi Calculadora!")
        break
    elif opcion < '1' or opcion > '5':
        print("Opción no válida")
    else:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))

    if opcion == '1':
        print("Resultado:", calculadora.suma(num1, num2))
    elif opcion == '2':
        print("Resultado:", calculadora.resta(num1, num2))
    elif opcion == '3':
        print("Resultado:", calculadora.multiplicacion(num1, num2))
    elif opcion == '4':        
        if num2 != 0:
            print("Resultado:", calculadora.division(num1, num2))
        else:
            print("No se puede dividir entre cero") """

""" def suma(a, b):
    return a + b

def resta(a, b):
    return a - b

def multiplicacion(a, b):
    return a * b

def division(a, b):
    return a / b

def mi_calculadora(opcion, num1, num2):
    if opcion == '1':
        return suma(num1, num2)
    elif opcion == '2':
        return resta(num1, num2)
    elif opcion == '3':
        return multiplicacion(num1, num2)
    elif opcion == '4' and num2 != 0:
        return division(num1, num2)
    else:
        return "Opción no válida"

while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")

    opcion = input("Selecciona una opción: ")

    if opcion == '5':
        print("¡Gracias por usar Mi Calculadora!")
        break
    elif opcion < '1' or opcion > '5':
        print("Opción no válida")
    else:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))
        resultado = mi_calculadora(opcion, num1, num2)
        print("Resultado:", resultado) """


n:str=10
print(f'n str esta en la direccion: {id(n)}')
n:int='hola'
print(f'n str esta en la direccion: {id(n)}')
hola=10
print(f'n str esta en la direccion: {id(hola)}')
cadena='hola'
print(f'n str esta en la direccion: {id(cadena)}')
```
```
# TIPOS DE DATOS
numero: int =10
numero= 'dos'
print(numero)
```
## operadores logicos
```
True
False
if 5 > 4:
    print(True)
print(5>7)
```
 ## operadores numericos
 ```
received: bool = False
not received```
print(5+4)
print(5-4)
print(5*4)
print(5/4)
print(5//4) # division entera
print(5%4) # modulo o residuo
print(5**4) # x a la y
```
```
# funcion decorador se utiliza para modificar el comportamiento de otra funcion

from dataclasses import dataclass

@dataclass #decorators
class User:
    id: str
    name: str
    age: int

    def show_data(self):
        return f"ID: {self.id}\nNOMBRE: {self.name}\nAÑO: {self.age}"

if __name__ == "__main__":
    usuario1 = User("1","EMMANUEL",25)
    usuario2 = User("2","HEBER",25)
    usuario3 = User("3","FIGUEROA",25)
    usuario4 = User("4","RODRIGUEZ",25)
    usuarios = [usuario1,usuario2,usuario3,usuario4]
    for usuario in usuarios:
        print(usuario.show_data())
```
