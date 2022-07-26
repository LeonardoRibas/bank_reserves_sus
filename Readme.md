# bank_reserves_sus

## Modelo original

O modelo original simula pessoas que, andando randomicamente por um espaço, fazem trocas financeiras com outras pessoas que encontrarem, tendo 50% de chance de trocar 0 dinheiros, e 25% para tanto 5 quando 2 dinheiros.

## Modelo proposto

O modelo proposto difere-se do original com a adcição uma nova fator. A variável "suspicion", refere-se à desconfiança da população em relação ao banco. A ideia é que essa nova variável afetará a tomada de decisão das pessoas em relação aos depositos e saques feitos no banco. Tal lógica se baseia no fato de que quanto maior o nível de desconfiança, menos as pessoas estarão inclinadas e manter seu dinheiro no banco. A regra aplicada no modelo segue as seguintes condições: 

Quanto maior o nível de desconfiança maiores vão ser os valores dos saques e menores os valores depositados no banco principal.

- Os valores dos saques serão aumentados proporcionalmente em relação ao fator "suspicion" seguindo a regra da tabela:

| Suspicion     | Valor de acréscimo do saque 
| ------------- |:-------------:
| 10%           | +1 dinheiros
| 20%           | +2 dinheiros     
| 30%           | +3 dinheiros     
| 40%           | +4 dinheiros     
| 50%           | +5 dinheiros     
| 60%           | +6 dinheiros     
| 70%           | +7 dinheiros     
| 80%           | +8 dinheiros     
| 90%           | +9 dinheiros     
| 100%          | +10 dinheiros     

- Os valores dos depositos serão diminuidos proporcionalmente em relação ao fator "suspicion" seguindo a regra da tabela

| Suspicion     | Valor de decréscimo do deposito 
| ------------- |:-------------:
| 10%           | -1 dinheiros
| 20%           | -2 dinheiros     
| 30%           | -3 dinheiros     
| 40%           | -4 dinheiros     
| 50%           | -5 dinheiros     
| 60%           | -6 dinheiros     
| 70%           | -7 dinheiros     
| 80%           | -8 dinheiros     
| 90%           | -9 dinheiros     
| 100%          | -10 dinheiros 


## Motivação e Hipótese Causal


## Análise dos Dados
