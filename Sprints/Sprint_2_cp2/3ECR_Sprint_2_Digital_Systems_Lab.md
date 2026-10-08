# 🔬 Resolução Técnica — Sprint 2 (Digital Systems Lab)

FACULDADE DE INFORMÁTICA E ADMINISTRAÇÃO PAULISTA (FIAP)

CHALLENGE Sanofi SPRINT 2

SÃO PAULO – SP

2024

BACHARELADO EM ENGENHARIA DA COMPUTAÇÃO – 1º SEMESTRE

Engenharia de Software

Vitor de Andrade Ferreira Dias – RM 957132

BENJAMIM LUCAS RODRIGUES GONÇALO - RM96026

Guilherme Macario da Silva - RM: 84057

Kaique Carvalho da Silva - RM: 93040

Julio Cesar de Andrade Santana – RM 88100

SÃO PAULO – SP

2024

Relatório de Progresso do Projeto de Automação e Centralização de Dados na Sanofi

1. Introdução e Conceituação Teórica

A Sanofi enfrenta desafios na gestão de dados e processos internos, impactando a eficiência e a tomada de decisões. Para solucionar esses problemas, estamos desenvolvendo uma solução que integra automação de processos, centralização de dados e visualização interativa.

Conceitos-chave:

Robotic Process Automation (RPA): Tecnologia que permite a automação de tarefas repetitivas e baseadas em regras, liberando os colaboradores para atividades de maior valor agregado.

Banco de Dados SQL e Data Warehouse: Estruturas para armazenar e organizar grandes volumes de dados de forma eficiente e segura, permitindo análises complexas e geração de relatórios personalizados.

ETL (Extract, Transform, Load): Processo de extração, transformação e carregamento de dados de diversas fontes para um destino centralizado, garantindo a qualidade e a consistência das informações.

Dashboards: Ferramentas de visualização de dados que permitem aos usuários explorar e analisar informações de forma intuitiva e interativa.

ODBC (Open Database Connectivity): Interface padrão para acessar diferentes tipos de bancos de dados, permitindo a integração de dados entre sistemas.

Inner Join: Operação em SQL que combina linhas de duas ou mais tabelas com base em uma condição de igualdade entre colunas relacionadas.

2. Objetivos e Escopo

O objetivo principal do projeto é otimizar os processos da Sanofi através da automação e centralização de dados, proporcionando maior eficiência, agilidade e qualidade nas informações. O escopo do projeto abrange:

Automação da coleta de dados de planilhas Excel, e-mails e sistema SAP.

Validação, limpeza e consolidação dos dados em um banco de dados SQL e Data Warehouse.

Unificação de dados de múltiplas planilhas em uma única planilha centralizada, utilizando INNER JOIN.

Criação de dashboards interativos e relatórios automatizados.

Implementação de conexão ODBC para atualização em tempo real da planilha centralizada.

Garantia da segurança e privacidade dos dados.

3. Contextualização e Arquitetura do Sistema

A solução proposta visa resolver as dores da Sanofi relacionadas à fragmentação de dados e ao controle manual de periféricos. A automação da coleta de dados eliminará o retrabalho e os erros humanos, enquanto a centralização em um banco de dados SQL e Data Warehouse permitirá análises mais completas e eficientes. A unificação de planilhas em uma única fonte centralizada, atualizada em tempo real via ODBC, facilitará o acesso e a gestão das informações.

Arquitetura do Sistema:

[Diagrama da arquitetura do sistema]

O diagrama apresenta os principais componentes da solução:

Fontes de Dados: Planilhas Excel, e-mails e sistema SAP.

RPA: Responsável pela automação da coleta de dados.

ETL: Extrai, transforma e carrega os dados para o banco de dados.

Banco de Dados SQL: Armazena os dados de forma estruturada e segura.

Data Warehouse: Consolida os dados para análise e geração de relatórios.

Dashboards: Interface para visualização e análise dos dados.

ODBC: Conecta a planilha centralizada ao banco de dados para atualização em tempo real.

4. Materiais e Métodos

Hardware: Servidor em nuvem para hospedar o banco de dados Oracle e a aplicação de dashboards.

Software:

Linguagem de programação Python para desenvolvimento dos scripts de RPA e ETL.

Banco de dados Oracle em nuvem.

Ferramenta de RPA (UiPath, Automation Anywhere, etc.).

Ferramenta de ETL (Talend, Pentaho, etc.).

Ferramenta de Business Intelligence (Power BI, Tableau, etc.) para criação de dashboards.

