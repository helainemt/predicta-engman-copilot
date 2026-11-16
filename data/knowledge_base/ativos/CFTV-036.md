# Cadastro de Ativo — CFTV-036

## 1. Identificação do ativo

- **TAG:** CFTV-036
- **Tipo de ativo:** Câmera de monitoramento rodoviário (CFTV)
- **Criticidade:** Média — classificação simulada para a persona.
- **Localização:** Trecho rodoviário sujeito à formação de neblina — localização fictícia não especificada.
- **Condição do cadastro:** Persona sintética elaborada para fins acadêmicos e testes do PREDICTA.
- **Vínculo com o Eval Set:** EVAL-004.

## 2. Caracterização técnica

### 2.1. Especificações técnicas adotadas para a persona

| Característica | Especificação adotada | Origem |
|---|---|---|
| Tipo de equipamento | Câmera IP de monitoramento rodoviário | Simulada |
| Fabricante | VisionTech — fabricante fictício | Simulada |
| Modelo | VT-Road Weather 25X — modelo fictício | Simulada |
| Resolução | Full HD (1920 × 1080) | Referência técnica pública |
| Zoom óptico | 25x | Simulada |
| Movimento | PTZ (pan, tilt e zoom) | Simulada |
| Protocolo de comunicação | ONVIF | Simulada |
| Protocolo de transmissão de vídeo | RTSP | Simulada |
| Alimentação elétrica | PoE+ | Simulada |
| Proteção do equipamento | IP66 | Simulada |
| Instalação | Ambiente externo, em estrutura elevada | Simulada |
| Ano de instalação | 2023 | Simulada |
| Recurso de detecção | Detecção Automática de Incidentes (DAI) | Referência técnica pública |
| Recurso de compensação ambiental | Função de compensação de neblina (Defog) | Simulada |

### 2.2. Componentes e funções relevantes

Para a construção da persona, são considerados os seguintes componentes:

- **Sensor de imagem:** responsável pela captura das imagens da rodovia.
- **Lente com zoom óptico:** permite ajustar o enquadramento e ampliar áreas de interesse.
- **Módulo de processamento:** realiza o tratamento e a codificação do vídeo.
- **Interface de comunicação:** permite transmitir o fluxo de vídeo ao sistema de monitoramento.
- **Alimentação elétrica:** fornece energia ao equipamento.
- **Mecanismo PTZ:** permite movimentação horizontal, vertical e aproximação óptica.
- **Recurso Defog:** considerado uma característica simulada do modelo adotado, destinado a compensar determinados efeitos visuais associados à neblina.

## 3. Contexto operacional

O CFTV-036 representa uma câmera instalada em um trecho rodoviário sujeito à formação de neblina, principalmente durante a madrugada.

Sua função é transmitir imagens ao Centro de Controle Operacional (CCO), permitindo o acompanhamento das condições de tráfego e auxiliando na identificação de ocorrências.

O principal desafio operacional desse ativo está relacionado à redução da visibilidade provocada pelas condições meteorológicas.

Conforme o cenário definido no EVAL-004, a câmera apresenta baixa visibilidade nas imagens durante um período de neblina intensa e umidade elevada. Entretanto, não existem evidências confirmadas de defeito físico no equipamento.

Nessas condições, a degradação da imagem deve ser analisada considerando o contexto ambiental. A perda de nitidez não representa necessariamente um defeito da câmera ou a necessidade imediata de manutenção corretiva.

A investigação deverá considerar os registros ambientais associados ao horário da ocorrência e verificar se a qualidade da imagem melhora após a normalização das condições meteorológicas.

### 3.1. Condições de instalação e operação

Para fins de simulação, considera-se que o equipamento:

- Está instalado em estrutura elevada de monitoramento rodoviário;
- Opera continuamente, durante 24 horas por dia;
- Está instalado em trecho com maior ocorrência de neblina durante a madrugada;
- Está exposto a chuva, poeira, umidade e variações de temperatura;
- Depende de alimentação elétrica e comunicação de dados para transmitir imagens ao CCO;
- Está integrado a um sistema de monitoramento que permite consultar as imagens em tempo real;
- Possui função de compensação de neblina, considerada uma característica simulada do modelo adotado.

### 3.2. Condições ambientais de referência

