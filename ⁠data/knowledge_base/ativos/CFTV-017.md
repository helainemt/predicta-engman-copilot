# Cadastro de Ativo — CFTV-017

## 1. Identificação do ativo

- **TAG:** CFTV-017
- **Tipo de ativo:** Câmera de monitoramento rodoviário (CFTV)
- **Criticidade:** Média — classificação simulada para a persona.
- **Localização:** Trecho rodoviário concedido — localização fictícia não especificada.
- **Condição do cadastro:** Persona sintética elaborada para fins acadêmicos e testes do PREDICTA.
- **Vínculo com o Eval Set:** EVAL-002.

## 2. Caracterização técnica

### 2.1. Especificações técnicas adotadas para a persona

| Característica | Especificação adotada | Origem |
|---|---|---|
| Tipo de equipamento | Câmera IP de monitoramento rodoviário | Simulada |
| Fabricante | VisionTech — fabricante fictício | Simulada |
| Modelo | VT-Road Compact 20X — modelo fictício | Simulada |
| Resolução | Full HD (1920 × 1080) | Referência técnica pública |
| Zoom óptico | 20x | Simulada |
| Movimento | PTZ (pan, tilt e zoom) | Simulada |
| Protocolo de comunicação | ONVIF | Simulada |
| Protocolo de transmissão | RTSP | Simulada |
| Alimentação elétrica | PoE+ | Simulada |
| Proteção do equipamento | IP66 | Simulada |
| Instalação | Ambiente externo, em estrutura de monitoramento rodoviário | Simulada |
| Ano de instalação | 2023 | Simulada |
| Recurso de detecção | Detecção Automática de Incidentes (DAI) | Referência técnica pública |

### 2.2. Componentes e funções relevantes

Para a construção da persona, são considerados os seguintes componentes:

- **Sensor de imagem:** responsável pela captura das imagens da rodovia.
- **Lente com zoom óptico:** permite ajustar o enquadramento e ampliar áreas de interesse.
- **Módulo de processamento:** realiza o tratamento e a codificação do vídeo.
- **Interface de comunicação:** permite transmitir o fluxo de vídeo ao sistema de monitoramento.
- **Alimentação elétrica:** fornece energia ao equipamento.
- **Mecanismo PTZ:** permite movimentação horizontal, vertical e aproximação óptica.

## 3. Contexto operacional

O CFTV-017 representa uma câmera instalada em um trecho rodoviário concedido, utilizada para transmitir imagens ao Centro de Controle Operacional (CCO).

Sua disponibilidade é relevante para a continuidade do monitoramento e para o acompanhamento das condições de tráfego. O congelamento intermitente de imagem prejudica a visualização contínua do trecho, podendo dificultar a identificação e o acompanhamento de ocorrências.

A repetição desse tipo de falha exige atenção da equipe de manutenção, principalmente quando associada a alarmes de interrupções temporárias de comunicação.

A existência desses alarmes torna importante investigar possíveis instabilidades na transmissão, mas não permite concluir antecipadamente que a comunicação seja a causa dos congelamentos.

### 3.1. Condições de instalação e operação

Para fins de simulação, considera-se que o equipamento:

- Está instalado em estrutura de monitoramento rodoviário;
- Opera continuamente, durante 24 horas por dia;
- Está exposto a chuva, poeira, umidade e variações de temperatura;
- Depende de alimentação elétrica e comunicação de dados para transmitir imagens ao CCO;
- Possui movimentação PTZ para permitir o ajuste do enquadramento e do zoom;
- Está integrado a um sistema de monitoramento que permite consultar as imagens em tempo real;
- Depende da estabilidade da rede e do fluxo de vídeo para manter a transmissão contínua.

### 3.2. Dependência da infraestrutura de comunicação

O funcionamento do CFTV-017 depende da comunicação entre a câmera, os equipamentos de rede intermediários e o sistema responsável pela recepção e visualização das imagens.

