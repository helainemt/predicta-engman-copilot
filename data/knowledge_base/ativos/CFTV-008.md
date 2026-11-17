# Cadastro de Ativo — CFTV-008

## 1. Identificação do ativo

- **TAG:** CFTV-008
- **Tipo de ativo:** Câmera de monitoramento rodoviário (CFTV)
- **Criticidade:** Alta — conforme o cenário definido no Eval Set.
- **Localização:** Trecho rodoviário concedido — localização fictícia não especificada.
- **Condição do cadastro:** Persona sintética elaborada para fins acadêmicos e testes do PREDICTA.
- **Vínculo com o Eval Set:** EVAL-013.

## 2. Caracterização técnica

### 2.1. Especificações técnicas adotadas para a persona

| Característica | Especificação adotada | Origem |
|---|---|---|
| Tipo de equipamento | Câmera IP de monitoramento rodoviário | Simulada |
| Fabricante | VisionTech — fabricante fictício | Simulada |
| Modelo | VT-Road PTZ 30X — modelo fictício | Simulada |
| Resolução | Full HD (1920 × 1080) | Referência técnica pública |
| Zoom óptico | 30x | Simulada |
| Movimento | PTZ (pan, tilt e zoom) | Simulada |
| Protocolo de comunicação | ONVIF | Simulada |
| Protocolo de transmissão | RTSP | Simulada |
| Alimentação elétrica | PoE+ | Simulada |
| Proteção do equipamento | IP66 | Simulada |
| Instalação | Ambiente externo, em estrutura de monitoramento rodoviário | Simulada |
| Ano de instalação | 2022 | Simulada |
| Recurso de detecção | Detecção Automática de Incidentes (DAI) | Referência técnica pública |

### 2.2. Componentes e funções relevantes

Para a construção da persona, são considerados os seguintes componentes:

- **Sensor de imagem:** responsável pela captura das imagens da rodovia.
- **Lente com zoom óptico:** permite ajustar o enquadramento e ampliar áreas de interesse.
- **Módulo de processamento:** realiza o tratamento e a codificação do vídeo.
- **Interface de comunicação:** permite transmitir o fluxo de vídeo ao sistema de monitoramento.
- **Alimentação elétrica:** fornece energia ao equipamento.
- **Mecanismo PTZ:** permite movimentação horizontal, vertical e aproximação óptica.
- **Interface de rede:** possibilita a comunicação entre a câmera e os equipamentos responsáveis pela transmissão e visualização das imagens.

## 3. Contexto operacional

O CFTV-008 representa uma câmera instalada em um trecho rodoviário concedido, utilizada para transmitir imagens ao Centro de Controle Operacional (CCO).

O equipamento possui criticidade alta, pois sua disponibilidade é considerada relevante para a continuidade do monitoramento rodoviário e para o acompanhamento das condições de tráfego.

A perda de transmissão compromete a visualização das imagens e reduz a capacidade de acompanhamento do trecho pelo CCO. Quando a indisponibilidade se prolonga, a equipe operacional pode ficar temporariamente sem acesso às imagens fornecidas pelo equipamento.

No cenário definido pelo EVAL-013, o CFTV-008 encontra-se sem transmissão há quatro horas. Além disso, existem duas ocorrências anteriores de perda de transmissão registradas em seu histórico.

A repetição desse tipo de falha, associada à indisponibilidade atual, exige atenção da equipe de manutenção. A análise deverá considerar a criticidade do ativo, a duração da indisponibilidade, o histórico de ocorrências e os critérios de prioridade estabelecidos no plano de manutenção.

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

O funcionamento do CFTV-008 depende da comunicação entre a câmera, os equipamentos de rede intermediários e o sistema responsável pela recepção e visualização das imagens.

Para a simulação, considera-se a seguinte estrutura:

1. Captura da imagem pela câmera;
2. Processamento e codificação do vídeo;
3. Transmissão do fluxo pela infraestrutura de comunicação;
4. Recepção do fluxo pelo sistema de monitoramento;
5. Decodificação e apresentação da imagem ao operador do CCO.

