# Modelagem Técnica e Justificativa de Engenharia

**Projeto:** Sanofi EC Pharma Challenge (USV & Despoluição)
**Empresa Parceira:** Sanofi EC Pharma Challenge
**Ano Letivo:** 2024 | **Turma:** 3ECR
**Fase:** Sprint 2

### Especificação do Desafio
Dimensionar o sistema de propulsão elétrica baseado em dois propulsores subaquáticos (Thrusters BLDC) com empuxo nominal combinado de 14 kgf para vencer o arrasto hidrodinâmico à velocidade de cruzeiro de v = 1,8 m/s (3,5 nós). Dimensionar o teto de painéis solares semiflexíveis monocristalinos de 150 W instalados sobre a embarcação e o banco de baterias LiFePO4 de 24 V / 40 Ah.

### Formulação Matemática e Física
$$R_{\text{arrasto}} = \frac{1}{2} C_d \cdot \rho_{\text{água}} \cdot S_{\text{molhada}} \cdot v^2, \quad P_{\text{elétrica}} = \frac{R_{\text{arrasto}} \cdot v}{\eta_{\text{prop}}}$$
