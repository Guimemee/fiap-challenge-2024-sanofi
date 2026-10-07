# Challenge Sprint 2 - SISTEMAS OPERACIONAIS

**Título do Challenge:** Sanofi - EC Pharma Challenge
**Turma:** 3ECR | **Ano:** 2024
**Período para Entrega:** 21/05/2024
                                            -
                                            20/06/2024
**Status:** NOTA: 80
**Cabeçalho Original:** SISTEMAS OPERACIONAIS - Sérgio Ricardo Rota NOTA: 80

## 1. Enunciado e Instruções do Professor

**Fale com a “San”:**

1) Considerando-se os vários desafios apresentados pela Sanofi, o primeiro atendimento será realizado por assistentes virtuais (*chatbots*). Neste cenário, as demandas serão processadas em um servidor *multithread*, responsável por realizar múltiplos atendimentos, provenientes de assistentes virtuais (*chatbots*). Cada entrada de usuário, vinda de um assistente virtual, é uma requisição de trabalho. E cada requisição resolvida significa: a requisição foi obtida, foi processada e despachada, e o restante do processamento foi concluído (como a exposição dos resultados ao usuário). O servidor está equipado com um processador *multicore* com 16 núcleos de processamento (16 *cores*).

*Em cada um dos oito primeiros cores* está rodando um algoritmo que faz com que o atendimento tenha as seguintes características: são necessários 5 ms (milissegundo, 1x10–3 s) para resolver cada requisição de trabalho, presumindo que todos os dados necessários já estejam na memória *cache*. Se for necessária uma operação de disco, o que ocorre em um quarto (1/4) das requisições de trabalho, será preciso um tempo adicional de 10 ms, durante o qual o *thread* permanece bloqueado.

Em cada um dos oito últimos *cores* está rodando um algoritmo que faz com que o atendimento tenha as seguintes características: são necessários 10 ms para resolver cada requisição de trabalho, presumindo que todos os dados necessários já estejam na memória *cache*. Se for necessária uma operação de disco, o que ocorre em um sexto (1/6) das requisições de trabalho, será preciso um tempo adicional de 20 ms, durante o qual o *thread* permanece bloqueado.

 

Diante deste cenário, responda:

a) Quantas requisições por segundo cada tipo de algoritmo pode tratar?

b) Quantas requisições por segundo os oito primeiros *cores*, em conjunto, são capazes de resolver?

c) Quantas requisições por segundo os oito últimos *cores*, em conjunto, são capazes de resolver?

d) No total, este servidor é capaz de atender quantas requisições por segundo?

e) Quantos servidores são necessários para atender 30.000 requisições por segundo?

f) Caso os processadores *multicore* sejam equipado com a tecnologia *hyper-threading*, quantos servidores serão necessários para atender 30.000 requisições por segundo?

