# Cadastro de Ativo — CFTV-042

## 1. Identificação do ativo

- **TAG:** CFTV-042
- **Tipo de ativo:** Câmera de monitoramento rodoviário (CFTV)
- **Criticidade:** Média — classificação simulada para a persona.
- **Localização:** Trecho rodoviário concedido — localização fictícia não especificada.
- **Condição do cadastro:** Persona sintética elaborada para fins acadêmicos e testes do PREDICTA.
- **Vínculo com o Eval Set:** EVAL-008.

## 2. Caracterização técnica

### 2.1. Especificações técnicas adotadas para a persona

| Característica | Especificação adotada | Origem |
|---|---|---|
| Tipo de equipamento | Câmera IP de monitoramento rodoviário | Simulada |
| Fabricante | VisionTech — fabricante fictício | Simulada |
| Modelo | VT-Road Network 30X — modelo fictício | Simulada |
| Resolução | Full HD (1920 × 1080) | Referência técnica pública |
| Zoom óptico | 30x | Simulada |
| Movimento | PTZ (pan, tilt e zoom) | Simulada |
| Protocolo de comunicação | ONVIF | Simulada |
| Protocolo de transmissão de vídeo | RTSP | Simulada |
| Alimentação elétrica | PoE+ | Simulada |
| Proteção do equipamento | IP66 | Simulada |
| Instalação | Ambiente externo, em estrutura elevada | Simulada |
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
- **Interface de rede:** permite a comunicação entre a câmera e a infraestrutura de monitoramento.

## 3. Contexto operacional

O CFTV-042 representa uma câmera de monitoramento rodoviário responsável por transmitir imagens ao Centro de Controle Operacional (CCO).

Conforme o cenário definido no EVAL-008, o histórico do ativo apresenta registros de indisponibilidade e duas ocorrências anteriores. Entretanto, as evidências disponíveis não são suficientes para confirmar a causa do problema.

A situação exige uma investigação baseada no histórico de falhas, nos registros de funcionamento e nas condições de comunicação do equipamento.

A indisponibilidade de uma câmera pode estar relacionada a diferentes fatores, como alimentação elétrica, conectividade de rede, transmissão de vídeo, processamento do equipamento ou problemas físicos. Essas possibilidades devem ser investigadas, mas nenhuma delas poderá ser apresentada como causa confirmada sem evidências.

O principal objetivo da análise será identificar padrões nas ocorrências, verificar a existência de recorrência e reunir informações suficientes para orientar a avaliação técnica.

### 3.1. Condições de instalação e operação

Para fins de simulação, considera-se que o equipamento:

- Está instalado em estrutura de monitoramento rodoviário;
- Opera continuamente, durante 24 horas por dia;
- Está exposto a chuva, poeira, umidade e variações de temperatura;
- Depende de alimentação elétrica para funcionamento;
- Utiliza infraestrutura de comunicação de dados para transmitir imagens ao CCO;
- Está integrado a um sistema de monitoramento que permite consultar imagens e registros de funcionamento;
- Depende da disponibilidade dos equipamentos e serviços de rede associados para manter a transmissão de vídeo.

### 3.2. Condições operacionais de referência

| Variável | Condição considerada | Origem |
|---|---|---|
| TAG do equipamento | CFTV-042 | Proveniente do Eval Set |
| Condição operacional | Indisponibilidade registrada no histórico | Proveniente do Eval Set |
| Ocorrências anteriores | Duas ocorrências anteriores | Proveniente do Eval Set |
| Causa das ocorrências | Não confirmada | Proveniente do Eval Set |
| Alimentação elétrica | Sem informação conclusiva | Simulada |
| Conectividade de rede | Sem informação conclusiva | Simualda |
| Estado da transmissão de vídeo | Indisponibilidade registrada | Proveniente do Eval Set |
| Existência de defeito físico | Não confirmada | Simulada |
| Resultado de inspeção técnica | Não informado | Simulada |

## 4. Histórico de falhas

Conforme o cenário definido no EVAL-008:

- O histórico do CFTV-042 apresenta registros de indisponibilidade.
- Existem duas ocorrências anteriores registradas.
- As evidências disponíveis não são suficientes para confirmar a causa do problema.
- Não há diagnóstico conclusivo que permita atribuir a indisponibilidade a um componente específico.
- Não foram fornecidos detalhes suficientes para determinar as causas, intervenções realizadas ou resultados das ocorrências anteriores.

**Interpretação para o PREDICTA:**

A existência de duas ocorrências anteriores indica que há registros de recorrência de indisponibilidade no histórico do ativo.

Entretanto, a repetição de um sintoma não comprova que as ocorrências tenham a mesma causa.