Para a simulação, considera-se a seguinte estrutura:

1. Captura da imagem pela câmera;
2. Processamento e codificação do vídeo;
3. Transmissão do fluxo pela infraestrutura de comunicação;
4. Recepção do fluxo pelo sistema de monitoramento;
5. Decodificação e apresentação da imagem ao operador do CCO.

Uma falha em qualquer uma dessas etapas pode comprometer a fluidez da imagem.

## 4. Histórico de falhas

Conforme o cenário definido no EVAL-002:

- A câmera CFTV-017 apresentou três ocorrências de congelamento intermitente de imagem nos últimos 12 meses.
- Duas dessas ocorrências foram registradas em horários próximos.
- Foram identificados alarmes relacionados a interrupções temporárias de comunicação.
- Existe procedimento de diagnóstico para investigação de problemas de comunicação.
- A causa raiz dos congelamentos não está confirmada.

**Interpretação para o PREDICTA:**

A repetição dos congelamentos indica reincidência de um comportamento anormal na transmissão ou visualização das imagens.

A proximidade temporal de duas ocorrências, associada à presença de alarmes de interrupções temporárias de comunicação, constitui um indício relevante para investigar possíveis instabilidades na rede ou no fluxo de vídeo.

Entretanto, esses alarmes não comprovam que a comunicação seja a causa dos congelamentos. A investigação deverá considerar também o funcionamento do equipamento, o processamento do vídeo e os demais componentes envolvidos na transmissão.

O assistente deverá utilizar os dados do histórico e os registros disponíveis para fundamentar sua análise, sem inventar causas ou apresentar hipóteses como diagnósticos confirmados.

### 4.1. Complementação do histórico

| Ocorrência | Data | Sintoma | Duração | Causa |
|---|---|---|---|---|
| 1 | 10/02/2026 — data simulada | Congelamento intermitente de imagem | 8 minutos — duração simulada | Não confirmada |
| 2 | 14/06/2026 — data simulada | Congelamento intermitente de imagem | 12 minutos — duração simulada | Não confirmada |
| 3 | 03/10/2026 — data simulada | Congelamento intermitente de imagem | 6 minutos — duração simulada | Não confirmada |

### 4.2. Análise da proximidade temporal das ocorrências

Para complementar o histórico sintético, foram adotados os seguintes horários:

| Ocorrência | Horário | Intervalo em relação à ocorrência anterior |
|---|---|---|
| 1 | 07h42 | — |
| 2 | 07h51 | 9 minutos |
| 3 | 19h20 | Não aplicável |

### 4.3. Hipóteses técnicas para investigação

Considerando que o sintoma informado é o congelamento intermitente da imagem, as seguintes possibilidades poderão ser avaliadas:

| Hipótese | Possível relação com o sintoma | Evidência necessária |
|---|---|---|
| Instabilidade na conexão de rede | Pode interromper temporariamente a transmissão do fluxo de vídeo | Verificação da conectividade e dos registros de comunicação |
| Perda de pacotes | Pode comprometer a continuidade da transmissão das imagens | Consulta aos registros de rede e indicadores de perda de pacotes |
| Limitação de largura de banda | Pode prejudicar a transmissão contínua do vídeo | Verificação da utilização da rede e da taxa de transmissão |
| Falha no processamento da câmera | Pode provocar interrupções ou congelamentos na geração do fluxo de vídeo | Análise dos registros de funcionamento e desempenho do equipamento |
| Problema no sistema de visualização | Pode provocar congelamentos mesmo quando a câmera continua transmitindo | Consulta aos registros do servidor e do sistema de visualização |
| Falha de alimentação elétrica | Pode provocar instabilidade ou reinicializações do equipamento | Verificação da alimentação e dos registros de energia |
| Sobrecarga do equipamento ou servidor | Pode comprometer o processamento, a transmissão ou a reprodução das imagens | Consulta aos indicadores de processamento, memória e utilização de recursos |

