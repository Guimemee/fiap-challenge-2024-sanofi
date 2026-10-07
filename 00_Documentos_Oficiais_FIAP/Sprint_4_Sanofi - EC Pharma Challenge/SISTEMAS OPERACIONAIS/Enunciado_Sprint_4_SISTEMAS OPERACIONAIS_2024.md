# Challenge Sprint 4 - SISTEMAS OPERACIONAIS

**Título do Challenge:** Sanofi - EC Pharma Challenge
**Turma:** 3ECR | **Ano:** 2024
**Período para Entrega:** 07/10/2024
                                            -
                                            01/11/2024
**Status:** NOTA: 100
**Cabeçalho Original:** SISTEMAS OPERACIONAIS - Sérgio Ricardo Rota NOTA: 100

## 1. Enunciado e Instruções do Professor

O gerenciamento e desempenho dos dispositivos de entrada e saída (E/S) é uma parte importante da grande maioria das soluções computacionais. Neste contexto, responda as seguintes questões:

 

1) A expressão fast wide SCSI-II significa um bus SCSI que opera a uma taxa de transferência de dados da ordem de megabytes (MB) por segundo quando movimenta um pacote de dados entre a controladora de disco e o disco. Suponha que um drive de disco gire a 9.000 rpm, tenha setores de 512 bytes e contenha 240 setores por trilha.

a) (3,0 pontos) Qual é a taxa de transferência sustentada por este drive em megabytes por segundo?

b) (2,5 pontos) Neste sistema há um controlador de DMA que tem 4 canais. Este controlador de DMA é capaz de requisitar uma palavra de 32 bits a cada 250 ns (250 x 10^-9 s). Este controlador de DMA é rápido o suficiente para trabalhar com este bus SCSI ou ele representará um gargalo? Justifique sua resposta.

 

2) (1,5 ponto) Em relação aos device drivers, assinale a opção INCORRETA:

(A) Como os device drivers são códigos reentrantes que executam em modo núcleo (kernel), qualquer erro de programação pode comprometer por completo o funcionamento do sistema computacional. Por isto, um device driver deve ser cuidadosamente desenvolvido e testado.

(B) Os device drivers fazem parte do núcleo do sistema operacional e, geralmente, são escritos em linguagem assembly ou linguagem C.

(C) Devido ao alto grau de dependência entre os device drivers e o restante do núcleo do sistema operacional, os fabricantes desenvolvem, para um mesmo dispositivo, diferentes device drivers, um para cada sistema operacional.

(D) Tipicamente, após emitir uma sequência de comandos para um dispositivo, o device driver deste dispositivo espera até que o dispositivo realize a operação solicitada, de modo que o device driver se autobloqueia até que uma interrupção ocorra e o desbloqueie.

(E) Normalmente, os device drivers são aptos a fazer chamadas ao sistema, mas, no entanto, eles podem interagir diretamente com o núcleo do sistema operacional para executar tarefas como: alocar e liberar páginas físicas de memória para serem usadas como buffers, acessar o controlador de DMA (Direct Memory Access), acessar o controlador de interrupção etc.

 

3) (1,5 ponto) Os módulos de E/S podem operar de três maneiras básicas: E/S programada (polling ou inquirição), E/S via interrupções e E/S via acesso direto à memória (DMA – Direct Memory Access). Com relação a esse assunto, assinale a opção INCORRETA:

(A) A maioria dos controladores de DMA usa endereçamento de memória física para suas transferências. O uso de endereços de memória física requer que o sistema operacional converta o endereço virtual do buffer de memória pretendido em um endereço físico e escreva esse endereço físico no registrador de endereço do controlador de DMA.

(B) Um dos grandes problemas relacionados à utilização de um controlador de DMA advém do fato do controlador de DMA e do processador não conseguirem utilizar os barramentos de dados e endereços simultaneamente. Isto é, durante o tempo em que o controlador de DMA estiver utilizando os barramentos de dados e endereços a operação do processador é completamente interrompida.

(C) As técnicas de E/S programada e E/S via interrupções limitam a velocidade de transferência dos dados do módulo de E/S para a memória. Além disto, a CPU fica comprometida com a monitoração do módulo de E/S (no caso de E/S programada) ou com a sobrecarga imposta pelo tratamento das interrupções (no caso de E/S via interrupções).

(D) Na técnica de E/S programada os dados são trocados entre o processador e o módulo de E/S. Ou seja, o processador deve executar um programa que verifique o estado do módulo de E/S, envie o comando que deve ser executado e aguarde o resultado do comando para então efetuar a transferência entre o módulo de E/S e algum registrador do processador.

(E) Para superar o problema da espera da CPU por operações nos dispositivos periféricos pode ser utilizado o mecanismo das interrupções, ou seja, E/S via interrupções. Uma interrupção permite que um módulo de E/S ganhe a atenção imediata da CPU para finalizar sua tarefa.

 

4) (1,5 ponto) Processadores atuais incluem mecanismos para o tratamento de situações especiais, conhecidas como interrupções. Em uma interrupção, o fluxo normal de instruções é interrompido para que a causa da interrupção seja tratada. Em relação a esse assunto, assinale a opção INCORRETA:

(A) O processador pode auto interromper-se para tratar exceções de execução, tais como um erro em uma operação aritmética, uma tentativa de execução de instrução ilegal ou uma falha de página em memória virtual.

(B) Geralmente, a tabela de vetores de interrupção é armazenada na memória baixa, nas primeiras posições de memória RAM. Estas posições mantêm os endereços das rotinas de tratamento de interrupção para os diversos dispositivos. Este array de endereços, ou vetor de interrupções é então indexado por um único número de dispositivo fornecido com a solicitação de interrupção, de modo a fornecer o endereço da rotina de tratamento de interrupção para o dispositivo que está provocando a interrupção.

(C) Quando uma solicitação de interrupção de um dispositivo chega, caso a CPU esteja executando uma instrução, em geral, a interrupção fica pendente até o término da execução da instrução em questão.

(D) Geralmente, são assinalados números para as interrupções, onde as interrupções de menor número têm prioridade sobre as interrupções de maior número. Isto significa que uma interrupção 5 terá prioridade de processamento sobre uma interrupção 7, mas poderá ser interrompida por uma interrupção 3.

(E) Rotinas de tratamento de interrupção devem ser executadas com o mecanismo de interrupção inibido, pois esse tipo de rotina não permite funções aninhadas.