Uma falha em qualquer uma dessas etapas pode comprometer a transmissão e provocar a indisponibilidade das imagens.

## 4. Histórico de falhas

Conforme o cenário definido no EVAL-013:

- O ativo CFTV-008 possui criticidade alta.
- Foram registradas duas ocorrências anteriores de perda de transmissão.
- No momento representado pelo cenário de avaliação, o equipamento está sem transmissão há quatro horas.
- O plano de manutenção estabelece prioridade elevada para esse tipo de situação.
- O cenário não apresenta uma causa raiz confirmada para a indisponibilidade atual.

**Interpretação para o PREDICTA:**

A existência de duas ocorrências anteriores de perda de transmissão indica reincidência desse tipo de falha no ativo.

A indisponibilidade atual, com duração de quatro horas, representa uma condição que exige atenção, especialmente considerando a criticidade alta do equipamento.

A combinação entre criticidade, reincidência e duração da indisponibilidade deve ser considerada na análise de prioridade da manutenção. O plano de manutenção estabelece prioridade elevada para o cenário.

Entretanto, a repetição das ocorrências não permite concluir antecipadamente qual é a causa da falha. A investigação deverá considerar possíveis problemas no equipamento, na alimentação elétrica, na infraestrutura de comunicação e no sistema de recepção das imagens.

O assistente deverá utilizar os dados do histórico e os registros disponíveis para fundamentar sua análise, sem inventar causas, intervenções ou resultados de testes.

### 4.1. Complementação do histórico

Para permitir a simulação de consultas ao histórico de falhas, foram adotadas datas e durações fictícias para as duas ocorrências anteriores. Esses dados não são informados pelo EVAL-013.

| Ocorrência | Data | Sintoma | Duração | Causa |
|---|---|---|---|---|
| 1 | 18/03/2026 — data simulada | Perda de transmissão de vídeo | 45 minutos — duração simulada | Não confirmada |
| 2 | 22/08/2026 — data simulada | Perda de transmissão de vídeo | 1 hora — duração simulada | Não confirmada |

**Condição atual do cenário de avaliação:**

| Evento | Condição | Duração | Origem |
|---|---|---|---|
| Indisponibilidade atual | Câmera sem transmissão | 4 horas | EVAL-013 |

As datas e durações das duas ocorrências anteriores são complementações fictícias da persona. A indisponibilidade atual de quatro horas é uma informação expressamente definida no Eval Set e não deve ser confundida com as ocorrências anteriores.

### 4.2. Análise da reincidência das ocorrências

As duas ocorrências anteriores foram caracterizadas como perdas de transmissão. Para complementar a persona, foram adotados os seguintes horários fictícios:

| Ocorrência | Horário | Intervalo em relação à ocorrência anterior |
|---|---|---|
| 1 | 09h15 | — |
| 2 | 14h40 | Não aplicável |

Os horários foram definidos exclusivamente para permitir testes de consulta e organização do histórico. O EVAL-013 não informa os horários originais das ocorrências.

A existência de duas ocorrências anteriores permite identificar reincidência do sintoma, mas não comprova que os eventos tenham a mesma causa técnica.

### 4.3. Hipóteses técnicas para investigação

Considerando que o sintoma informado é a perda de transmissão, as seguintes possibilidades poderão ser avaliadas:

| Hipótese | Possível relação com o sintoma | Evidência necessária |
|---|---|---|
| Instabilidade na conexão de rede | Pode interromper a comunicação entre a câmera e o sistema de monitoramento | Verificação da conectividade e dos registros de comunicação |
| Perda de pacotes | Pode comprometer a transmissão contínua do fluxo de vídeo | Consulta aos registros de rede e indicadores de perda de pacotes |
| Falha de alimentação elétrica | Pode provocar desligamento ou reinicialização do equipamento | Verificação da alimentação e dos registros de energia |
| Falha no processamento da câmera | Pode impedir a geração ou transmissão adequada do fluxo de vídeo | Análise dos registros de funcionamento e desempenho do equipamento |
| Problema no cabeamento ou nas conexões | Pode interromper a comunicação entre a câmera e a infraestrutura de rede | Inspeção técnica das conexões e do cabeamento |
| Falha no equipamento de rede intermediário | Pode comprometer a comunicação entre a câmera e o sistema de monitoramento | Verificação dos switches, roteadores e demais equipamentos envolvidos |
| Falha no sistema de recepção ou visualização | Pode impedir a apresentação das imagens mesmo quando a câmera permanece ativa | Consulta aos registros do servidor e do sistema de monitoramento |

