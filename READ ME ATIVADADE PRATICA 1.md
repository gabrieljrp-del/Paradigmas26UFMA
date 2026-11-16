ALUNOS: GABRIEL JACINTO RODRIGUES PINTO, ANGELICA DA SILVA ALVES
na linha 7 utilizamos uma variavel para incluir o paradigma imperativo e declarativo
das linhas um a 22 criamos as funções
das linhas 15 a 46 fizemos uma função de alto nivel
os 3 tipos de dados são float para o saldo, int para o menu e boolean para o processar opção
CONSULTA AO CHATGPT:
Estou realizando uma avaliação de paradigmas de programação onde a tarefa é criar uma aplicação utilizando os paradigmas imperativo e funcional em python, com os requisitos de no mínimo 3 funções e 3 tipos de dados. estou fazendo uma aplicação de PDV com as opções consultar saldo, sacar, depositar e encerrar operação. Nesta aplicação conseguimos ter os 3 tipos de dados? se não como podemos inclui-la?
Sim. Uma aplicação de **PDV/caixa bancário em Python** pode facilmente atender ao requisito de **3 funções e 3 tipos de dados**, e inclusive permite demonstrar os paradigmas **imperativo e funcional**.

 ### 1\. Tipos de dados

 Na sua aplicação, você provavelmente já utiliza pelo menos estes 3 tipos:

 - **`float`** → para representar o saldo e os valores de saque/depósito.
- **`int`** → para representar a opção escolhida no menu.
- **`str`** → para mensagens, nome do usuário ou confirmação.
- **`bool`** → também pode ser utilizado para controlar se a operação continua ou encerra.

 Por exemplo:

```
saldo = 1000.50       # float
opcao = 1             # int
nome = "João"         # str
operacao_ativa = True # bool
```

 Então, **sim, sua aplicação já consegue cumprir o requisito de 3 tipos de dados**.

 ### 2\. Funções

 As próprias operações do seu PDV podem ser transformadas em funções:

```
def consultar_saldo(saldo):
    return saldo

def sacar(saldo, valor):
    if valor <= saldo:
        return saldo - valor
    return saldo

def depositar(saldo, valor):
    return saldo + valor
```

 Aqui você já possui **3 funções**.

 Além disso, poderia ter uma quarta função para o menu:

```
def exibir_menu():
    print("1 - Consultar saldo")
    print("2 - Sacar")
    print("3 - Depositar")
    print("4 - Encerrar")
```

 ### 3\. Como demonstrar os dois paradigmas

 Esse é um ponto interessante para sua avaliação.

 **Paradigma imperativo:** você pode utilizar variáveis que são modificadas durante a execução, estruturas `if/elif`, `while`, etc.

```
saldo = 1000.0

while True:
    opcao = int(input("Escolha uma opção: "))

    if opcao == 2:
        valor = float(input("Valor do saque: "))
        saldo = saldo - valor
```

 Nesse caso, `saldo` é alterado durante a execução.

 **Paradigma funcional:** você pode fazer as funções receberem valores e **retornarem novos valores**, sem alterar diretamente a variável original:

```
def sacar(saldo, valor):
    if valor <= saldo:
        return saldo - valor
    return saldo

def depositar(saldo, valor):
    return saldo + valor
```

 Por exemplo:

```
saldo = 1000.0

novo_saldo = sacar(saldo, 200.0)

print(saldo)       # 1000.0
print(novo_saldo)  # 800.0
```

 A função `sacar()` não modifica `saldo`; ela recebe um valor e produz outro. Isso é uma maneira simples de evidenciar o **paradigma funcional** em Python.

 ### Uma estrutura que atenderia bem ao trabalho

 Você poderia montar seu projeto aproximadamente assim:

```
PDV Bancário
│
├── consultar_saldo()
├── sacar()
├── depositar()
├── exibir_menu()
└── encerrar operação
```

 E utilizar:

 | Tipo | Utilização |
| --- | --- |
| `int` | Opção do menu |
| `float` | Saldo e valores monetários |
| `str` | Mensagens/nome do cliente |
| `bool` | Controle da operação |

**Uma observação:** para dinheiro, em uma aplicação real, seria preferível usar `Decimal` em vez de `float`, por questões de precisão. Mas, para um trabalho introdutório de paradigmas, `float` provavelmente é suficiente, salvo se o professor tiver especificado outra coisa.

 Se você quiser, posso montar **o código completo desse PDV em Python**, estruturado propositalmente para deixar **bem evidente onde está o paradigma imperativo, onde está o funcional, as 3+ funções e os 3+ tipos de dados**, para você poder apresentar e explicar na avaliação.