O PREDICTA deverá consultar o histórico disponível, identificar os eventos registrados e verificar quais informações podem ser utilizadas para aprofundar a investigação.

O assistente não deverá afirmar que existe defeito na câmera, falha de rede, problema de alimentação elétrica ou qualquer outra causa específica sem evidências que sustentem essa conclusão.

A análise deverá distinguir os fatos registrados das hipóteses técnicas e indicar quais informações ainda precisam ser coletadas.

### 4.1. Complementação do histórico

| Ocorrência | Data e horário | Sintoma registrado | Causa | Intervenção | Resultado |
|---|---|---|---|---|---|
| 1 | Não informado | Indisponibilidade | Não confirmada | Não informado | Não informado |
| 2 | Não informado | Indisponibilidade | Não confirmada | Não informado | Não informado |

### 4.2. Hipóteses técnicas para investigação

Considerando a indisponibilidade registrada, as seguintes possibilidades poderão ser avaliadas:

| Hipótese | Possível relação com o sintoma | Evidência necessária |
|---|---|---|
| Falha de alimentação elétrica | A interrupção da alimentação pode provocar desligamento do equipamento | Registros de alimentação, alarmes elétricos e inspeção técnica |
| Perda de conectividade de rede | A interrupção da comunicação pode impedir o acesso à câmera | Registros de rede, conectividade e alarmes |
| Congestionamento ou sobrecarga de rede | Pode comprometer a transmissão do fluxo de vídeo | Dados de utilização de banda, perda de pacotes e registros de rede |
| Falha na transmissão de vídeo | O equipamento pode permanecer ativo, mas não disponibilizar o fluxo de vídeo | Registros RTSP, servidor de vídeo e monitoramento |
| Falha de processamento do equipamento | Problemas internos podem afetar o funcionamento ou a disponibilização das imagens | Logs do equipamento e diagnóstico técnico |
| Defeito físico na câmera | Pode provocar indisponibilidade total ou intermitente | Inspeção e testes técnicos especializados |
| Falha em equipamento intermediário | Switches, fontes ou outros componentes podem afetar a comunicação ou alimentação | Registros dos equipamentos associados e testes da infraestrutura |

### 4.4. Indicadores técnicos que podem auxiliar no diagnóstico

| Indicador | Finalidade | Possível interpretação |
|---|---|---|
| Quantidade de ocorrências | Identificar registros de indisponibilidade | Permite reconhecer a existência de recorrência |
| Duração da indisponibilidade | Avaliar o tempo em que o ativo permaneceu indisponível | Auxilia na avaliação do impacto operacional |
| Intervalo entre ocorrências | Identificar a distribuição temporal dos eventos | Pode auxiliar na investigação de padrões de recorrência |
| Disponibilidade do ativo | Avaliar o tempo em que o equipamento permaneceu disponível | Permite acompanhar o comportamento operacional |
| Alarmes de comunicação | Identificar registros de perda de conectividade | Podem orientar a investigação da infraestrutura de rede |
| Registros de alimentação | Verificar possíveis interrupções elétricas | Podem auxiliar na investigação de falhas de energia |
| Registros de transmissão | Avaliar a disponibilidade do fluxo de vídeo | Permitem diferenciar problemas de transmissão de outras indisponibilidades |
| Histórico de intervenções | Verificar ações realizadas e resultados registrados | Ajuda a identificar se houve recuperação ou reincidência após intervenções |

## 5. Condições de manutenção

- **Criticidade operacional:** Média — classificação simulada para a persona.
- **Condição identificada:** Indisponibilidade registrada no histórico do ativo.
- **Histórico de falhas:** Duas ocorrências anteriores de indisponibilidade, conforme o cenário de avaliação.
- **Causa das ocorrências:** Não confirmada.
- **Plano de manutenção:** Plano preventivo proposto para a persona, com atividades simuladas.
- **Procedimento técnico:** Procedimento de diagnóstico de indisponibilidade e comunicação, proposto para fins de simulação.
- **Necessidade de avaliação:** Consultar o histórico, verificar os registros de alimentação, conectividade e transmissão e encaminhar a investigação técnica conforme as evidências encontradas.
- **Prioridade de atendimento:** A definir conforme criticidade, duração da indisponibilidade, impacto operacional e critérios do plano de manutenção.

### 5.1. Plano de manutenção simulado

| Atividade | Periodicidade proposta | Classificação |
|---|---|---|
| Verificação remota da disponibilidade da câmera | Mensal | Simulada |
| Análise dos alarmes de comunicação | Mensal | Simulada |
| Verificação dos registros de transmissão de vídeo | Mensal | Simulada |
| Inspeção das conexões e alimentação elétrica | Trimestral | Simulada |
| Verificação da infraestrutura de rede associada | Trimestral | Simulada |
| Inspeção visual da câmera e estrutura | Semestral | Simulada |
| Revisão do histórico de falhas e intervenções | Semestral | Simulada |