As hipóteses apresentadas são possibilidades técnicas para orientar a investigação. Nenhuma delas representa uma causa confirmada das ocorrências do CFTV-008.

### 4.4. Indicadores técnicos que podem auxiliar no diagnóstico

Para aprofundar a investigação das ocorrências, a persona considera os seguintes indicadores:

| Indicador | Finalidade | Possível interpretação |
|---|---|---|
| Disponibilidade da câmera | Verificar se o equipamento permanece acessível | Indisponibilidade pode indicar falha no equipamento ou na comunicação |
| Perda de pacotes | Avaliar a integridade da transmissão dos dados | Valores elevados podem comprometer o fluxo de vídeo |
| Latência | Medir o atraso na comunicação entre os pontos do sistema | Latência elevada pode prejudicar a transmissão e a visualização |
| Largura de banda utilizada | Avaliar o consumo de recursos da infraestrutura de rede | Consumo próximo do limite pode prejudicar a transmissão |
| Estado da alimentação elétrica | Verificar a continuidade do fornecimento de energia | Interrupções podem provocar desligamentos ou reinicializações |
| Alarmes de comunicação | Identificar interrupções ou instabilidades registradas | Permitem investigar possíveis problemas na conectividade |
| Registros de reinicialização | Identificar desligamentos ou reinicializações do equipamento | Podem indicar instabilidade elétrica ou falhas no equipamento |
| Uso de CPU e memória | Avaliar a carga de processamento do equipamento ou servidor | Sobrecarga pode prejudicar o processamento e a transmissão do vídeo |

## 5. Condições de manutenção

- **Criticidade operacional:** Alta — conforme o EVAL-013.
- **Histórico de falhas:** Duas ocorrências anteriores de perda de transmissão.
- **Condição atual:** Equipamento sem transmissão há quatro horas, conforme o cenário de avaliação.
- **Plano de manutenção:** Plano preventivo proposto para a persona, com atividades simuladas.
- **Procedimento técnico:** Procedimento de diagnóstico proposto para investigação de perda de transmissão e problemas de comunicação.
- **Necessidade de avaliação:** Investigar a indisponibilidade atual, consultar o histórico, verificar a comunicação de rede, a alimentação elétrica e o funcionamento do equipamento antes de recomendar uma intervenção.
- **Prioridade de atendimento:** Elevada, conforme o critério estabelecido no plano de manutenção do cenário.

### 5.1. Plano de manutenção simulado

| Atividade | Periodicidade proposta | Classificação |
|---|---|---|
| Inspeção visual do equipamento e da estrutura | Mensal | Simulada |
| Verificação dos registros de funcionamento e alarmes | Mensal | Simulada |
| Verificação da disponibilidade da câmera no sistema de monitoramento | Mensal | Simulada |
| Verificação da estabilidade da transmissão de vídeo | Mensal | Simulada |
| Inspeção das conexões e alimentação elétrica | Trimestral | Simulada |
| Verificação da conexão de rede e do cabeamento | Trimestral | Simulada |
| Avaliação dos parâmetros de transmissão do fluxo de vídeo | Trimestral | Simulada |
| Avaliação geral das condições de instalação e funcionamento | Semestral | Simulada |

### 5.2. Procedimento técnico simulado

