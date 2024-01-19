def calcular_comissao(total_venda):
    if total_venda <= 5000:
        porcentagem_comissao = 5
        comissao = 0.05 * total_venda
        categoria = "Bom"
    elif total_venda <= 50000:
        porcentagem_comissao = 10
        comissao = 0.1 * total_venda
        categoria = "Ótimo"
    else:
        porcentagem_comissao = 15
        comissao = 0.15 * total_venda
        categoria = "Excelente"

    return comissao, porcentagem_comissao, categoria

def main():
    identificacao_vendedor = input("Digite a identificação do vendedor: ")
    codigo_peca = input("Digite o código da peça: ")
    preco_unitario = float(input("Digite o preço unitário da peça: "))
    quantidade_vendida = int(input("Digite a quantidade vendida: "))

    total_venda = preco_unitario * quantidade_vendida

    comissao, porcentagem_comissao, categoria = calcular_comissao(total_venda)

    print("\nResumo da venda:")
    print(f"Identificação do vendedor: {identificacao_vendedor}")
    print(f"Código da peça: {codigo_peca}")
    print(f"Preço unitário da peça: R${preco_unitario:.2f}")
    print(f"Quantidade vendida: {quantidade_vendida}")
    print(f"Total da venda: R${total_venda:.2f}")
    print(f"Comissão ({categoria} - {porcentagem_comissao}%): R${comissao:.2f}")

if __name__ == "__main__":
    main()
