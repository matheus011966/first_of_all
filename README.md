MASTER_SENHA = 3684
MASTER_USUARIO = 'MATH'

def U():
    Usuario = (input(str("coloque seu usuario:")))
    if Usuario == MASTER_USUARIO:
        print(" ")
    else:
        print("Usario invalida! Programa encerado")
        exit()
print (U())

def I():
    senha = int(input ("coloque a senha:"))
    if senha == MASTER_SENHA:
        print("acesso liberado")
    else:
        print("senha invalida! Programa encerado")
        exit()
print (I())

def menu():
    print('***********************')
    print('*I - inserir senha')
    print('*R - Mudar senha')
    print("*S - sair")
    print('************************')

while True:
    menu()
    op = input(" O que você deseja fazer?")
    if op not in ('I', 'R', 'S'):
        print('Opção invalda')
        continue
    elif op == 'S':
        print('Programa finalizado')
        break
    elif op == 'I':
        print (I())
    elif op == 'R':
        print(U())
        MASTER_SENHA = int(input('Escolha uma nova senha'))