1. Confirmar a TAG do equipamento e verificar a condição de indisponibilidade informada.
2. Consultar o histórico de falhas para identificar as duas ocorrências anteriores de perda de transmissão.
3. Verificar a duração da indisponibilidade atual e os registros disponíveis no sistema.
4. Consultar os alarmes registrados no período da ocorrência.
5. Verificar a disponibilidade da câmera e o estado da comunicação com o sistema de monitoramento.
6. Investigar possíveis registros de perda de pacotes ou instabilidade na conexão de rede.
7. Verificar os registros de alimentação elétrica e possíveis reinicializações do equipamento.
8. Avaliar o funcionamento dos equipamentos de rede intermediários, quando houver dados disponíveis.
9. Verificar se a indisponibilidade afeta somente o CFTV-008 ou outros equipamentos do mesmo trecho.
10. Consultar o procedimento técnico documentado aplicável ao diagnóstico da falha.
11. Comparar a ocorrência atual com as duas ocorrências anteriores, considerando a reincidência do sintoma.
12. Registrar os resultados da investigação.
13. Encaminhar para avaliação técnica especializada quando a causa não puder ser identificada remotamente.

### 5.3. Critérios para encaminhamento à manutenção

O encaminhamento para avaliação técnica deverá considerar:

- Criticidade alta do ativo;
- Indisponibilidade atual de quatro horas;
- Existência de duas ocorrências anteriores de perda de transmissão;
- Reincidência do sintoma;
- Duração e impacto da indisponibilidade;
- Existência de alarmes simultâneos;
- Evidências de falha no equipamento, na alimentação elétrica ou na infraestrutura de comunicação;
- Critérios de prioridade estabelecidos no plano de manutenção.

A prioridade elevada deverá ser considerada conforme o plano de manutenção definido para o cenário, sem que o assistente invente prazos de atendimento ou disponibilidade de equipes.

## 6. Aplicação no PREDICTA

1. Reconhecer a identificação e a criticidade alta cadastrada do equipamento.
2. Identificar corretamente as duas ocorrências anteriores de perda de transmissão.
3. Diferenciar as ocorrências anteriores da indisponibilidade atual de quatro horas.
4. Reconhecer a reincidência do sintoma.
5. Considerar a duração da indisponibilidade atual na análise.
6. Reconhecer que o plano de manutenção estabelece prioridade elevada para o cenário.
7. Consultar o histórico de falhas antes de apresentar uma recomendação.
8. Investigar possíveis problemas de rede, alimentação elétrica e funcionamento do equipamento.
9. Diferenciar informações registradas de hipóteses técnicas.
10. Evitar apresentar uma causa raiz como confirmada sem evidências.
11. Identificar quais indicadores técnicos poderiam auxiliar na investigação.
12. Reconhecer quando os registros disponíveis são insuficientes para concluir um diagnóstico.
13. Considerar a criticidade e a reincidência na análise de prioridade.
14. Utilizar informações técnicas do cadastro sem confundir dados simulados com dados oficiais.
15. Apresentar recomendações fundamentadas nos registros disponíveis.
16. Respeitar a necessidade de autorização humana para qualquer ação operacional.

### 6.1. Consultas e ferramentas que podem ser utilizadas

| Ferramenta do PREDICTA | Aplicação no CFTV-008 |
|---|---|
| `consultar_ativo` | Recuperar identificação, criticidade alta e características cadastradas |
| `consultar_historico_falhas` | Consultar as duas ocorrências anteriores de perda de transmissão e identificar padrões de reincidência |
| `consultar_condicoes_ambientais` | Verificar se existem condições ambientais relevantes no período das ocorrências, sem presumir relação causal |
| `consultar_procedimento` | Recuperar procedimentos documentados para diagnóstico de perda de transmissão e falhas de comunicação |
| `calcular_metricas_confiabilidade` | Calcular indicadores de confiabilidade quando houver dados suficientes e consistentes |

A ferramenta `listar_ativos_por_criticidade` também poderá ser utilizada em análises comparativas para apoiar a priorização da manutenção. A ferramenta `abrir_ordem_servico` poderá ser utilizada para criar uma OS simulada, exclusivamente após autorização humana explícita e recente do profissional responsável.

### 6.2. Comportamento esperado do assistente

Ao analisar uma consulta sobre o CFTV-008, o PREDICTA deverá:

- Apresentar a criticidade alta do equipamento;
- Identificar as duas ocorrências anteriores de perda de transmissão;
- Destacar a indisponibilidade atual de quatro horas;
- Diferenciar claramente o histórico anterior da condição atual;
- Reconhecer a reincidência do sintoma;
- Considerar a prioridade elevada estabelecida pelo plano de manutenção;
- Investigar possíveis problemas de comunicação, alimentação elétrica e funcionamento do equipamento;
- Solicitar informações adicionais quando necessário;
- Apresentar hipóteses como possibilidades, nunca como causas confirmadas sem evidências;
- Recomendar investigação técnica fundamentada;
- Não inventar resultados de testes, causas ou intervenções;
- Não abrir ordem de serviço sem a autorização humana exigida.

## 7. Referências técnicas e fundamentação

### 7.1. Dados provenientes do Eval Set

- TAG: CFTV-008.
- Criticidade alta.
- Duas ocorrências anteriores de perda de transmissão.
- Indisponibilidade atual de quatro horas.
- Plano de manutenção estabelece prioridade elevada.

**Origem:** EVAL-013.

### 7.2. Características técnicas fundamentadas em fonte pública

- Resolução Full HD.
- Zoom óptico.
- Recursos de Detecção Automática de Incidentes (DAI).
- Utilização de câmeras para monitoramento dos trechos rodoviários concedidos.

**Fonte oficial:**

Concessionária de Rodovias PRVias S.A. — Motiva Paraná. *Carta de Serviços Motiva Paraná*, seção 3.9 — Circuito fechado de televisão (CFTV), página 4 do PDF.

Link: https://rodovias.motiva.com.br/content/dam/conteudo-multicanal/rodovias/conteudo/pt/midia/prvias/carta-aos-usuarios/Carta%20de%20Servi%C3%A7os%20Motiva%20Paran%C3%A1%202.pdf

A documentação apresenta informações sobre o sistema de CFTV da concessionária, incluindo resolução Full HD, zoom óptico e recursos de Detecção Automática de Incidentes.

### 7.3. Fundamentação técnica complementar

**Fonte 1 — Axis Communications**

- **Instituição:** Axis Communications.
- **Documento:** *Troubleshooting guide for network connection*.
- **Assuntos relevantes:** infraestrutura de rede, largura de banda, perda de pacotes, cabeamento e sobrecarga de dispositivos.
- **Link:** https://help.axis.com/en-us/troubleshooting-network

A documentação aborda como a infraestrutura de comunicação pode afetar a transmissão de vídeo. Entre os fatores apresentados estão limitações de largura de banda, congestionamento de rede, interferências e sobrecarga de processamento.

**Aplicação na persona:** fundamenta a inclusão de instabilidade de rede, perda de pacotes e limitação de largura de banda como hipóteses técnicas para investigação da perda de transmissão.

**Fonte 2 — Axis Communications**

- **Instituição:** Axis Communications.
- **Documento:** *Troubleshooting guide for streaming issues*.
- **Assuntos relevantes:** latência, processamento do equipamento, transmissão, infraestrutura de rede e sistema de visualização.
- **Link:** https://help.axis.com/en-us/troubleshooting-streaming

A documentação explica que a transmissão e a visualização de vídeo dependem de diferentes etapas, incluindo o processamento no equipamento, a comunicação pela rede e a reprodução no sistema de visualização.

Também apresenta fatores como largura de banda, configuração do fluxo, taxa de quadros e capacidade de processamento.

**Aplicação na persona:** fundamenta a investigação de problemas de transmissão e indisponibilidade de imagens, evitando atribuir automaticamente a causa à câmera ou à rede.

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
- Zoom óptico de 30x;
- Movimento PTZ;
- Protocolos ONVIF e RTSP;
- Alimentação PoE+;
- Grau de proteção IP66;
- Ano de instalação;
- Localização genérica;
- Condições ambientais de instalação;
- Operação contínua durante 24 horas;
- Datas e horários individuais das duas ocorrências anteriores;
- Durações individuais das duas ocorrências anteriores;
- Detalhamento complementar dos sintomas;
- Periodicidades do plano de manutenção;
- Etapas do procedimento técnico de diagnóstico;
- Indicadores técnicos propostos para investigação;
- Hipóteses técnicas para investigação;
- Critérios complementares de encaminhamento para manutenção.