### 5.2. Procedimento técnico simulado

1. Confirmar a TAG do equipamento.
2. Consultar o histórico de indisponibilidades e identificar as ocorrências anteriores.
3. Verificar as datas, horários e durações dos eventos, quando essas informações estiverem disponíveis.
4. Consultar os alarmes registrados no período da ocorrência.
5. Verificar o estado de comunicação entre a câmera e o sistema de monitoramento.
6. Consultar os registros de transmissão de vídeo.
7. Verificar os registros de alimentação elétrica, caso estejam disponíveis.
8. Avaliar possíveis falhas na infraestrutura de rede associada.
9. Comparar os registros atuais com as ocorrências anteriores.
10. Identificar quais hipóteses possuem evidências suficientes para continuar a investigação.
11. Consultar o procedimento técnico documentado aplicável.
12. Encaminhar a demanda para avaliação especializada quando os registros remotos forem insuficientes.
13. Registrar os resultados da investigação e as informações efetivamente confirmadas.
14. Atualizar o histórico do ativo após a conclusão da avaliação ou intervenção.

### 5.3. Critérios para encaminhamento à manutenção

O encaminhamento deverá considerar:

- Persistência da indisponibilidade;
- Quantidade e frequência das ocorrências registradas;
- Duração dos períodos de indisponibilidade;
- Existência de alarmes de comunicação;
- Registros de falhas de alimentação elétrica;
- Evidências de problemas na transmissão de vídeo;
- Resultados das verificações remotas;
- Necessidade de inspeção física;
- Impacto operacional da indisponibilidade;
- Criticidade cadastrada do equipamento.

## 6. Aplicação no PREDICTA

1. Identificar corretamente o ativo CFTV-042.
2. Reconhecer os registros de indisponibilidade presentes no histórico.
3. Identificar a existência de duas ocorrências anteriores.
4. Reconhecer que as evidências disponíveis são insuficientes para confirmar a causa.
5. Consultar o histórico de falhas antes de apresentar uma conclusão.
6. Diferenciar recorrência de sintoma e recorrência de causa.
7. Considerar hipóteses de alimentação elétrica, conectividade, transmissão e falha física sem tratá-las como diagnósticos confirmados.
8. Identificar informações ausentes que poderiam auxiliar na investigação.
9. Evitar inventar datas, durações, causas ou intervenções anteriores.
10. Consultar procedimentos documentados antes de recomendar uma intervenção.
11. Solicitar registros adicionais quando forem necessários para aprofundar o diagnóstico.
12. Calcular indicadores de confiabilidade somente quando houver dados suficientes.
13. Evitar afirmar que existe um padrão temporal sem datas e intervalos comprovados.
14. Apresentar recomendações fundamentadas nas evidências disponíveis.
15. Respeitar o mecanismo de autorização humana para abertura de ordem de serviço simulada.

### 6.1. Consultas e ferramentas que podem ser utilizadas

| Ferramenta do PREDICTA | Aplicação no CFTV-042 |
|---|---|
| `consultar_ativo` | Recuperar a identificação, criticidade e características cadastradas do equipamento |
| `consultar_historico_falhas` | Consultar as duas ocorrências anteriores de indisponibilidade e recuperar os detalhes efetivamente registrados |
| `consultar_condicoes_ambientais` | Consultar as condições ambientais no período das ocorrências, caso existam registros e haja justificativa técnica para essa investigação |
| `consultar_procedimento` | Recuperar procedimentos documentados para investigação de indisponibilidade e problemas de comunicação |
| `calcular_metricas_confiabilidade` | Calcular indicadores de confiabilidade e disponibilidade somente quando houver dados suficientes e consistentes |

A ferramenta `listar_ativos_por_criticidade` também poderá ser utilizada em análises comparativas, caso seja necessário apoiar a priorização da manutenção entre diferentes equipamentos.

A ferramenta `abrir_ordem_servico` poderá criar exclusivamente uma ordem de serviço simulada, após autorização humana explícita e recente. A abertura da OS não confirma a causa da indisponibilidade nem representa autorização automática para a execução de uma intervenção.

### 6.2. Comportamento esperado do assistente

Ao analisar uma consulta sobre o CFTV-042, o PREDICTA deverá:

- Identificar os registros de indisponibilidade;
- Informar que existem duas ocorrências anteriores no histórico;
- Consultar os detalhes disponíveis sobre cada evento;
- Reconhecer que a causa não foi confirmada;
- Evitar atribuir a indisponibilidade a uma falha específica sem evidências;
- Diferenciar os sintomas registrados das hipóteses técnicas;
- Verificar a existência de alarmes de comunicação, alimentação e transmissão;
- Identificar as informações ausentes;
- Recomendar verificações compatíveis com os registros disponíveis;
- Consultar procedimentos documentados;
- Solicitar avaliação técnica especializada quando necessário;
- Calcular indicadores somente quando os dados forem suficientes;
- Não inventar datas, durações, intervenções ou resultados;
- Respeitar a necessidade de autorização humana para abertura de uma ordem de serviço simulada.

## 7. Referências técnicas e fundamentação

### 7.1. Dados provenientes do Eval Set

- TAG: CFTV-042.
- Histórico com registros de indisponibilidade.
- Existência de duas ocorrências anteriores.
- Evidências insuficientes para confirmar a causa do problema.
- Necessidade de evitar a criação de diagnósticos não sustentados pelos registros.

**Origem:** EVAL-008.

### 7.2. Características técnicas fundamentadas em fonte pública da Motiva

- Utilização de câmeras para monitoramento dos trechos rodoviários concedidos.
- Resolução Full HD.
- Zoom óptico.
- Recursos de Detecção Automática de Incidentes (DAI).

**Fonte oficial:**

Concessionária de Rodovias PRVias S.A. — Motiva Paraná. *Carta de Serviços Motiva Paraná*, seção 3.9 — Circuito fechado de televisão (CFTV), página 4 do PDF.

Link: https://rodovias.motiva.com.br/content/dam/conteudo-multicanal/rodovias/conteudo/pt/midia/prvias/carta-aos-usuarios/Carta%20de%20Servi%C3%A7os%20Motiva%20Paran%C3%A1%202.pdf

A documentação é utilizada como referência pública para a caracterização geral de sistemas de CFTV rodoviário. Não comprova o fabricante, o modelo ou as demais especificações simuladas do CFTV-042.

### 7.3. Fundamentação técnica complementar — conectividade de rede

**Instituição:** Axis Communications.

**Documento:** *Troubleshooting guide for network connection*.

**Link:** https://help.axis.com/en-us/troubleshooting-network

A documentação apresenta orientações para investigação de problemas de conexão em equipamentos de rede, abordando fatores como infraestrutura, largura de banda, perda de pacotes, sobrecarga e congestionamento.

**Aplicação na persona:** fundamenta a inclusão de conectividade e infraestrutura de rede como possibilidades de investigação da indisponibilidade do CFTV-042.

A referência não comprova que tenha ocorrido falha de rede neste ativo.

### 7.4. Fundamentação técnica complementar — transmissão de vídeo

**Instituição:** Axis Communications.

**Documento:** *Troubleshooting guide for streaming issues*.

**Link:** https://help.axis.com/en-us/troubleshooting-streaming

A documentação apresenta fatores que podem afetar a transmissão de vídeo, incluindo latência, processamento do equipamento, infraestrutura de rede, largura de banda e comportamento do cliente de visualização.

**Aplicação na persona:** fundamenta a investigação da transmissão de vídeo como uma etapa distinta da verificação de conectividade e do funcionamento físico da câmera.

A referência não comprova que a indisponibilidade do CFTV-042 tenha sido provocada por problemas de streaming.

### 7.5. Fundamentação técnica complementar — câmeras de rede

**Instituição:** Microsoft.

**Documento:** *Network Cameras*.

**Link:** https://learn.microsoft.com/en-us/windows-hardware/drivers/stream/network-cameras

A documentação apresenta conceitos relacionados à integração e ao funcionamento de câmeras de rede.

**Aplicação na persona:** serve como referência complementar para a compreensão da comunicação entre câmeras IP e sistemas que recebem e processam seus fluxos de vídeo.

A documentação não comprova a arquitetura específica utilizada no CFTV-042.

### 7.6. Dados fictícios e premissas da persona

Foram criados para completar o cadastro e permitir simulações mais realistas:

- Criticidade média;
- Fabricante e modelo do equipamento;
- Zoom óptico de 30x;
- Movimento PTZ;
- Protocolo ONVIF;
- Protocolo RTSP;
- Alimentação PoE+;
- Grau de proteção IP66;
- Ano de instalação;
- Características complementares de instalação e operação;
- Plano de manutenção preventiva;
- Periodicidades das atividades de manutenção;
- Procedimento técnico de investigação;
- Hipóteses técnicas para diagnóstico;
- Indicadores complementares para investigação;
- Critérios de encaminhamento para manutenção.