5. Cronograma

Sprint 1 (Concluído): Levantamento de requisitos, análise do problema e definição da solução.

Sprint 2 (Em andamento): Configuração do ambiente de desenvolvimento, criação do banco de dados Oracle em nuvem e desenvolvimento dos scripts de RPA e ETL.

Sprint 3: Implementação da conexão ODBC, desenvolvimento dos dashboards e testes integrados.

Sprint 4: Implantação da solução em ambiente de produção e treinamento dos usuários.

6. Desenvolvimento

Até o momento, foram realizados os seguintes desenvolvimentos:

Levantamento de requisitos e definição da solução.

Criação do banco de dados Oracle em nuvem e modelagem inicial das tabelas.

Desenvolvimento dos scripts de RPA para coleta de dados de planilhas e e-mails.

Início do desenvolvimento dos scripts de ETL.

7. Comentários e Perspectivas

A equipe está progredindo no desenvolvimento da solução, com foco na automação da coleta de dados e na criação do banco de dados. A colaboração com a Sanofi tem sido fundamental para o entendimento das necessidades e para a definição dos requisitos.

As perspectivas para as próximas etapas são:

Finalizar o desenvolvimento dos scripts de RPA e ETL.

Implementar a conexão ODBC e os dashboards.

Realizar testes integrados e ajustes finos na solução.

Implantar a solução em ambiente de produção e treinar os usuários.

Acreditamos que a solução proposta trará benefícios significativos para a Sanofi, melhorando a eficiência, a qualidade dos dados e a tomada de decisões.

8.Detalhes Técnicos da Solução

Automação da Coleta de Dados

A automação da coleta de dados será realizada através de RPA (Robotic Process Automation). Bots de software serão desenvolvidos em Python para acessar as planilhas Excel, extrair os dados relevantes e transferi-los para o banco de dados SQL. Essa automação eliminará a necessidade de intervenção manual, reduzindo o tempo gasto na coleta de dados e minimizando o risco de erros humanos.

Banco de Dados SQL e Data Warehouse

Um banco de dados SQL será criado para armazenar os dados de forma estruturada e segura. As tabelas do banco de dados serão modeladas de acordo com as informações presentes nas planilhas Excel, garantindo a integridade e a consistência dos dados.

Além do banco de dados SQL, será implementado um Data Warehouse para otimizar a análise e a geração de relatórios. O Data Warehouse será modelado dimensionalmente, separando os dados em tabelas de fatos (que armazenam as métricas de negócio) e tabelas de dimensões (que fornecem o contexto para as métricas). Essa estrutura permite análises mais rápidas e eficientes, além de facilitar a criação de relatórios personalizados.

Unificação de Dados com INNER JOIN

A unificação dos dados de múltiplas planilhas será realizada através de INNER JOIN no banco de dados SQL. Essa operação permite combinar linhas de diferentes tabelas com base em uma condição de igualdade entre colunas relacionadas. No caso da Sanofi, as chaves primárias e estrangeiras das tabelas serão utilizadas para estabelecer as relações entre os dados e garantir a correta combinação das informações.

O resultado do INNER JOIN será uma única tabela consolidada, contendo todas as informações relevantes das planilhas originais, sem redundâncias e com maior facilidade de análise.

Atualização em Tempo Real com ODBC

A planilha centralizada será conectada ao banco de dados SQL através de uma conexão ODBC (Open Database Connectivity). O ODBC é uma interface padrão que permite que diferentes aplicativos acessem e manipulem dados em bancos de dados heterogêneos.

A conexão ODBC permitirá que a planilha seja atualizada em tempo real, sempre que houver alterações nos dados do banco de dados. Isso garante que os usuários da Sanofi tenham acesso às informações mais recentes, sem a necessidade de intervenção manual.

Benefícios para a Sanofi

A implementação dessa solução trará os seguintes benefícios para a Sanofi:

Redução de Erros: A automação da coleta de dados e a centralização em um banco de dados SQL reduzirão significativamente os erros humanos e a inconsistência das informações.

Aumento da Eficiência: A automação de tarefas repetitivas e a atualização em tempo real da planilha centralizada liberarão os colaboradores para atividades mais estratégicas.

Melhora na Tomada de Decisões: A disponibilidade de dados consolidados e atualizados em um único local facilitará a análise e a tomada de decisões baseadas em informações precisas e confiáveis.

Redução de Custos: A otimização dos processos e a eliminação de retrabalho resultarão em economia de tempo e recursos.