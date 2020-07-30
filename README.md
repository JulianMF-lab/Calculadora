# Calculadora
Meu primeiro desafio no Python!

## Fazendo uma calculadora

def welcome():
    print("Bem-vinde à calculadora do Juju!")
    
def calculadora():

    # Definindo as 4 funções básicas
    def somar(x, y):
        return x + y

    def subtrair(x,y):
        return x - y

    def dividir(x,y):
        return x/y

    def multiplicar(x,y):
        return x*y

    # Printando as opções na tela
    print('Essa calculadora faz as seguintes operações')
    print('1. Somar')
    print('2. Subtrair')
    print('3. Dividir')
    print('4. Multiplicar')

    # Input do usuário
    def take_input():
        choice = input("Digite o número da operação que você deseja realizar: ")

        # Verifique se a escolha é uma das opções
        while True:
            try:                
                if choice in ('1','2','3','4'):
                                    num1 = float(input("Digite o primeiro número: "))                            
                                    num2 = float(input("Digite o segundo número: "))                                                    

                                    if choice == '1':
                                            print(num1, "+", num2, "=", somar(num1,num2))

                                    elif choice == '2':
                                            print(num1, "-", num2, "=", subtrair(num1,num2))

                                    elif choice == '3':
                                            print(num1, "/", num2, "=", dividir(num1,num2))

                                    elif choice == '4':
                                            print(num1, "*", num2, "=", multiplicar(num1,num2))

                else:
                    print("Por favor, escolha entre as opções disponíveis:")
                    print('1. Somar')
                    print('2. Subtrair')
                    print('3. Dividir')
                    print('4. Multiplicar')
                    take_input()
            
            except ValueError:
                print('Valor incompatível! Por favor, tente novamente.')
                
            else:
                break
        
        return choice
            
    take_input()    
            
    again()

# Definindo a função para realizar outra operação
def again():
    
    # Input do usuário
    calc_again = input('''
    Você deseja realizar outra operação? 
    Por favor, digite S para SIM e N para não
    ''')
        
        
    if calc_again.upper() == 'S':
        calculadora()
            
    if calc_again.upper() == 'N':
         print('Fique em casa!')
            
    else:
        again()
      
            
# Chamar a calculadora fora da função
welcome()
calculadora()