| Variável ambiental | Condição considerada | Origem |
|---|---|---|
| Horário de ocorrência | 04h30 | Simulada |
| Temperatura ambiente | 16 °C | Simulada |
| Umidade relativa do ar | 97% | Simulada |
| Condição meteorológica | Neblina intensa | Proveniente do Eval Set |
| Visibilidade | Reduzida | Proveniente do Eval Set |
| Precipitação | Sem registro de chuva no cenário | Simulada |
| Comunicação da câmera | Sem falha identificada | Proveniente do Eval Set |

## 4. Histórico de falhas

Conforme o cenário definido no EVAL-004:

- Foi identificada baixa visibilidade nas imagens durante a madrugada.
- O cenário apresenta neblina intensa e umidade elevada.
- Não há evidência confirmada de defeito físico no equipamento.
- Não foram identificadas falhas de comunicação.
- O cenário não apresenta reincidência de falha física de imagem.
- Existe procedimento de inspeção disponível.

**Interpretação para o PREDICTA:**

A degradação visual observada deve ser analisada considerando as condições ambientais existentes no momento da ocorrência.

A presença de neblina intensa e umidade elevada constitui um contexto relevante para investigar a redução da visibilidade, mas não permite afirmar, isoladamente, que essas condições sejam a causa definitiva do problema.

A ausência de falhas de comunicação e de evidências confirmadas de defeito físico reforça a necessidade de uma investigação contextual antes de recomendar uma intervenção corretiva.

O PREDICTA deverá consultar os registros ambientais, correlacioná-los com o horário da ocorrência e verificar se a degradação da imagem persiste após a normalização das condições meteorológicas.

O assistente não deverá recomendar substituição ou manutenção corretiva do equipamento sem evidências suficientes de defeito físico.

### 4.1. Complementação do histórico

Para permitir a simulação de consultas ambientais e a comparação entre ocorrências, foram adotados dois registros complementares fictícios.

| Ocorrência | Data e horário simulados | Sintoma | Condições ambientais | Comunicação | Resultado da avaliação |
|---|---|---|---|---|---|
| 1 | 16/07/2026 — 04h30 | Redução da nitidez e do alcance visual | Neblina intensa e umidade relativa de 97% | Normal | Sem evidência de defeito físico |
| 2 | 28/07/2026 — 05h10 | Redução da visibilidade da imagem | Neblina e umidade relativa de 95% | Normal | Sem evidência de defeito físico |

### 4.2. Análise das condições ambientais

A presença de neblina intensa e umidade elevada é relevante para a investigação da degradação visual.

Para a análise do CFTV-036, deverão ser considerados:

- O horário em que a imagem apresentou baixa visibilidade;
- Os registros de umidade relativa do ar;
- A presença e a intensidade de neblina;
- Os registros de visibilidade disponíveis;
- A existência ou ausência de precipitação;
- A estabilidade da comunicação da câmera;
- A qualidade da imagem após a normalização das condições ambientais.

### 4.3. Hipóteses técnicas para investigação

Considerando o comportamento descrito, as seguintes possibilidades poderão ser avaliadas:

| Hipótese | Possível relação com o sintoma | Evidência necessária |
|---|---|---|
| Neblina intensa | Pode reduzir o contraste e o alcance visual da imagem | Dados meteorológicos e imagens capturadas no momento |
| Umidade elevada e condensação | Pode provocar formação de gotículas na superfície óptica e prejudicar a nitidez | Inspeção da lente ou proteção externa e registros de umidade |
| Gotas de água na proteção da câmera | Podem gerar reflexos e interferências na imagem | Inspeção visual da proteção e análise das imagens |
| Sujeira na lente ou proteção externa | Pode reduzir a nitidez e intensificar os efeitos de iluminação | Inspeção física e comparação das imagens antes e depois da limpeza |
| Defeito no sistema óptico | Pode provocar perda de foco ou degradação persistente da imagem | Testes de foco, inspeção técnica e verificação em condições ambientais normais |

### 4.4. Indicadores técnicos que podem auxiliar no diagnóstico

Para aprofundar a investigação das ocorrências, a persona considera os seguintes indicadores:

