# 💻 Resolução Técnica — Sprint 2 (Engenharia de Software)

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

Análise e Otimização de Processos na Sanofi: Relatório Técnico Detalhado

1. Contexto e Problemas

A Sanofi, como muitas empresas modernas, enfrenta desafios na gestão de dados e processos internos. Dois problemas críticos foram identificados:

Fragmentação de Dados: Dados cruciais para a tomada de decisões estão dispersos em múltiplas planilhas, dificultando a análise, a geração de relatórios e a obtenção de insights acionáveis. Essa fragmentação leva a ineficiências, retrabalho e potencial para erros humanos.

Controle Manual de Periféricos: O processo de gestão de periféricos para home office (mochilas, mouses, teclados, etc.) é inteiramente manual. A comunicação entre as partes responsáveis depende de ligações telefônicas e e-mails, e o rastreamento de pedidos é feito em planilhas separadas. Este processo é suscetível a erros, atrasos e perda de informações, impactando a produtividade dos funcionários.

2. Solução Proposta

Para solucionar esses problemas, propomos uma abordagem holística que integra automação, centralização de dados e visualização interativa:

Automação de Processos:

Robotic Process Automation (RPA): Bots de software serão implementados para extrair dados automaticamente de diversas fontes (SAP, e-mails, sistemas legados), eliminando a necessidade de entrada manual de dados e reduzindo o risco de erros.

Integração de APIs: APIs serão utilizadas para conectar sistemas e facilitar o fluxo de dados entre eles, agilizando processos e garantindo a consistência das informações.

Centralização de Dados:

Banco de Dados SQL: Um banco de dados SQL centralizado será criado para armazenar todos os dados relevantes de forma estruturada e segura. Isso permitirá consultas eficientes, geração de relatórios personalizados e integração com ferramentas de análise.

ETL (Extract, Transform, Load): Processos ETL serão implementados para extrair dados de fontes diversas, transformá-los em um formato consistente e carregá-los no banco de dados central.

Visualização de Dados:

Dashboards Interativos: Dashboards personalizados serão desenvolvidos para fornecer aos gestores e analistas uma visão clara e em tempo real dos dados. Gráficos, tabelas e indicadores-chave de desempenho (KPIs) permitirão identificar tendências, anomalias e oportunidades de melhoria.

Relatórios Automatizados: Relatórios periódicos serão gerados automaticamente, poupando tempo e garantindo que as informações relevantes cheguem às partes interessadas de forma consistente.

3. Levantamento de Requisitos

Devido à natureza sensível dos dados e à ausência de um acordo de confidencialidade formal no início do projeto, optamos por realizar entrevistas presenciais com os colaboradores da Sanofi. Essa abordagem permitiu:

Compreensão Detalhada: Obter informações detalhadas sobre os fluxos de trabalho, as dificuldades enfrentadas e as expectativas dos usuários em relação à solução.

Flexibilidade: Adaptar as perguntas e o foco da entrevista em tempo real, explorando tópicos relevantes que surgiram durante a conversa.

Construção de Rapport: Estabelecer um relacionamento com os colaboradores, o que pode ser útil para o engajamento e a colaboração em fases posteriores do projeto.

Desafios: A principal limitação das entrevistas foi a falta de acesso a dados concretos e sistemas internos, o que dificultou a análise técnica detalhada. No entanto, as informações qualitativas obtidas foram valiosas para definir os requisitos do projeto.

4. Requisitos Detalhados

Com base nas entrevistas e na análise do problema, os seguintes requisitos foram levantados:

Funcionalidades:

Automação da coleta de dados de planilhas Excel, e-mails e sistema SAP.

Validação e limpeza de dados para garantir a qualidade e consistência.

Armazenamento seguro e centralizado de dados em um banco de dados SQL.

Criação de dashboards interativos com filtros, gráficos e KPIs personalizáveis.

Geração de relatórios automatizados em formatos como PDF e Excel.

Integração com o sistema de autenticação da empresa para controle de acesso.

Usabilidade:

Interface intuitiva e fácil de usar, mesmo para usuários não técnicos.

Design responsivo para acesso em diferentes dispositivos (desktops, tablets, smartphones).

Documentação clara e treinamento para usuários.

Desempenho:

Tempo de resposta rápido para consultas e geração de relatórios.

Capacidade de lidar com grandes volumes de dados de forma eficiente.

Segurança:

Implementação de medidas de segurança para proteger os dados confidenciais, como criptografia, controle de acesso e backups regulares.

Conformidade com as políticas de segurança da Sanofi e com as regulamentações aplicáveis (LGPD, GDPR, etc.).

Escalabilidade:

Arquitetura flexível e modular para facilitar a adição de novas funcionalidades e fontes de dados no futuro.

5. Próximos Passos

Os próximos passos incluem:

Definição da Arquitetura: Detalhar a arquitetura da solução, incluindo a escolha das tecnologias (Python, RPA, SQL Server, Power BI, etc.), a estrutura do banco de dados e o design da interface.

Desenvolvimento: Implementar a solução, incluindo a criação dos bots de RPA, a configuração do banco de dados, o desenvolvimento dos dashboards e a integração com os sistemas existentes.

Testes: Realizar testes rigorosos para garantir a funcionalidade, o desempenho e a segurança da solução.

Implantação: Implantar a solução em ambiente de produção, com treinamento para os usuários e monitoramento contínuo.

Manutenção e Evolução: Acompanhar o desempenho da solução, corrigir eventuais problemas e implementar melhorias contínuas com base no feedback dos usuários.

Este relatório técnico detalhado visa fornecer à Sanofi uma visão clara e abrangente da solução proposta para os problemas de gestão de dados e controle de periféricos. Estamos confiantes de que a implementação desta solução trará benefícios significativos em termos de eficiência, produtividade e tomada de decisões baseada em dados.