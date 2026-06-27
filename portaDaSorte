import random 

porcentagem_inicio = [2, 5, 7, 4, 1, 8, 11, 14] #porcentagens possiveis para cada porta
valor_acumulado = 0
rodada = 1
print(" Bem vindo ao JOGO DAS PORTAS! \n Escolha uma porta entre as três e veja até onde sua sorte te leva. \n Boa sorte!") 

while True: 
    p0, p1, p2 = random.choices(porcentagem_inicio, k=3) 
    porta = [[1, p0], [2, p1], [3, p2]] #junta N° da porta em uma porcentagem aleatória 

    print(f'+-------RODADA {rodada}-------+')
    print(f'Escolha uma porta:')
    print("   1    2    3")
    print("  🚪   🚪   🚪")

    while True:
            try:
                escolha = int(input('R: '))
                if escolha in (1, 2, 3):
                    break
                print('Número Inválido. Escolha 1, 2 ou 3.')
            except ValueError:
                print('Digite um número inteiro.') 


    print(f'\nValor em cada porta:')
    print("   1    2    3")
    print(f'   {porta[0][1]}%   {porta[1][1]}%   {porta[2][1]}%')


    result = [valor for num, valor in porta if num == escolha] # pegar porcentagem com abse na escolha da porta

    if result:  
        porta_escolhida = result[0] 
        valor_acumulado += porta_escolhida
        print(f'\nPorta escolhida: {escolha}, porcentagem: {porta_escolhida}%')
        print(f'Chance acumulada: {valor_acumulado}%')
    
    if valor_acumulado > 100: 
        valor_acumulado = 100 

    chance = [] 
    chance_porta = int(valor_acumulado)
    chance_fim = int(100 - chance_porta)

    for i in range(chance_porta): # laço com for para definir porcentagem de continuar ou acabar
        chance.append("x")        # ex: [x, x, x, y, y, y, y, y, y, y] 30% (3x, 7y) 
    for i in  range(chance_fim):
        chance.append("y")

    fim = random.choice(chance)
    if fim == "y":
        print("Jogo Continua.\n") 
        rodada += 1
    elif fim == "x":
        print("GAME OVER!")
        print(f'\nParabéns você chegou até a rodada {rodada}!')
        break
    else:
        print("Erro.") 
