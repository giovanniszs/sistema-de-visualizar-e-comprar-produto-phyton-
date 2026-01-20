while True:
    print("\n=== LOJA ===")
    print("1 - Ver Produto")
    print("2 - Sair")
    opcao = int(input("Escolha uma opção: "))
    
    if opcao == 1:
        print("\n=== PRODUTO ===")
        print("Camisa SANTOS FC 25/26")
        print("Preço: R$299.90")
        
        comprar = input("\nDeseja comprar? (s/n): ")
        
        if comprar.lower() == 's':
            quantidade = int(input("Quantas unidades? (máximo 5): "))
            
            if quantidade <= 5 and quantidade > 0:
                preco_total = quantidade * 299.90
                print(f"\n=== CARRINHO ===")
                print(f"Quantidade: {quantidade}")
                print(f"Total: R${preco_total:.2f}")
                print("Compra realizada com sucesso!")
            elif quantidade > 5:
                print("Desculpe! Essa quantidade não está disponível no estoque!")
            else:
                print("Quantidade inválida!")
    
    if opcao == 2:
        print("Encerrando sistema...")
        break
