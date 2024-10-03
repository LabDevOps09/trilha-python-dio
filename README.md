# Sistema Bancário ( Desafio 1)

Este é um simples sistema bancário em Python que permite ao usuário realizar operações de depósito, saque e visualizar o extrato da conta. A seguir estão as principais funcionalidades implementadas:

## Funcionalidades

### 1. Menu de Opções

O sistema apresenta um menu interativo com as seguintes opções:

- **[d] Depositar**: Para realizar um depósito.
- **[s] Sacar**: Para realizar um saque.
- **[e] Extrato**: Para visualizar o extrato da conta.
- **[q] Sair**: Para encerrar o programa.

### 2. Variáveis de Controle

- `saldo`: Armazena o saldo atual da conta, inicialmente definido como `0`.
- `limite`: Define o limite de saque permitido, que é de `R$ 500`.
- `extrato`: Armazena todas as movimentações (depósitos e saques) realizadas.
- `numero_saques`: Contador para rastrear quantos saques foram feitos.
- `LIMITE_SAQUES`: Define o número máximo de saques permitidos, que é `3`.

### 3. Depósito

- O usuário é solicitado a informar um valor para depósito.
- Se o valor for positivo, ele é adicionado ao saldo e registrado no extrato.
- Uma mensagem de confirmação é exibida após a realização do depósito.
- Se o valor for inválido (menor ou igual a zero), uma mensagem de erro é exibida.

### 4. Saque

- O usuário informa o valor a ser sacado.
- O sistema verifica três condições:
  - Se o valor solicitado é maior que o saldo disponível.
  - Se o valor solicitado excede o limite de saque permitido.
  - Se o número máximo de saques foi alcançado.
- Se todas as condições forem atendidas, o valor é subtraído do saldo e registrado no extrato.
- Uma mensagem de confirmação é exibida após a realização do saque.
- Se alguma das condições não for atendida, uma mensagem de erro correspondente é exibida.

### 5. Extrato

- Quando o usuário seleciona a opção de extrato, o sistema exibe todas as movimentações realizadas (depósitos e saques).
- Se não houver movimentações, uma mensagem informativa é exibida.
- O saldo atual da conta é exibido ao final do extrato, no formato `R$ xxx.xx`.

### 6. Encerramento

- Ao escolher a opção de sair, uma mensagem de despedida é exibida e o programa é encerrado.

## Exemplo de Uso

```plaintext
[d] Depositar
[s] Sacar
[e] Extrato
[q] Sair

=> d
Informe o valor do depósito: 200
Depósito de R$ 200.00 realizado com sucesso!

[d] Depositar
[s] Sacar
[e] Extrato
[q] Sair

=> s
Informe o valor do saque: 100
Saque de R$ 100.00 realizado com sucesso!

[d] Depositar
[s] Sacar
[e] Extrato
[q] Sair

=> e

================ EXTRATO ================
Depósito: R$ 200.00
Saque: R$ 100.00

Saldo atual: R$ 100.00
==========================================

# 🏦 Sistema Bancário Simples (Desafio 2)

Este é um sistema bancário simples em Python que permite a gestão de contas e usuários. O programa realiza operações como depósito, saque, exibição de extratos, criação de novos usuários e contas, e listagem de contas.

## Funcionalidades

O programa possui as seguintes funcionalidades:

1. **💰 Depositar**: Permite ao usuário realizar um depósito na conta.
2. **💵 Sacar**: Permite ao usuário realizar um saque da conta, respeitando limites de saldo e quantidade de saques.
3. **📊 Extrato**: Exibe o extrato da conta, mostrando depósitos e saques realizados.
4. **👤 Cadastrar Usuário**: Cria um novo usuário, armazenando informações como nome, data de nascimento, CPF e endereço.
5. **🏧 Cadastrar Conta Corrente**: Cria uma nova conta corrente vinculada a um usuário existente.
6. **📋 Listar Contas**: Exibe todas as contas cadastradas no sistema.
7. **🚪 Sair**: Encerra o programa.

## Estrutura do Código

O código foi modularizado com as seguintes funções:

- `menu()`: Exibe o menu de opções para o usuário.
- `depositar(saldo, valor, extrato)`: Realiza o depósito e atualiza o saldo e o extrato.
- `sacar(*, saldo, valor, extrato, limite, numero_saques, limite_saques)`: Realiza o saque e atualiza o saldo e o extrato.
- `exibir_extrato(saldo, /, *, extrato)`: Exibe o extrato da conta.
- `criar_usuario(usuarios)`: Cadastra um novo usuário.
- `filtrar_usuario(cpf, usuarios)`: Filtra o usuário pelo CPF.
- `criar_conta(agencia, numero_conta, usuarios)`: Cadastra uma nova conta corrente vinculada ao usuário.
- `listar_contas(contas)`: Lista todas as contas cadastradas.
- `main()`: Função principal que controla a lógica do programa.

## Regras de Implementação

- ⚙️ A função `sacar` deve receber argumentos apenas como *keyword arguments*.
- 🛠️ A função `depositar` deve receber argumentos apenas como *positional arguments*.
- 📋 A função `exibir_extrato` deve receber argumentos tanto como *positional* quanto como *keyword arguments*.
- 👥 O programa armazena os usuários em uma lista, composta por: nome, data de nascimento, CPF e endereço.
- 🏠 O endereço deve ser informado no formato: `logradouro, nro - bairro - cidade/sigla estado`.
- 🔢 O número da conta é sequencial, iniciando em 1.
- 🏦 A agência é fixada como "0001".

## Exemplo de Uso

1. 🖥️ Inicie o programa.
2. 📜 Escolha uma operação no menu.
3. 👣 Siga as instruções para realizar a operação desejada.

O código está estruturado para facilitar a manutenção e a adição de novas funcionalidades no futuro.








