import random

def escolher_dias_academia(num_dias):
    dias_da_semana = ["Segunda-feira", "Terça-feira", "Quarta-feira", "Quinta-feira", "Sexta-feira", "Sábado", "Domingo"]
    
    if num_dias > len(dias_da_semana):
        raise ValueError("O número de dias não pode ser maior que 7")
    
    dias_escolhidos = random.sample(dias_da_semana, num_dias)
    return dias_escolhidos

# Solicitar ao usuário o número de dias que ele quer ir à academia
num_dias = int(input("Quantos dias na semana você quer ir à academia? "))

try:
    dias = escolher_dias_academia(num_dias)
    print("Você deve ir à academia nos seguintes dias:")
    for dia in dias:
        print(dia)
except ValueError as e:
    print(e)