| Indicador | Finalidade | Possível interpretação |
|---|---|---|
| Umidade relativa do ar | Avaliar a presença de umidade elevada no período | Valores elevados podem compor um contexto favorável à formação de condensação |
| Visibilidade atmosférica | Avaliar as condições de visibilidade no trecho | Redução pode explicar parte da degradação visual |
| Temperatura ambiente | Complementar a análise das condições meteorológicas | Variações podem ser relevantes para investigar condensação |
| Precipitação | Verificar a ocorrência de chuva no período | Pode auxiliar na análise de gotas de água e interferências na imagem |
| Qualidade e nitidez da imagem | Avaliar a intensidade da degradação visual | Permite comparar imagens em diferentes condições ambientais |
| Disponibilidade da câmera | Verificar se o equipamento permanece acessível | Ajuda a diferenciar degradação visual de indisponibilidade |
| Estado da comunicação | Verificar a estabilidade da transmissão | Ausência de falhas de comunicação ajuda a delimitar a investigação |
| Funcionamento do foco e zoom | Avaliar o comportamento dos recursos ópticos | Alterações persistentes podem justificar inspeção técnica |

## 5. Condições de manutenção

- **Criticidade operacional:** Média — classificação simulada para a persona.
- **Histórico de falhas:** Cenário de baixa visibilidade durante neblina intensa e umidade elevada, sem evidência confirmada de defeito físico.
- **Condição identificada:** Degradação visual associada a um contexto de condições meteorológicas adversas, com comunicação normal.
- **Plano de manutenção:** Plano preventivo proposto para a persona, com atividades simuladas.
- **Procedimento técnico:** Procedimento de inspeção disponível no cenário de avaliação, complementado por etapas simuladas.
- **Necessidade de avaliação:** Consultar registros ambientais, correlacionar as condições meteorológicas com o horário da ocorrência e verificar se a degradação visual persiste após a normalização do ambiente.
- **Prioridade de atendimento:** A definir conforme a avaliação técnica, a persistência do problema e os critérios do plano de manutenção.

### 5.1. Plano de manutenção simulado

| Atividade | Periodicidade proposta | Classificação |
|---|---|---|
| Inspeção visual da câmera e estrutura | Mensal | Simulada |
| Verificação da qualidade e nitidez da imagem | Mensal | Simulada |
| Inspeção da lente e proteção externa | Mensal | Simulada |
| Verificação do funcionamento do foco e zoom | Trimestral | Simulada |
| Inspeção de conexões e alimentação elétrica | Trimestral | Simulada |
| Verificação do funcionamento da compensação de neblina | Trimestral | Simulada |
| Avaliação das condições de instalação e vedação | Semestral | Simulada |

### 5.2. Procedimento técnico simulado

1. Confirmar a TAG do equipamento e identificar o horário em que ocorreu a degradação da imagem.
2. Consultar os registros de condições ambientais associados ao período da ocorrência.
3. Verificar os níveis de umidade e os registros de visibilidade no trecho.
4. Identificar a presença de neblina, névoa ou outras condições meteorológicas relevantes.
5. Comparar a qualidade da imagem com registros obtidos em condições ambientais normais.
6. Verificar se a transmissão de vídeo permanece estável.
7. Consultar os registros de funcionamento do equipamento.
8. Inspecionar a lente e a proteção externa para identificar sujeira, gotas de água ou condensação, caso a análise indique essa necessidade.
9. Verificar o funcionamento do foco e do zoom.
10. Avaliar, quando disponível, a configuração do recurso de compensação de neblina.
11. Verificar se a degradação visual persiste após a normalização das condições ambientais.
12. Registrar as evidências e encaminhar para avaliação técnica especializada caso o problema permaneça.

### 5.3. Critérios para encaminhamento à manutenção

O encaminhamento para avaliação técnica deverá considerar:

- Persistência da baixa visibilidade após a normalização das condições ambientais;
- Existência de evidências de sujeira, condensação ou danos na lente e proteção externa;
- Alterações persistentes no foco ou no zoom;
- Existência de falhas de comunicação ou outros alarmes;
- Ausência de melhora da qualidade da imagem após a normalização meteorológica;
- Resultados da inspeção técnica;
- Evidências suficientes para diferenciar uma interferência ambiental de um possível defeito físico.

## 6. Aplicação no PREDICTA

