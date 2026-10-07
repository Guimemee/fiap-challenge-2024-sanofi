# Modelagem Técnica e Justificativa de Engenharia

**Projeto:** Sanofi EC Pharma Challenge (USV & Despoluição)
**Empresa Parceira:** Sanofi EC Pharma Challenge
**Ano Letivo:** 2024 | **Turma:** 3ECR
**Fase:** Sprint 3

### Especificação do Desafio
Implementar e quantizar um modelo de rede neural convolucional de detecção de objetos (YOLOv8 Nano) para execução em tempo real na placa de inteligência de borda Nvidia Jetson Orin Nano acoplada à câmera estéreo frontal da embarcação. O modelo deve detectar e segmentar garrafas plásticas, sacolas, resíduos químicos e barreiras de contenção com taxa de quadros superior a 15 FPS.

### Formulação Matemática e Física
$$\text{mAP@50} = \frac{1}{N_{\text{classes}}} \sum_{c=1}^{N} \text{AP}_c, \quad \text{IoU} = \frac{\text{Área de Interseção}}{\text{Área de União}} \ge 0,50$$
