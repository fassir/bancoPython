# Introdução
Este arquivo de leia-me contém informações sobre este projeto, mostrando seus seguintes pontos:
- [ Descrição do projeto ](#banco-python)
- [ Funcionalidades ](#funcionalidades)
- [ Requisitos ](#requisitos)
- [ Como usar ](#como-usar)
- [ Operações ](#operações)

# Banco Python

Este é um projeto simples de um sistema bancário em Python, onde é possível realizar operações de depósito, saque e consulta de extrato. O arquivo conta somente com o código [`code.py`](code.py), que implementa as funcionalidades básicas de um banco no backend e não possui interface gráfica. O objetivo é demonstrar conceitos básicos de programação, como controle de fluxo, manipulação de listas e funções.

Esta versão do projeto utiliza metodos de instanciamento de classes, encapsulamento e herança, permitindo a criação de contas e usuários para garantir segurança e organização dos dados. 

Foi adicionado um sistema de logs e data da operação, além de um sistema recursivo de listagem de contas para não causar sobrecarga ao servidor.

## Funcionalidades

- [x] Depositar
- [x] Sacar
- [x] Consultar Extrato
- [x] Limitar número de saques
- [x] Nova conta
- [x] Listar contas
- [x] Novo usuário

## Requisitos
- Python 3.x
- Biblioteca `datetime` para manipulação de datas
- Biblioteca `Path` para manipulação de caminhos de arquivos

## Como usar

1. Clone o repositório
2. Execute o arquivo `code.py` com o comando:
   ```bash
   python code.py
   ```
3. Siga as instruções no menu

## Operações
- **Depositar** [d]: Adiciona um valor à conta. Para depósitos, o valor deve ser positivo. Caso valor seja incorreto, uma mensagem de erro será exibida.

- **Sacar** [s]: Retira um valor da conta, respeitando o limite de saques. O valor deve ser positivo e não pode exceder o saldo disponível, além de respeitar o limite de saques diários (3). Caso o valor seja incorreto, sem o saldo em conta para a operação ou exceda o limite, uma mensagem de erro será exibida.

- **Consultar Extrato** [e]: Mostra o histórico de transações. Se não houver movimentações, o saldo atual será exibido. Caso haja movimentações, o extrato será exibido com os valores alterados e o saldo final.
- **Nova Conta** [nc]: Cria uma nova conta bancária. Solicita o nome do usuário, CPF e data de nascimento. O CPF deve ser único e válido. Caso o CPF já exista, uma mensagem de erro será exibida.
- **Listar Contas** [lc]: Exibe todas as contas cadastradas, mostrando o nome do usuário, CPF e data de nascimento.
- **Novo Usuário** [nu]: Cria um novo usuário. Solicita o nome completo, CPF, data de nascimento e endereço. O CPF deve ser único e válido. Caso o CPF já exista, uma mensagem de erro será exibida.

- **Sair** [q]: Encerra o programa.