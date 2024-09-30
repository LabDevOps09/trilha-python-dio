# Sistema Bancário

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









