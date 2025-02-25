# Praticando-Python
REVISÂO
python

# Programa que interage com o usuário e utiliza variáveis, estruturas de decisão, laços de repetição e funções

def calcular_media(notas):
    """Calcula a média de uma lista de notas."""
    return sum(notas) / len(notas)

def main():
    # Variáveis
    nome = input("Qual é o seu nome? ")
    notas = []
    
    # Interação com o usuário
    print(f"Olá, {nome}! Vamos calcular a média das suas notas.")
    
    # Laço de repetição com while
    while True:
        nota = input("Digite uma nota (ou 'sair' para finalizar): ")
        if nota.lower() == 'sair':
            break
        try:
            notas.append(float(nota))
        except ValueError:
            print("Por favor, digite um número válido.")

    # Estrutura de decisão
    if notas:
        media = calcular_media(notas)
        print(f"A sua média é: {media:.2f}")
        
        if media >= 7:
            print("Parabéns, você foi aprovado!")
        elif media >= 5:
            print("Você está de recuperação.")
        else:
            print("Infelizmente, você foi reprovado.")
    else:
        print("Nenhuma nota foi registrada.")

# Laço de repetição com for
for i in range(3):
    print(f"Executando o programa pela {i + 1}ª vez.")
    main()

if __name__ == "__main__":
    main()
