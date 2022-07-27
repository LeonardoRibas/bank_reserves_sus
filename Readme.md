# bank_reserves_sus

## Modelo original

O modelo original simula pessoas que, andando randomicamente por um espaço, fazem trocas financeiras com outras pessoas que encontrarem, tendo 50% de chance de trocar 0 dinheiros, e 25% para tanto 5 quando 2 dinheiros.

## Modelo proposto

O modelo proposto difere-se do original com a adcição uma nova fator. A variável "suspicion", refere-se à desconfiança da população em relação ao banco. A ideia é que essa nova variável afetará a tomada de decisão das pessoas em relação aos depositos feitos no banco. Tal lógica se baseia no fato de que quanto maior o nível de desconfiança, menos as pessoas estarão inclinadas e manter seu dinheiro no banco. A regra aplicada no modelo segue as seguintes condições: 

Quanto maior o nível de desconfiança, menores são as chances de serem efetuados depositos no banco principal.

- As chances de deposito no banco principal de um saldo positivo após uma troca serão diminuidas proporcionalmente em relação ao fator "suspicion" seguindo a regra da tabela

| Suspicion     | Chances de depósito pós saldo positivo
| ------------- |:--------------------------------------:
| 0%            | 100% 
| 10%           | 90% 
| 20%           | 80%      
| 30%           | 70%      
| 40%           | 60%      
| 50%           | 50%      
| 60%           | 40%      
| 70%           | 30%      
| 80%           | 20%      
| 90%           | 10%      
| 100%          | 0%  


## Motivação e Hipótese Causal

A ideia por trás da variável independente proposta é de adicionar um fator historicamente relevenate: a desconfiança no banco como instituição segura e estável.

Como visto acima, espera-se que, a medida em que essa desconfiança aumenta menos dinheiro será depositado no banco. isso, por consequência afetará diretamente as quantidade de dinheiro que o banco aramazenará em suas reservas, que por sua vez, limitará a disponibilidade de empréstimos, acarrentando em um número menor de empréstimos e de dinheiro gerado no sistema


## Análise dos Dados

Ao alterar o fator "suspicion" nos seguintes valores: 0% -> 50% -> 100%. Foi possível observar consequências diretas nas variáveis dependentes:

- Savings (dinheiro total guardado por toda população): Quanto maior o valor de suspicion menor é a quantidade de dinheiro guardado pela população
- Wallets (dinheiro total disponível na carteira de toda população): Quanto maior o valor de suspicion maior é o valor de dinehiro guardado na carteira das população
- Money (dinheiro total, savings + wallets): Quanto maior o valor de suspicion, o dinheiro gerado pelo sistema tende a ser menor

