# 📄 Resolução Oficial — 3ECR - Sprint 1 - Engenharia de Software .docx

FACULDADE DE INFORMÁTICA E ADMINISTRAÇÃO PAULISTA (FIAP),

Engenharia de Software

SÃO PAULO – SP

2024

BACHARELADO EM ENGENHARIA DA COMPUTAÇÃO

Engenharia de Software

Vitor de Andrade Ferreira Dias – RM 957132

Guilherme Macario da Silva - RM: 84057

Kaique Carvalho da Silva - RM: 93040

Julio Cesar de Andrade Santana – RM 88100

BENJAMIM LUCAS RODRIGUES GONÇALO - RM96026

2) Introdução

Projetos que estamos trabalhando são:Mariana

Análise de Dados Mariana A falta de uma visão unificada do histórico de compras e demanda de serviços leva à extração manual de informações, consumindo tempo significativo. É necessário desenvolver uma ferramenta que automatize a extração e análise de dados com critérios pré-estabelecidos, proporcionando informações de maneira visual e de fácil compreensão.

Raisa Barbosa

Novo Projeto: Controle de Mochilas e Periféricos Controle de Compras de Malas e acessórios para força de vendas, para acompanhar o que cada colaborador tem solicitado e com que frequência a troca ocorre. Isso poderá mensurar qualidade dos materiais, auxiliar no controle de trocas, tratativa dos fornecedores e auxiliar no planejamento do budget por Centro de Custo.

2.1) SOLUÇÃO

Descrição dos objetivos e do escopo (fronteiras; até onde vai) do seu projeto.

O nosso projeto consiste em unificar todas as planilhas que a Sanofi utiliza e fazer uma só em obdc, que atenda todas as necessidades deles.

Por trás dessa planilha existem muitas coisas interligadas que vão fazê-la acontecer.

Unificar todas as planilhas criando um banco de dados no SQL, seguindo o exemplo a seguir que é fictício.

Nesse caso fizemos dois bancos de dados simulando duas planilhas da Sanofi, estamos esperando eles enviarem as planilhas reais para inserir as colunas reais no banco de dados, porém isso não descarta nossa idea, nossa ideia é manter todos as planilhas dentro de um banco de dados só, de acordo com cada projeto, depois fazer um inner Join em todas as planilhas e trazer a informação consolidade para UMA planilha só.

Nosso projeto tem três passos.

Primeiro buscar de onde vem as informações da Sanofi.

Sabemos que eles extraem as informações do SAP, o SAP possui uma função que é o SAP SCRIPTING, esse SAP SCRIPT já é feito para automatizar as tarefas de rotina do SAP.

Podemos pegar esse script do SAP e transformá-lo de código de python, é um processo simples, porém exige nível de conhecimento de programação.

Transformação se dá necessário porque vamos utilizado como um processo de RPA, para extrair de forma automática os dados de lá.

Iremos fazer um processo de ETL, com knime ou pentaho, para jogar esses dados que foram extraídos do SAP para o nosso banco de dados do SQL.

Após extraídos os dados do e transformados através do processo de ETL ao SQL, vamos conectar o Excel no SQL e suprir as necessidades das planilhas e consolidar em uma só para Sanofi.

3-) Definição das tecnologias:

EXCEL:

Atualizar todos em tempo real através de obdc.

SAP e SAP SCRIPTING:

Verificar se conseguimos extrair informações da fonte de dados deles que é o SAP

KNIME:

Utilizamos para caráter de exemplo, o knime para ETL, mas podemos utilizar o pentaho também.

Python:

Para extrair informações do SAP, automatizar processos e também para agendar automações através do agendador de tarefas do Windows ou dentro do servidor de SQL.

Futuramente pensamos em utilizar aplicações web, API para extrair informações de sites da intranet da Sanofi.

EXEMPLO DE ETL:

Node 9, lê a planilha extraída do SAP.

Node 8, converte os dados da planilha.

Node 6 renomeia as colunas.

Node 7 Conecta no SQL.

Node 10 Escreve no banco de dados.

EXEMPLO REAL E FUNCIONAL DE CÓDIGO DE EXTRAÇÃO DE INFORMAÇÃO DO SAP

EXEMPLO REAL E FUNCIONAL DE CÓDIGO DE EXTRAÇÃO DE INFORMAÇÃO DO SAP

Lembrando que o código acima ele não está com as bibliotecas que iremos utilizar (importar), quando ele estiver pronto e funcional vamos introduzir eles.

Também vamos contextualizar e padronizar o programa de acordo com as normas UML

EXCEL OBDC:

ESSE DOIS PASSOS SÃO OPÇÕES DO EXCEL, ELE CONECTA FONTE DE DADOS DO SQL NO EXCEL.

NESSE IMAGEM ACIMA PODEMOS COLOCAR A QUERY DO SQL COM INNER JOIN EM OUTRAS TABELAS QUE JÁ VÃO ESTAR NO NOSSO BANCO DE DADOS.

A PARTE DA ATUALIZAÇÃO DA PLANILHA PODE SER ESCOLHIDA PELO USUÁRIO, SEJA QUANDO ABRIR A PLANILHA, SEJA EM 5 EM 5 MINUTOS, COMO FOR A NECESSIDADE DELE E CLARO NÃO DEVEMOS ESQUECER QUE O BANCO DE DADOS DEVE ESTAR ATUALIZADO E AUTOMATIZADO.

CONCLUSÃO

Hoje nos ainda estamos à mercê de mentorias com a Sanofi.

Sabemos que a nossa ideia pode suprir mais de um projeto, queremos dar uma solução para Sanofi que não torne um problema para o usuário final, queremos manter o que eles têm mas implementar tecnologia no back-end deles, eles vão continuar utilizando as planilhas, porém vamos fazer o trabalho de bastidores deles para tornar tudo mais produtivo e mais modernizado e assim aumentar a efetividade deles.

Até outubro queremos colocar as ideias que temos hoje em prática e funcional, a partir de setembro vamos começar a utilizar inteligência artificial na nossa solução para análise preventiva de dados e também vamos entender as necessidades dele e como utilizar a inteligência artificial para tornar nosso projeto mais assertivo e mais funcional.

Também estamos pensando em fazer uma aplicação web para melhorar o sistema deles, que hoje é muito engessado, devido a rotina deles.

Por enquanto temos muito a trabalhar na ideia que temos e muito a desenvolver e descobrir conforme formos fazendo as mentorias.