1. Reconhecer a identificação do equipamento e a criticidade cadastrada.
2. Identificar a baixa visibilidade nas imagens durante a madrugada.
3. Considerar a presença de neblina intensa e umidade elevada na análise.
4. Consultar os registros ambientais associados ao horário da ocorrência.
5. Correlacionar os registros meteorológicos com o período de degradação da imagem.
6. Diferenciar interferência ambiental de falha física do equipamento.
7. Considerar a ausência de falhas de comunicação como evidência relevante.
8. Reconhecer que não existem evidências confirmadas de defeito físico.
9. Verificar se a degradação da imagem persiste após a normalização das condições ambientais.
10. Evitar recomendar substituição da câmera sem evidências de defeito físico.
11. Consultar o procedimento de inspeção antes de recomendar uma intervenção.
12. Solicitar inspeção física quando houver indícios que justifiquem verificar a lente ou a proteção externa.
13. Diferenciar informações provenientes do Eval Set de dados complementares simulados.
14. Indicar quando são necessárias novas evidências para confirmar a causa do problema.
15. Apresentar recomendações fundamentadas nos registros disponíveis.

### 6.1. Consultas e ferramentas que podem ser utilizadas

| Ferramenta do PREDICTA | Aplicação no CFTV-036 |
|---|---|
| `consultar_ativo` | Recuperar identificação, criticidade e características cadastradas |
| `consultar_historico_falhas` | Consultar os registros disponíveis e verificar a existência de ocorrências anteriores relacionadas à degradação da imagem, sem presumir reincidência de defeito físico |
| `consultar_condicoes_ambientais` | Consultar registros de temperatura, umidade, chuva e visibilidade no período da ocorrência, correlacionando-os com o horário da degradação da imagem |
| `consultar_procedimento` | Recuperar o procedimento de inspeção aplicável ao equipamento |
| `calcular_metricas_confiabilidade` | Calcular indicadores quando houver dados suficientes e consistentes, sem utilizar a degradação ambiental como falha física confirmada |

A ferramenta `listar_ativos_por_criticidade` também poderá ser utilizada em análises comparativas, caso seja necessário apoiar a priorização da manutenção. A ferramenta `abrir_ordem_servico` poderá ser utilizada para criar uma OS simulada, exclusivamente após autorização humana explícita e recente do profissional responsável.

### 6.2. Comportamento esperado do assistente

Ao analisar uma consulta sobre o CFTV-036, o PREDICTA deverá:

- Identificar a baixa visibilidade nas imagens;
- Considerar a presença de neblina intensa e umidade elevada;
- Consultar os registros ambientais disponíveis para o período da ocorrência;
- Correlacionar as condições meteorológicas com o horário da degradação da imagem;
- Considerar a ausência de falhas de comunicação;
- Informar que não existem evidências confirmadas de defeito físico;
- Evitar classificar automaticamente a degradação visual como falha do equipamento;
- Verificar se a imagem melhora após a normalização das condições ambientais;
- Consultar o procedimento de inspeção disponível;
- Recomendar inspeção física quando houver evidências que justifiquem essa necessidade;
- Diferenciar dados registrados de hipóteses técnicas;
- Não inventar medições ambientais, resultados de inspeção ou diagnósticos;
- Respeitar a necessidade de autorização humana para qualquer ação operacional.

## 7. Referências técnicas e fundamentação

### 7.1. Dados provenientes do Eval Set

- TAG: CFTV-036.
- Baixa visibilidade nas imagens durante a madrugada.
- Presença de neblina intensa e umidade elevada.
- Ausência de reincidência de falha física de imagem.
- Ausência de falhas de comunicação.
- Procedimento de inspeção disponível.
- Ausência de evidências confirmadas de defeito físico.
- Necessidade de consultar os registros ambientais, correlacioná-los com o horário da ocorrência e verificar se o problema persiste após a normalização das condições ambientais.

**Origem:** EVAL-004.

### 7.2. Características técnicas fundamentadas em fonte pública da Motiva

- Resolução Full HD.
- Zoom óptico.
- Recursos de Detecção Automática de Incidentes (DAI).
- Utilização de câmeras para monitoramento dos trechos rodoviários concedidos.

**Fonte oficial:**

