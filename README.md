def calcular_imc(peso, altura):
    """Calcula el Índice de Masa Corporal (IMC)."""
    return peso / (altura ** 2)

def clasificar_imc(imc):
    """Clasifica el IMC en diferentes categorías."""
    if imc < 18.5:
        return "Bajo peso"
    elif 18.5 <= imc < 24.9:
        return "Peso normal"
    elif 25 <= imc < 29.9:
        return "Sobrepeso"
    else:
        return "Obesidad"

# Solicitar los datos del usuario
nombre = input("Introduce tu nombre: ")
apellido_paterno = input("Introduce tu apellido paterno: ")
apellido_materno = input("Introduce tu apellido materno: ")
edad = input("Introduce tu edad: ")
peso = float(input("Introduce tu peso (kg): "))
altura = float(input("Introduce tu estatura (m): "))

# Calcular el IMC
imc = calcular_imc(peso, altura)
clasificacion_imc = clasificar_imc(imc)

# Desplegar toda la información concatenada
print(f"\n{nombre} {apellido_paterno} {apellido_materno}, {edad} años, pesa {peso} kg, mide {altura} m y su IMC es {imc:.2f}. Clasificación: {clasificacion_imc}.")
