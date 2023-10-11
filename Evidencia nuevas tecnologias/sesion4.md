<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->

1.Calculadora Básica: Crea una función llamada calculadora que tome tres argumentos: dos números y un operador (+, -, *, /). La función debe realizar la operación indicada en los dos números y devolver el resultado.
def calculadora(numero1, numero2, operador):
    if operador == '+':
        resultado = numero1 + numero2
    elif operador == '-':
        resultado = numero1 - numero2
    elif operador == '*':
        resultado = numero1 * numero2
    elif operador == '/':
        if numero2 != 0:
            resultado = numero1 / numero2
      
    
    return resultado


print(calculadora(12, 4, '+'))  
print(calculadora(20, 10, '-')) 
print(calculadora(18, 4, '*')) 
print(calculadora(100, 50, '/')) 

2.Contador de Palabras: Escribe una función llamada contar_palabras que tome una cadena como argumento y devuelva el número de palabras en esa cadena. Supón que las palabras están separadas por espacios.
def cont_palabras(frase):

    palabras = frase.split()
    
  
    return len(palabras)



texto = input("Ingrese una frase de texto: ")
cantidad_palabras = cont_palabras(texto)
print("Número de palabras en la cadena:", cantidad_palabras)

3.Solicita al usuario una cadena e imprime cuántas vocales contiene.
def contador_vocales(frase):
    vocales = "aeiouAEIOU"
    contador = 0
    i = 0
    
    while i < len(frase):
        if frase[i] in vocales:
            contador += 1
        i += 1
    
    return contador

frase = input("Ingrese una frase de texto: ")
cantidad_vocales = contador_vocales(frase)
print("La frase contiene", cantidad_vocales, "vocales.")

4.Cálculo de Potencia: Escribe una función llamada potencia que tome dos números enteros como argumentos, uno como base y otro como exponente, y devuelva el resultado de elevar la base al exponente.
def potencia(base, exponente):
    resultado = base ** exponente
    return resultado


base = 5
exponente = 2
resultado = potencia(base, exponente)
print(f"{base} elevado a la {exponente} da como resultado {resultado}")

5.Primo o No Primo: Escribe una función llamada es_primo que tome un número entero positivo como argumento y determine si es un número primo (es decir, solo es divisible por 1 y por sí mismo). La función debe devolver True si es primo y False si no lo es.

def primo(numero):
    
    if numero <= 1:
        return False
    
    
    for i in range(2, numero):
        if numero % i == 0:
            return False
    

    return True


print(primo(100))  
print(primo(23))