### 4.4. Indicadores técnicos que podem auxiliar no diagnóstico

Para aprofundar a investigação das ocorrências, a persona considera os seguintes indicadores:

| Indicador | Finalidade | Possível interpretação |
|---|---|---|
| Disponibilidade da câmera | Verificar se o equipamento permanece acessível | Indisponibilidade pode indicar falha no equipamento ou na comunicação |
| Perda de pacotes | Avaliar a integridade da transmissão dos dados | Valores elevados podem comprometer o fluxo de vídeo |
| Latência | Medir o atraso na comunicação entre os pontos do sistema | Latência elevada pode provocar atraso na visualização |
| Largura de banda utilizada | Avaliar o consumo de recursos da infraestrutura de rede | Consumo próximo do limite pode prejudicar a transmissão |
| Taxa de quadros (FPS) | Verificar a quantidade de imagens transmitidas por segundo | Redução pode comprometer a fluidez do vídeo |
| Alarmes de comunicação | Identificar interrupções ou instabilidades registradas | Permitem comparar eventos de comunicação com os horários dos congelamentos |
| Uso de CPU e memória | Avaliar a carga de processamento do equipamento ou servidor | Sobrecarga pode prejudicar o processamento e a reprodução do vídeo |

## 5. Condições de manutenção

- **Criticidade operacional:** Média — classificação simulada para a persona.
- **Histórico de falhas:** Três ocorrências de congelamento intermitente de imagem nos últimos 12 meses.
- **Condição identificada:** Duas ocorrências em horários próximos e presença de alarmes de interrupções temporárias de comunicação.
- **Plano de manutenção:** Plano preventivo proposto para a persona, com atividades simuladas.
- **Procedimento técnico:** Procedimento de diagnóstico proposto para investigação de congelamentos de imagem e problemas de comunicação.
- **Necessidade de avaliação:** Investigar as ocorrências, consultar o histórico, verificar a comunicação de rede e o funcionamento do equipamento antes de recomendar uma intervenção.
- **Prioridade de atendimento:** A definir conforme os critérios do plano de manutenção e a avaliação das condições operacionais.

### 5.1. Plano de manutenção simulado

| Atividade | Periodicidade proposta | Classificação |
|---|---|---|
| Inspeção visual do equipamento e da estrutura | Mensal | Simulada |
| Verificação dos registros de funcionamento e alarmes | Mensal | Simulada |
| Verificação da estabilidade da transmissão de vídeo | Mensal | Simulada |
| Verificação da disponibilidade da câmera no sistema de monitoramento | Mensal | Simulada |
| Inspeção das conexões e alimentação elétrica | Trimestral | Simulada |
| Verificação da conexão de rede e do cabeamento | Trimestral | Simulada |
| Avaliação dos parâmetros de transmissão do fluxo de vídeo | Trimestral | Simulada |
| Avaliação geral das condições de instalação e funcionamento | Semestral | Simulada |

### 5.2. Procedimento técnico simulado

1. Confirmar a TAG do equipamento e identificar o período em que ocorreu o congelamento.
2. Consultar o histórico de falhas para identificar as três ocorrências registradas.
3. Verificar os alarmes registrados nos períodos dos congelamentos.
4. Consultar o estado da comunicação entre a câmera e o sistema de monitoramento.
5. Verificar a disponibilidade e a estabilidade da conexão de rede.
6. Investigar possíveis registros de perda de pacotes ou limitação de largura de banda.
7. Consultar os registros de funcionamento e possíveis reinicializações do equipamento.
8. Verificar se o problema afeta somente o CFTV-017 ou outros equipamentos do mesmo trecho.
9. Comparar os resultados com as ocorrências anteriores, considerando a proximidade temporal de duas delas.
10. Verificar indicadores de latência, taxa de quadros e utilização de recursos, quando disponíveis.
11. Registrar os resultados da investigação.
12. Encaminhar para avaliação técnica especializada quando a causa não puder ser identificada remotamente.

