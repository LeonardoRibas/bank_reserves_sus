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


## Análise dos Dados
