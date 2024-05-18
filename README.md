from itertools import product

def generar_lenguaje(alfabeto, potencia):
    lenguaje = []
    for i in range(potencia + 1):
        combinaciones = product(alfabeto, repeat=i)
        lenguaje.extend([''.join(combinacion) for combinacion in combinaciones])
    return lenguaje

# Entrada
n = int(input("Ingrese el tamaño del alfabeto: "))
alfabeto = input("Ingrese los elementos del alfabeto separados por espacio: ").split()
P = int(input("Ingrese la potencia del lenguaje: "))

# Generar el lenguaje
Lp = generar_lenguaje(alfabeto, P)

# Salida
print("Elementos del lenguaje L^{}:".format(P))
for elemento in Lp:
    print(elemento)