### 5.3. Critérios para encaminhamento à manutenção

O encaminhamento para avaliação técnica deverá considerar:

- Repetição dos congelamentos de imagem;
- Recorrência de alarmes de comunicação;
- Proximidade temporal entre as ocorrências;
- Duração e impacto das interrupções;
- Existência de outros alarmes simultâneos;
- Evidências de falha no equipamento ou na infraestrutura de comunicação;
- Persistência do problema após as verificações iniciais.

## 6. Aplicação no PREDICTA

1. Reconhecer a identificação e a criticidade cadastrada do equipamento.
2. Identificar corretamente as três ocorrências de congelamento intermitente de imagem nos últimos 12 meses.
3. Reconhecer que duas ocorrências aconteceram em horários próximos.
4. Identificar a existência de alarmes relacionados a interrupções temporárias de comunicação.
5. Consultar o histórico de falhas antes de apresentar uma recomendação.
6. Relacionar temporalmente os congelamentos e os alarmes sem afirmar que existe uma causa comprovada.
7. Considerar a disponibilidade de procedimento de diagnóstico para problemas de comunicação.
8. Investigar possíveis problemas de rede, transmissão e funcionamento do equipamento.
9. Diferenciar informações registradas de hipóteses técnicas.
10. Evitar apresentar uma causa raiz como confirmada sem evidências.
11. Identificar quais indicadores técnicos poderiam auxiliar na investigação.
12. Reconhecer quando os registros disponíveis são insuficientes para concluir um diagnóstico.
13. Utilizar informações técnicas do cadastro sem confundir dados simulados com dados oficiais.
14. Apresentar recomendações fundamentadas nos registros disponíveis.
15. Respeitar a necessidade de autorização humana para qualquer ação operacional.

### 6.1. Consultas e ferramentas que podem ser utilizadas

| Ferramenta do PREDICTA | Aplicação no CFTV-017 |
|---|---|
| `consultar_ativo` | Recuperar identificação, criticidade e características cadastradas |
| `consultar_historico_falhas` | Consultar as três ocorrências e identificar padrões de reincidência |
| `consultar_condicoes_ambientais` | Verificar se existem condições ambientais relevantes no período das ocorrências, sem presumir relação causal |
| `consultar_procedimento` | Recuperar o procedimento de diagnóstico de comunicação |
| `calcular_metricas_confiabilidade` | Calcular indicadores quando houver dados suficientes e consistentes |

### 6.2. Comportamento esperado do assistente

Ao analisar uma consulta sobre o CFTV-017, o PREDICTA deverá:

- Apresentar o histórico de congelamentos de imagem;
- Destacar a proximidade temporal das duas ocorrências;
- Informar a existência de alarmes de interrupções temporárias de comunicação;
- Explicar por que a comunicação deve ser investigada;
- Considerar outras possibilidades técnicas além da rede;
- Solicitar informações adicionais quando necessário;
- Apresentar hipóteses como possibilidades, nunca como causas confirmadas sem evidências;
- Recomendar investigação técnica fundamentada;
- Não abrir ordem de serviço sem a autorização humana exigida.

## 7. Referências técnicas e fundamentação

### 7.1. Dados provenientes do Eval Set

- TAG: CFTV-017.
- Três ocorrências de congelamento intermitente de imagem nos últimos 12 meses.
- Duas ocorrências registradas em horários próximos.
- Presença de alarmes relacionados a interrupções temporárias de comunicação.
- Disponibilidade de procedimento de diagnóstico para problemas de comunicação.
- Causa raiz não confirmada.

**Origem:** EVAL-002.

### 7.2. Características técnicas fundamentadas em fonte pública

- Resolução Full HD.
- Zoom óptico.
- Recursos de Detecção Automática de Incidentes (DAI).
- Utilização de câmeras para monitoramento dos trechos rodoviários concedidos.

