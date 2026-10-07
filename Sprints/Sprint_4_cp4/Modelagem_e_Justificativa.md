# Modelagem Técnica e Justificativa de Engenharia

**Projeto:** Sanofi EC Pharma Challenge (USV & Despoluição)
**Empresa Parceira:** Sanofi EC Pharma Challenge
**Ano Letivo:** 2024 | **Turma:** 3ECR
**Fase:** Sprint 4

### Especificação do Desafio
Projetar o sistema de navegação e guiamento autônomo baseado no piloto automático ArduPilot/PX4 com receptor GNSS RTK de dupla frequência entregando precisão centimétrica. Implementar o planejamento de curvas de Dubins com raio de giro mínimo R_min = 2,5 m para cobertura completa de área hídrica (Lawnmower Pattern) com transmissão contínua de telemetria via 4G/LTE para dashboard corporativo da Sanofi.

### Formulação Matemática e Física
$$x_{k+1} = x_k + v \cdot \Delta t \cos\theta_k, \quad y_{k+1} = y_k + v \cdot \Delta t \sin\theta_k, \quad \theta_{k+1} = \theta_k + \frac{v}{L}\tan\delta_k \cdot \Delta t$$
