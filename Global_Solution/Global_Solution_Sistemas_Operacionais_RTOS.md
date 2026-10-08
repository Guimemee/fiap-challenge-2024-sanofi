# ⚡ Global Solution 2024 — Sistemas Operacionais em Tempo Real (RTOS & Radares)

FACULDADE DE INFORMÁTICA E ADMINISTRAÇÃO PAULISTA (FIAP)

Sistemas Operacionais

SÃO PAULO – SP - 2024

BACHARELADO EM ENGENHARIA DA COMPUTAÇÃO

Sistemas Operacionais

Guilherme Macario da Silva - RM: 84057

Kaique Carvalho da Silva - RM: 93040

Julio Cesar de Andrade Santana – RM 88100

Questão 1:

Sensores:

6 radares (1 frontal, 1 traseiro, 2 lateral esquerda e 2 lateral direita)

4 câmeras (1 frontal, 1 traseira, 1 lateral esquerda e 1 lateral direita)

1 receptor de GPS

3 sensores de bordo (pressão, temperatura e pH)

Periodicidade de Leitura:

Radares: 100 ms

Câmeras: 200 ms

GPS: 100 ms

Sensores de Bordo: 300 ms

Tempo de CPU por Leitura:

Radar: 10 ms

Câmera: 15 ms

GPS: 5 ms

Condição de Escalabilidade:

A soma do tempo de CPU por leitura de todos os sensores deve ser menor ou igual a 1 ms.

Cálculo do Tempo Máximo para Leitura dos Sensores de Bordo:

Para determinar o tempo máximo que a leitura dos sensores de bordo pode levar, é necessário calcular o tempo total de CPU consumido pelas leituras dos demais sensores e subtraí-lo de 1 ms.

Tempo Total de CPU dos Radares:

6 radares * 10 ms/radar = 60 ms

Tempo Total de CPU das Câmeras:

4 câmeras * 15 ms/câmera = 60 ms

Tempo Total de CPU do GPS:

1 GPS * 5 ms/GPS = 5 ms

Tempo Total de CPU dos Sensores:

60 ms (radares) + 60 ms (câmeras) + 5 ms (GPS) = 125 ms

Tempo Máximo para Sensores de Bordo:

1 ms (condição de escalabilidade) - 125 ms (outros sensores) = -125 ms

Questão 2:Para resolver este problema, precisamos considerar alguns fatores:

Tempo total por medida: Cada medida requer 2 ms de CPU e 4 ms de E/S em cada thread, totalizando 6 ms por thread. Como são dois threads (um para cada tipo de dado), o tempo total por medida é de 12 ms.

Tempo total disponível: Temos 60 segundos de navegação, o que equivale a 60.000 ms (60 s * 1000 ms/s).

Limitação: O enunciado não especifica se a CPU ou a E/S são o fator limitante. Em sistemas reais, normalmente a E/S é mais lenta que a CPU. No entanto, para fins de cálculo, vamos considerar ambos os casos:

Cenário 1: CPU como fator limitante

Tempo disponível por thread: Como a CPU é compartilhada entre os dois threads, cada um tem, em média, metade do tempo disponível, ou seja, 30.000 ms.

Número de medidas por thread: 30.000 ms / 6 ms/medida = 5.000 medidas

Número total de medidas: Como cada medida requer ambos os threads, o número total de medidas é limitado pelo thread que processa menos medidas. Portanto, o número total de medidas é 5.000.

Cenário 2: E/S como fator limitante

Número de medidas por thread: 60.000 ms / 6 ms/medida = 10.000 medidas

Número total de medidas: 10.000 medidas (limitado pela E/S, que é mais lenta neste cenário)

Conclusão:

Em 60 segundos de navegação, o "FIAP Ocean Microplastic Cleaner" pode recepcionar:

5.000 medidas se a CPU for o fator limitante.

10.000 medidas se a E/S for o fator limitante.

É importante notar que, em um sistema real, o número de medidas pode ser menor devido a outros fatores, como overhead do sistema operacional e variações no tempo de processamento.

Questão 3:Para calcular o tempo de acesso efetivo à memória virtual, vamos analisar cada componente do tempo de acesso e suas probabilidades:

Acesso à página corrente:

Tempo: 1 µs

Probabilidade: 1 - 0.02 = 0.98 (98% das instruções acessam a página corrente)

Acesso à página em memória (não corrente):

Tempo: 1 µs (acesso à página não corrente)

Probabilidade: 0.02 * 0.40 = 0.008 (2% das instruções acessam outra página e 40% delas já estão em memória)

Acesso à página no disco (não corrente e modificada):

Tempo: 1 µs (acesso à página não corrente) + tempo de leitura do disco

Probabilidade: 0.02 * 0.60 * 0.50 = 0.006 (2% das instruções acessam outra página, 60% delas não estão em memória e 50% das substituídas foram modificadas)

Acesso à página no disco (não corrente e não modificada):

Tempo: 1 µs (acesso à página não corrente) + tempo de leitura do disco

Probabilidade: 0.02 * 0.60 * 0.50 = 0.006 (2% das instruções acessam outra página, 60% delas não estão em memória e 50% das substituídas não foram modificadas)

Cálculo do tempo de leitura do disco:

Tamanho da página: 4 kB = 4096 bytes

Taxa de transferência: 8 MB/s = 8.000.000 bytes/s

Tempo de leitura: 4096 bytes / 8.000.000 bytes/s = 0,000512 s = 0.512 µs

Cálculo do tempo efetivo de acesso à memória:

Tempo efetivo = (Tempo de acesso à página corrente * Probabilidade) + (Tempo de acesso à página em memória * Probabilidade) + (Tempo de acesso à página no disco (modificada) * Probabilidade) + (Tempo de acesso à página no disco (não modificada) * Probabilidade)

a) Três aplicações do sistema operacional VxWorks:

Sistemas aeroespaciais: O VxWorks é amplamente utilizado em sistemas de controle de voo, navegação e comunicação em aeronaves e espaçonaves, devido à sua confiabilidade e capacidade de resposta em tempo real.

Dispositivos médicos: O VxWorks é utilizado em equipamentos médicos como monitores cardíacos, ventiladores pulmonares e bombas de infusão, onde o tempo de resposta é crítico para a segurança do paciente.

Sistemas industriais: O VxWorks é utilizado em sistemas de controle de processos industriais, robótica e automação, onde a precisão e o tempo de resposta são essenciais para o bom funcionamento da produção.

b1) Duas aplicações de sistemas de tempo real rígido (crítico):

Controle de motores de aeronaves: O atraso no tempo de resposta pode levar a falhas catastróficas.

Sistemas de frenagem automotiva: O tempo de resposta deve ser extremamente rápido para garantir a segurança dos passageiros.

b2) Duas aplicações de sistemas de tempo real flexível (não crítico):

Sistemas de entretenimento a bordo (em aviões): Um pequeno atraso na resposta não é crítico.

Dispositivos de automação residencial: Um atraso na resposta pode causar inconvenientes, mas não representa um risco à segurança.