**Fonte oficial:**

Concessionária de Rodovias PRVias S.A. — Motiva Paraná. *Carta de Serviços Motiva Paraná*, seção 3.9 — Circuito fechado de televisão (CFTV), página 4 do PDF.

Link: https://rodovias.motiva.com.br/content/dam/conteudo-multicanal/rodovias/conteudo/pt/midia/prvias/carta-aos-usuarios/Carta%20de%20Servi%C3%A7os%20Motiva%20Paran%C3%A1%202.pdf

A documentação apresenta informações sobre o sistema de CFTV da concessionária, incluindo resolução Full HD, zoom óptico e recursos de Detecção Automática de Incidentes.

Essas características são utilizadas como referência tecnológica pública para a construção da persona. O documento não confirma o fabricante, modelo ou demais especificações simuladas deste cadastro.

### 7.3. Fundamentação técnica complementar

**Fonte 1 — Axis Communications**

- **Instituição:** Axis Communications.
- **Documento:** *Troubleshooting guide for streaming issues*.
- **Assuntos relevantes:** latência, fluidez do vídeo, transmissão, processamento do equipamento, infraestrutura de rede e sistema de visualização.
- **Link:** https://help.axis.com/en-us/troubleshooting-streaming

A documentação explica que a fluidez do vídeo depende de diferentes etapas, incluindo o processamento no equipamento, a transmissão pela rede e a reprodução no cliente de visualização.

Também apresenta fatores como largura de banda, configuração do fluxo, taxa de quadros, capacidade de processamento e desempenho do sistema de visualização.

**Aplicação na persona:** fundamenta a investigação de problemas de transmissão e congelamento de imagem, evitando atribuir automaticamente a causa à câmera ou à rede.

**Fonte 2 — Axis Communications**

- **Instituição:** Axis Communications.
- **Documento:** *Troubleshooting guide for network connection*.
- **Assuntos relevantes:** infraestrutura de rede, largura de banda, perda de pacotes, interferência em cabeamento e sobrecarga de dispositivos.
- **Link:** https://help.axis.com/en-us/troubleshooting-network

A documentação aborda como a infraestrutura de comunicação pode afetar a transmissão de vídeo. Entre os fatores apresentados estão limitações de largura de banda, congestionamento de rede, interferências e sobrecarga de processamento.

**Aplicação na persona:** fundamenta a inclusão de instabilidade de rede, perda de pacotes e limitação de largura de banda como hipóteses técnicas para investigação.

**Fonte 3 — Microsoft Learn**

- **Instituição:** Microsoft.
- **Documento:** *Network Cameras*.
- **Assunto:** funcionamento e integração de câmeras de rede.
- **Link:** https://learn.microsoft.com/en-us/windows-hardware/drivers/stream/network-cameras

A documentação apresenta aspectos técnicos relacionados a câmeras de rede e à transmissão de fluxos de vídeo.

**Aplicação na persona:** referência complementar para contextualizar a utilização de câmeras IP e os mecanismos envolvidos na transmissão de vídeo.

### 7.4. Dados fictícios e premissas da persona

Foram criados para completar o cadastro e permitir simulações mais realistas:

- Fabricante e modelo do equipamento;
- Zoom óptico de 20x;
- Movimento PTZ;
- Protocolos ONVIF e RTSP;
- Alimentação PoE+;
- Grau de proteção IP66;
- Ano de instalação;
- Localização genérica;
- Condições ambientais de instalação;
- Operação contínua durante 24 horas;
- Datas, horários e durações individuais das três ocorrências;
- Detalhamento complementar dos sintomas;
- Criticidade média adotada para a persona;
- Periodicidades do plano de manutenção;
- Etapas do procedimento técnico de diagnóstico;
- Indicadores técnicos propostos para investigação;
- Hipóteses técnicas para investigação;
- Critérios de encaminhamento para manutenção.