Concessionária de Rodovias PRVias S.A. — Motiva Paraná. *Carta de Serviços Motiva Paraná*, seção 3.9 — Circuito fechado de televisão (CFTV), página 4 do PDF.

Link: https://rodovias.motiva.com.br/content/dam/conteudo-multicanal/rodovias/conteudo/pt/midia/prvias/carta-aos-usuarios/Carta%20de%20Servi%C3%A7os%20Motiva%20Paran%C3%A1%202.pdf

A documentação apresenta informações sobre o sistema de CFTV da concessionária, incluindo resolução Full HD, zoom óptico e recursos de Detecção Automática de Incidentes.

### 7.3. Fundamentação regulatória e meteorológica

A Resolução ANTT nº 6.000/2022 apresenta requisitos relacionados ao monitoramento meteorológico rodoviário.

Entre os elementos abordados estão variáveis ambientais relevantes para a operação rodoviária, como:

- Temperatura;
- Precipitação;
- Umidade relativa;
- Visibilidade;
- Condições de neblina, névoa e nevoeiro;
- Disponibilização de informações meteorológicas ao Centro de Controle Operacional, conforme os requisitos aplicáveis.

**Fonte oficial:**

Agência Nacional de Transportes Terrestres (ANTT). *Resolução nº 6.000, de 1º de dezembro de 2022*.

Link: https://anttlegis.antt.gov.br/action/ActionDatalegis.php?acao=abrirTextoAto&cod_menu=7796&cod_modulo=161&link=S&numeroAto=00006000&orgao=DG%2FANTT%2FMI&seqAto=000&tipo=RES&valorAno=2022

A resolução fundamenta a importância das variáveis meteorológicas para o acompanhamento das condições operacionais das rodovias. Sua aplicação específica deve observar as condições e obrigações do contrato de concessão correspondente.

### 7.4. Fundamentação técnica complementar

**Fonte 1 — Axis Communications**

- **Instituição:** Axis Communications.
- **Documento:** *Troubleshooting guide for image quality*.
- **Assuntos relevantes:** problemas de qualidade de imagem, gotas de água, sujeira, poeira, reflexos e outras interferências visuais.
- **Link:** https://help.axis.com/en-us/troubleshooting-image-quality

A documentação apresenta possíveis fatores que podem comprometer a qualidade das imagens capturadas por câmeras de monitoramento, incluindo condições relacionadas à lente, à proteção externa e à iluminação.

**Aplicação na persona:** fundamenta a inclusão de sujeira, gotas de água e outras interferências ópticas como possibilidades de investigação, sem afirmar que estejam presentes no CFTV-036.

**Fonte 2 — Axis Communications**

- **Instituição:** Axis Communications.
- **Documento:** *AXIS Q1635 Fixed Network Camera — User Manual*.
- **Assunto:** recurso de compensação de neblina (Defog) em um modelo específico de câmera.
- **Link:** https://www.axis.com/dam/public/c7/78/d5/axis-q1635--user-manual-en-US-103962.pdf

O manual apresenta o recurso Defog em um equipamento específico da fabricante.

**Aplicação na persona:** serve como referência técnica para fundamentar a existência de tecnologias de compensação de neblina em determinados modelos de câmeras. Não comprova que o equipamento fictício VisionTech VT-Road Weather 25X possua esse recurso.

### 7.5. Dados fictícios e premissas da persona

Foram criados para completar o cadastro e permitir simulações mais realistas:

- Fabricante e modelo do equipamento;
- Zoom óptico de 25x;
- Movimento PTZ;
- Protocolo ONVIF;
- Protocolo RTSP;
- Alimentação PoE+;
- Grau de proteção IP66;
- Ano de instalação;
- Localização genérica em trecho sujeito à neblina;
- Condições ambientais detalhadas;
- Horário específico da ocorrência;
- Temperatura e umidade específicas do cenário;
- Ausência de chuva no cenário complementar;
- Datas e horários complementares das observações;
- Valores individuais de umidade das observações;
- Recurso de compensação de neblina;
- Periodicidades do plano de manutenção;
- Etapas complementares do procedimento técnico de inspeção;
- Hipóteses técnicas de investigação;
- Indicadores técnicos propostos para investigação;
- Critérios complementares de encaminhamento para manutenção.
