# bank_reserves_sus

## Modelo original

O modelo original simula pessoas que, andando randomicamente por um grid, fazem trocas financeiras com outras pessoas que encontrarem, tendo 50% de chance de trocar 0 dinheiros, e 25% para tanto 5 quando 2 dinheiros.

## Modelo proposto

O modelo proposto difere-se do original com a adcição uma nova fator. A variável "suspicion", que refere-se à desconfiança da população em relação ao banco. A ideia é que essa nova variável afetará a tomada de decisão das pessoas em relação aos depositos feitos. Tal lógica se baseia no fato de que quanto maior o nível de desconfiança, menos as pessoas estarão inclinadas e manter seu dinheiro guardado no banco. A regra aplicada no modelo segue as seguintes condições:

Quanto maior o nível de desconfiança, menores são as chances de serem efetuados depositos no banco principal.

- As chances de deposito no banco principal de um saldo positivo após uma troca serão diminuidas proporcionalmente em relação ao fator "suspicion" seguindo a regra da tabela

| Suspicion | Chances de depósito pós saldo positivo |
| --------- | :------------------------------------: |
| 0%        |                  100%                  |
| 10%       |                  90%                   |
| 20%       |                  80%                   |
| 30%       |                  70%                   |
| 40%       |                  60%                   |
| 50%       |                  50%                   |
| 60%       |                  40%                   |
| 70%       |                  30%                   |
| 80%       |                  20%                   |
| 90%       |                  10%                   |
| 100%      |                   0%                   |

Além da variável independente 'suspicion', foi introduzida outras duas variáveis (dependentes) ao modelo que serão análisadas: a reserva total do banco (reserves) e a quantidade total de dívidas (debts) geradas pelas transações economicas. Essas dívidas ocorrem quando as seguintes condições acontecem simultaneamente:

1.  O agente não possui dinheiro suficiente para pagar a transação.
2.  O banco não possui reserva o suficiente para emprestar ao agente para pagar a transação.

## Motivação e Hipótese Causal

A ideia por trás da variável independente proposta é de adicionar um fator historicamente relevante: a desconfiança no banco como instituição segura e estável.

Como visto acima, espera-se que, a medida em que essa desconfiança aumenta menos dinheiro será depositado no banco. isso, por consequência afetará diretamente as quantidade de dinheiro que o banco aramazenará em suas reservas, que por sua vez, limitará a disponibilidade de empréstimos, acarrentando em um número maior de dívidas geradas pelo modelo.

## Análise dos Dados

Ao alterar o fator "suspicion" foi possível observar consequências diretas nas variáveis dependentes:

- Savings (dinheiro total guardado por toda população): Quanto maior o valor de suspicion menor é a quantidade de dinheiro guardado pela população
- Wallets (dinheiro total disponível na carteira da população): Quanto maior o valor de suspicion maior é o valor de dinehiro guardado na carteira dos agentes
- Money (dinheiro total, savings + wallets): Quanto maior o valor de suspicion, o dinheiro gerado pelo sistema tende a ser menor
- Reserves (reserva de dinheiro disponível no banco para empréstimo): Quanto maior o valor de suspicion, menor são as reservas mantidas pelo banco.
- Debts (quantidade de dívidas total da população): quanto maior o valor de suspicion, maior é quantidade de dívidas geradas.
