# LojaEletronicos.py
Trabalho linguagem de Python sobre controle de uma loja de eletrônicos

banco_dados= []

def mostrar_produto():
    contador = 1
    for item in banco_dados:
             print(f'{contador} - {item}')
             contador +=1

def selecionar_menu(opcao):
    if (opcao == '1'):
        produto = input('Digite o produto novo: ')       
        preco = float(input("Digite o preço do produto: R$"))
        quantidade = input("Digite a quantidade em estoque: ")
        banco_dados.append(produto)
        banco_dados.append(preco)
        banco_dados.append(quantidade)
    elif (opcao == '2'):
        mostrar_produto()
    elif (opcao == '3'):
        mostrar_produto
        numero_produto = int (input('Digite o produto que deseja excluir: '))
        del banco_dados[numero_produto -1] 
    elif (opcao == '4'):
        print ('Visualizar estoque atualizado...')
        mostrar_produto()
    elif (opcao == '0'):
        print ('Saindo do sistema...')
        exit(0)
    else:
        print ('Opcão incorreta, tente novamente!')
       

def exibir_menu():
        print('==== MENU ===')
        print('1 - Adicionar produto')
        print('2 - Atualizar produto')
        print('3 - Excluir produto')
        print('4 - Visualizar estoque')
        print('0 - Sair')
        opcao = input('Escolha uma opção: ')
        selecionar_menu(opcao)
        exibir_menu()


exibir_menu()
