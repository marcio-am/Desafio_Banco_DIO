menu = """

[d] Depositar
[s] Sacar
[e] Extrato
[q] Sair

=> """

saldo = 0
limite = 500
extrato = ""
numero_saques = 0
LIMITE_SAQUES = 3

while True:

    opcao = input(menu)

    if opcao == "d":

        valor = float(input("Informe o valor do depósito: "))
                

        if valor>0:

            saldo += valor
            extrato += f"Depósito: R$ {valor:.2f}\n"

            print("Depósito realizado com sucesso.")
        else:
            print("Operação falhou! O valor informado é inválido.")

    elif opcao == "s":
        valor = float(input("Informe o valor do saque: "))

        if numero_saques <= LIMITE_SAQUES and valor <= limite:

            saldo -= valor

            extrato += f"Saque: R$ {valor:.2f}\n"

            print("Saque efetuado com sucesso!")
            
        elif numero_saques >= LIMITE_SAQUES:

            print("Operação falhou! Número máximo de saques diários excedido!")
        elif valor >= saldo:
            print("Operação falhou! Seu saldo é insuficiente!")

        elif valor >= limite:
            print("Operação falhou! O valor excede o limite máximo permitido!")

        else:
            print("Operação falhou! O valor informado é inválido.")
        
        numero_saques += 1
        saldo -= valor

    elif opcao == "e":
        print("\n================ EXTRATO ================")
        print("Não foram realizadas movimentações." if not extrato else extrato)
        print(f"\nSaldo: R$ {saldo:.2f}")
        print("==========================================")

    elif opcao == "q":
        break

    else:
        print("Operação inválida, por favor selecione novamente a operação desejada.")
