# Challenge Sprint 3 - SISTEMAS OPERACIONAIS

**Título do Challenge:** Sanofi - EC Pharma Challenge
**Turma:** 3ECR | **Ano:** 2024
**Período para Entrega:** 09/09/2024
                                            -
                                            30/09/2024
**Status:** NOTA: 100
**Cabeçalho Original:** SISTEMAS OPERACIONAIS - Sérgio Ricardo Rota NOTA: 100

## 1. Enunciado e Instruções do Professor

A grande maioria das soluções, mesmo as que utilizam sistemas embarcados, compreende servidores Web, servidores de banco de dados e componentes em nuvem. Assim, é muito importante que estes computadores operem de maneira segura. Certamente, este cuidado se aplica ao "seu Projeto Sanofi".

Quando pensamos em manter nossos computadores seguros, a primeira ação que nos ocorre é instalar um software antivírus na máquina. Um software antivírus possui seu próprio banco de dados, com informações atualizadas sobre as ameaças encontradas no mundo digital. Este banco de dados é uma espécie de catálogo de vírus, que chamamos de vacina, ou seja, um conjunto de padrões de dados que representam algum vírus (é por isso que as vacinas são atualizadas regularmente).

Assim, quando executamos o software antivírus, ele faz uma varredura dos programas carregados na memória RAM e dos arquivos armazenados no disco rígido, em busca de padrões de dados representativos de vírus. Neste sentido, fazer uma varredura no disco, é equivalente a fazer uma operação de leitura de todos os arquivos armazenados no disco rígido.

Muito embora, já há algum tempo, existam discos de estado sólido (SSD – Solid State Drive), por questões mercadológicas, a maioria dos equipamentos – notebooks, desktops e servidores – ainda utilizam discos rígidos (HDD – Hard Disk Drive) como principal dispositivo de memória secundária.

Neste contexto, avalie as situações a seguir.

 

1) (3,0 pontos) Considere a superfície superior de um dos pratos de um disco rígido. Uma operação de seek (seek time) gasta 6 ms (milissegundo, 1x10-3 s) por trilha. Dois blocos logicamente consecutivos, ou seja, que se seguem em um arquivo, estão distantes, em média, 6 trilhas. Quanto tempo será gasto pelo software antivírus para fazer a varredura em um arquivo de 100 blocos, se a latência rotacional for de 150 ms e o tempo de transferência for de 25 ms por bloco?

 

2) Para melhorar o desempenho, é muito comum, reorganizar os arquivos de forma a diminuir o tempo de acesso aos mesmos – processo conhecido como desfragmentação do disco. Desfragmentar um arquivo requer um posicionamento e um atraso rotacional para ler o arquivo, seguido pela transferência dos dados do arquivo. Escrever o arquivo de volta para o disco requer o mesmo trabalho. Presumindo um tempo de posicionamento de 3 ms, um atraso rotacional de 2 ms, uma taxa de transferência de 320 MB/s (padrão Ultra-320 SCSI) e um tamanho médio de arquivo de 256 kB para todos os arquivos, responda as seguintes questões:

a) (4,0 pontos) Quanto tempo será gasto para ler um arquivo para a memória e então escrevê-lo de volta no disco em um novo local?

b) (3,0 pontos) Quanto tempo será necessário para compactar um disco de 1 TB de espaço utilizado?

Dica: Considere 1.024 bytes (2^10 bytes) como sendo 1.000 bytes (10^3 bytes).

