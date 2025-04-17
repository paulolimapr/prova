# prova

1- # (20) Considerando a matriz abaixo, crie um laço for para calcular a média de uso de CPU por linha e imprima os resultados com 2 casas decimais.


uso_cpu = [
[20, 25, 40, 50, 45, 60, 55, 35, 70, 65],
[30, 35, 50, 60, 40, 55, 60, 45, 50, 55],
[15, 20, 30, 25, 35, 40, 45, 50, 55, 60],
[10, 15, 25, 35, 45, 50, 55, 60, 65, 70],
]




for linha in uso_cpu:
    media = sum(linha) / len(linha)
    print(f"A média de uso de CPU é: {media:.2f}")


    2-
    # (20) Crie uma função chamada alerta_uso que recebe como parâmetro uma lista com os valores de uso de CPU de uma região. A função deve retornar True se algum valor ultrapassar 85% de uso, e False caso contrário. Teste a função para todas as regiões da matriz.
def alerta_uso():
  for linha in uso_cpu:
    for valor in linha:
      if valor > 85:
        print("True")
    else:
      print("False")

alerta_uso()



3- 
# (20) Crie uma função chamada dados_crescente que recebe como parâmetro uma lista com os valores de uso de CPU de uma região. A função deve retornar a lista organizada em ordem crescente, do menor uso de CPU para o maior. Teste a função para todas as regiões da matriz
def dados_crescente():
  for linha in uso_cpu:
    linha.sort()
    print(linha)

dados_crescente()

4-
df = pd.DataFrame(uso_cpu)

df.columns = ['1h', '2h', '3h', '4h', '5h', '6h', '7h', '8h', '9h', '10h']

df
