# Inventário da Base de Conhecimento — PREDICTA

## 1. Objetivo

Este documento apresenta o inventário dos materiais que deverão compor a base de conhecimento do PREDICTA, assistente desenvolvido para apoiar a operação e a Engenharia de Manutenção na análise de ocorrências, investigação de possíveis falhas e priorização de intervenções em ativos de Sistemas Inteligentes de Transporte (ITS), com foco nos equipamentos CFTV contemplados pelo recorte do projeto.

A base será utilizada para recuperar informações técnicas e operacionais documentadas, incluindo dados cadastrais dos ativos, histórico de falhas, procedimentos, condições ambientais, critérios de criticidade e requisitos de segurança.

O objetivo é fornecer informações rastreáveis que contribuam para:

- Consulta de dados técnicos e cadastrais dos ativos;
- Análise de ocorrências e identificação de possíveis causas;
- Consulta de histórico e identificação de reincidências;
- Diferenciação entre falhas técnicas e condições ambientais;
- Avaliação de criticidade e priorização de atendimentos;
- Apoio à elaboração de propostas de ordens de serviço;
- Consulta de procedimentos e requisitos de segurança aplicáveis.

Os dados simulados serão identificados como fictícios e não deverão ser apresentados como registros reais da Motiva ou de qualquer operação efetiva.

## 2. Inventário dos documentos

### Documento 1 — Catálogo de ativos

- **Finalidade:** reunir informações cadastrais e técnicas dos ativos contemplados pelo recorte do projeto, permitindo sua identificação e consulta por TAG.

- **Conteúdo previsto:**
  - TAG de identificação do ativo;
  - Tipo de equipamento;
  - Fabricante;
  - Modelo;
  - Quilometragem (km), quando aplicável;
  - Identificação da praça ou pórtico;
  - Localização e trecho de instalação;
  - Data de instalação, quando disponível;
  - Vida útil estimada;
  - Classificação de criticidade;
  - Status operacional (ativo, inativo, em manutenção ou desativado);
  - Data de referência do cadastro;
  - Horas de operação acumuladas, quando disponíveis.

- **Origem:** dados cadastrais fictícios elaborados para fins acadêmicos.
- **Classificação da fonte:** simulada.
- **Quantidade mínima prevista:** 30 linhas de cadastro.
- **Status:** conteúdo a ser elaborado.

### Documento 2 — Plano de manutenção preventiva

- **Finalidade:** documentar as atividades preventivas e os critérios operacionais utilizados como referência para orientar a manutenção e apoiar a priorização de ocorrências.

- **Conteúdo previsto:**
  - Código ou identificação do plano;
  - Identificação do ativo ou categoria de ativos;
  - Tarefa de manutenção;
  - Periodicidade, definida por tempo, horas de operação ou condição do equipamento, conforme a referência técnica disponível;
  - Responsável pela atividade;
  - Tempo estimado de execução;
  - Recursos e ferramentas necessários;
  - Condições para execução;
  - Pré-requisitos e cuidados de segurança;
  - Critérios de inspeção;
  - Critérios de aceitação para conclusão da atividade;
  - Modalidades de intervenção;
  - Diretrizes de escalonamento e encaminhamento;
  - Critérios de priorização relacionados à criticidade, impacto, indisponibilidade e reincidência, em conformidade com a matriz de criticidade do projeto;
  - Condições de aplicabilidade do plano;
  - Referências técnicas utilizadas, como manuais, normas e procedimentos aplicáveis;
  - Data de elaboração e data da última revisão.

- **Origem:** plano fictício elaborado para fins acadêmicos.
- **Classificação da fonte:** simulada.
- **Quantidade mínima prevista:** 1 plano documentado.
- **Status:** conteúdo a ser elaborado.

### Documento 3 — Histórico de falhas do FSM

- **Finalidade:** registrar ocorrências anteriores e permitir a consulta de padrões de falhas, reincidências, intervenções e resultados dos atendimentos, fornecendo dados temporais e de exposição para apoiar os cálculos de confiabilidade.

- **Conteúdo previsto:**
  - TAG do ativo;
  - Data e horário da ocorrência;
  - Tipo de falha;
  - Sintoma identificado;
  - Causa identificada, quando conhecida;
  - Tempo de reparo;
  - Data e horário de início e término da intervenção, quando disponíveis;
  - Peça ou componente substituído, quando aplicável;
  - Intervenção realizada;
  - Resultado do atendimento;
  - Registro de reincidência;
  - Situação da ocorrência;
  - Horas de operação acumuladas do ativo, quando disponíveis;
  - Horas de operação desde a última falha, quando disponíveis;
  - Período de exposição sem falhas, quando disponível;
  - Registro de modificações ou intervenções que possam influenciar o comportamento de falhas;
  - Identificação de observações de vida até a falha ou observações censuradas, quando aplicável;
  - Identificação individual do componente ou conjunto analisado, quando aplicável;
  - Data de início do acompanhamento do componente;
  - Data da falha ou do encerramento da observação;
  - Tempo de vida acumulado até a falha ou censura;
  - Indicador de ocorrência da falha ou censura da observação;
  - Identificação da intervenção ou modificação realizada;
  - Data da intervenção ou modificação;
  - Identificação dos períodos anterior e posterior à intervenção, quando aplicável;
  - Data de referência e período de acompanhamento do ativo.

- **Origem:** registros fictícios elaborados para simular o histórico de manutenção dos ativos no FSM.
- **Classificação da fonte:** simulada.
- **Quantidade mínima prevista:** 50 registros de falhas.
- **Status:** conteúdo a ser elaborado.

**Tabela complementar — Exposição operacional dos ativos**

Além dos registros individuais de falhas, será elaborada uma tabela complementar para documentar os períodos de acompanhamento e a exposição operacional dos ativos.

Campos previstos:

- TAG do ativo;
- Identificação do componente ou conjunto ao qual a exposição se refere, quando aplicável;
- Data de início do período de acompanhamento;
- Data de término do período de acompanhamento;
- Horas de operação durante o período;
- Horas de operação acumuladas desde a última falha;
- Horas de operação acumuladas antes e depois de intervenções ou modificações relevantes, quando disponíveis;
- Identificação do período de análise;
- Fonte do dado;
- Unidade de tempo utilizada;
- Indicação de períodos com dados completos ou incompletos;
- Observações sobre lacunas, interrupções, indisponibilidade ou limitações dos registros.

Os registros de exposição deverão ser relacionados ao histórico de falhas por TAG, componente, quando aplicável, e período correspondente, preservando a sequência cronológica dos eventos. Períodos sem falhas também poderão ser registrados quando houver dados de exposição disponíveis.

Os dados deverão distinguir períodos efetivamente acompanhados de períodos sem informação suficiente. As análises de confiabilidade deverão considerar apenas dados adequados ao método utilizado.

As análises de confiabilidade deverão respeitar os requisitos específicos de cada método:

- Para RGA, deverão ser considerados dados cronológicos de falhas, exposição operacional comparável e registros de intervenções ou modificações, permitindo avaliar a evolução do comportamento de falhas ao longo do tempo.
- Para LDA, deverão ser considerados dados individuais de vida até a falha ou censura, com identificação do componente, início do acompanhamento, tempo observado e situação ao término do período.
- A ausência de dados suficientes para determinada análise deverá ser informada explicitamente, sem substituição por valores presumidos ou estimativas não fundamentadas.
- O período padrão de 12 meses poderá ser ampliado quando necessário para análises que dependam de histórico longitudinal, desde que os dados adicionais estejam disponíveis e sejam compatíveis com o método utilizado.

Quando os dados forem insuficientes, o PREDICTA deverá informar a limitação, sem inventar valores ou apresentar estimativas sem fundamentação.

### Documento 4 — Procedimentos operacionais (POPs)

- **Finalidade:** fornecer orientações documentadas para consulta e apoio à análise de inspeções, diagnósticos e atividades de manutenção relacionadas aos ativos CFTV, respeitando os limites de segurança e qualificação profissional. Os procedimentos servem como referência para o PREDICTA e não representam autorização automática para execução de intervenções.

- **Conteúdo previsto:**
  - Identificação do procedimento;
  - Objetivo;
  - Campo de aplicação;
  - Ativo ou equipamento abrangido;
  - Materiais e ferramentas necessários;
  - Pré-requisitos de execução;
  - Sequência de atividades;
  - Cuidados e requisitos de segurança;
  - Requisitos de qualificação profissional;
  - Critérios de conclusão;
  - Referências técnicas utilizadas.

- **Origem:** procedimentos simulados elaborados para fins acadêmicos.
- **Classificação da fonte:** simulada.
- **Quantidade mínima prevista:** 3 procedimentos.
- **Status:** conteúdo a ser elaborado.

**Procedimentos inicialmente previstos:**

1. Diagnóstico de perda de comunicação em câmeras CFTV.
2. Inspeção de degradação da qualidade da imagem e análise de possíveis fatores ambientais.
3. Inspeção e conservação de equipamentos CFTV, considerando requisitos de segurança e qualificação profissional.

### Documento 5 — Fichas técnicas dos equipamentos

- **Finalidade:** reunir informações técnicas específicas dos equipamentos para apoiar consultas sobre características, operação, instalação, inspeção e manutenção.

- **Conteúdo previsto:**
  - Identificação do equipamento;
  - Tipo de ativo;
  - Fabricante;
  - Modelo;
  - Especificações técnicas;
  - Características de operação;
  - Requisitos de instalação;
  - Condições ambientais de operação;
  - Orientações de inspeção;
  - Recomendações de limpeza e conservação;
  - Requisitos de manutenção;
  - Referência ao manual técnico correspondente.

- **Origem:** documentos técnicos reais dos fabricantes, complementados por fichas simuladas para fins acadêmicos quando necessário. As informações reais e simuladas deverão ser claramente identificadas, sem apresentar dados fictícios como especificações oficiais.
- **Classificação da fonte:** real e simulada, devidamente identificada.
- **Abrangência mínima prevista:** todos os ativos do recorte definido para o projeto.
- **Status:** modelos e documentos técnicos ainda a selecionar.

### Documento 6 — Matriz de criticidade

- **Finalidade:** estabelecer critérios documentados para classificação da criticidade dos ativos e apoiar a priorização de ocorrências e intervenções.

- **Conteúdo previsto:**
  - Identificação do ativo;
  - Classificação de criticidade;
  - Impacto na arrecadação, quando aplicável;
  - Impacto na segurança viária;
  - Impacto na disponibilidade operacional;
  - Consequências da indisponibilidade;
  - Critérios de classificação;
  - Escala ou níveis de criticidade adotados;
  - Regras para enquadramento dos ativos em cada nível;
  - Prioridade de atendimento associada;
  - Justificativa da classificação.

- **Origem:** matriz fictícia elaborada para fins acadêmicos, considerando o contexto operacional do projeto.
- **Classificação da fonte:** simulada.
- **Quantidade mínima prevista:** 1 matriz documentada.
- **Status:** conteúdo a ser elaborado.

### Documento 7 — Glossário de siglas

- **Finalidade:** padronizar termos técnicos e siglas utilizados no projeto, reduzindo ambiguidades nas consultas e respostas do assistente.

- **Conteúdo previsto:**
  - CFTV — Circuito Fechado de Televisão;
  - PMV — Painel de Mensagens Variáveis;
  - SAT — Sistema de Arrecadação e Tráfego, conforme a terminologia do briefing;
  - SCA — sigla conforme definição da documentação de referência;
  - CCO — Centro de Controle Operacional;
  - CBM — Condition-Based Maintenance (Manutenção Baseada na Condição);
  - RCM — Reliability-Centered Maintenance (Manutenção Centrada na Confiabilidade);
  - WCM — World Class Manufacturing;
  - FSM — sigla utilizada para identificar o sistema de histórico de falhas no contexto do projeto;
  - RGA, LDA, MTBF, MTTR, WIM e outras siglas presentes nos documentos de referência.

- **Origem:** briefing do projeto e referências técnicas selecionadas.
- **Classificação da fonte:** real/técnica.
- **Quantidade mínima prevista:** 1 glossário.
- **Status:** conteúdo a ser elaborado.

### Documento 8 — Normas e requisitos de segurança

- **Finalidade:** reunir resumos dos requisitos normativos e das regras de segurança relevantes para as atividades de inspeção e manutenção dos ativos contemplados pelo projeto.

- **Conteúdo previsto:**
  - Resumo dos requisitos aplicáveis da NR-10, relacionados à segurança em instalações e serviços em eletricidade;
  - Resumo dos requisitos aplicáveis da NR-35, relacionados ao trabalho em altura;
  - Regras internas de segurança para atividades em via;
  - Requisitos de qualificação e capacitação profissional;
  - Cuidados e restrições para intervenções em equipamentos;
  - Referência à norma ou documento de origem;
  - Identificação da versão e data de consulta.

- **Origem:** normas e documentos reais, apresentados em forma de resumo.
- **Classificação da fonte:** real (resumo).
- **Quantidade mínima prevista:** 1 documento consolidado.
- **Status:** referências ainda a selecionar e verificar.

### Documento 9 — Documentos do briefing Motiva

- **Finalidade:** reunir informações de contexto e orientações do desafio que fundamentam a proposta da PREDICTA.

- **Conteúdo previsto:**
  - Slides de contexto;
  - Descrição das ondas de inovação;
  - Descrição dos temas 1, 2 e 2.1;
  - Informações relacionadas ao desafio de monitoramento e manutenção;
  - Requisitos e orientações fornecidos para o desenvolvimento do projeto;
  - Informações que fundamentam o recorte escolhido;
  - Referências às páginas e seções dos documentos originais.

- **Origem:** documentos reais do briefing disponibilizados para o desenvolvimento do projeto.
- **Classificação da fonte:** real/briefing.
- **Quantidade mínima prevista:** 1 conjunto documental.
- **Status:** materiais de referência a organizar e preparar para consulta.

### Documento 10 — Boletins de ocorrência e laudos de campo

- **Finalidade:** registrar relatos de ocorrências e informações coletadas durante atendimentos e inspeções, apoiando a investigação de falhas e a correlação com condições ambientais. Os registros deverão distinguir observações realizadas, hipóteses levantadas e conclusões técnicas confirmadas.

- **Conteúdo previsto:**
  - TAG do ativo;
  - Data e horário da ocorrência;
  - Identificação do tipo de evento;
  - Relato textual do técnico;
  - Sintoma observado;
  - Condições ambientais no momento da ocorrência;
  - Temperatura, quando disponível;
  - Umidade relativa do ar, quando disponível;
  - Ocorrência de chuva;
  - Presença de neblina ou baixa visibilidade;
  - Condições de luminosidade;
  - Inspeções ou verificações realizadas;
  - Encaminhamento indicado;
  - Resultado registrado, quando disponível.

- **Origem:** boletins e relatos fictícios elaborados para fins acadêmicos.
- **Classificação da fonte:** simulada.
- **Quantidade mínima prevista:** 10 registros.
- **Status:** conteúdo a ser elaborado.

## 3. Classificação das fontes

Para garantir transparência e rastreabilidade sobre a procedência das informações, os documentos e seus respectivos segmentos serão identificados por meio de dois metadados complementares:

**Tipo de origem (`source_type`)**

| Classificação | Descrição |
|---|---|
| `simulada` | Informação fictícia criada exclusivamente para representar situações de operação e manutenção no projeto acadêmico. |
| `real` | Documento ou informação extraída de uma fonte existente e identificável. |

**Categoria da fonte (`source_category`)**

| Classificação | Descrição |
|---|---|
| `fabricante` | Manuais, fichas técnicas e demais documentos oficiais fornecidos pelos fabricantes dos equipamentos. |
| `norma` | Normas regulamentadoras e outros documentos normativos aplicáveis. |
| `briefing` | Informações extraídas dos documentos de orientação e descrição do desafio. |
| `tecnica` | Referências técnicas e materiais especializados utilizados para fundamentar informações do projeto. |
| `operacional` | Registros e documentos relacionados à operação e manutenção dos ativos. |

Quando um documento combinar informações reais e simuladas, a classificação deverá ser realizada por informação ou segmento, sempre que necessário, para evitar que dados fictícios sejam apresentados como oficiais.

A identificação da fonte deverá permitir rastrear a procedência de cada informação recuperada pela base de conhecimento.

## 4. Estratégia de preparação e segmentação dos documentos

Os documentos serão preparados para possibilitar sua recuperação pela arquitetura RAG (Retrieval-Augmented Generation) do PREDICTA, utilizando embeddings gerados pelo modelo BGE-M3 e armazenamento e recuperação vetorial por meio do ChromaDB.

A estratégia inicial de segmentação será:

- **Tamanho dos chunks:** aproximadamente 500 a 800 tokens.
- **Sobreposição (overlap):** aproximadamente 80 a 100 tokens.
- **Preservação de contexto:** manter títulos, subtítulos, identificação do documento e informações necessárias para compreender cada trecho.
- **Tabelas e históricos:** preservar a relação entre campos e registros, evitando segmentações que comprometam a interpretação dos dados.
- **Rastreabilidade:** manter informações suficientes para identificar o documento de origem, sua versão e sua classificação.
- **Registros operacionais:** evitar separar informações relacionadas ao mesmo evento, ativo ou ocorrência quando isso comprometer a compreensão do registro.

**Justificativa do tamanho dos chunks:** a segmentação em blocos de aproximadamente 500 a 800 tokens busca equilibrar a preservação do contexto técnico e a recuperação de informações específicas. Blocos muito extensos podem trazer informações desnecessárias para uma consulta, enquanto blocos excessivamente pequenos podem separar dados que precisam ser interpretados em conjunto.

Embora a janela de contexto do LLM permita processar uma quantidade maior de tokens, não é necessário recuperar documentos inteiros em todas as consultas. A recuperação de trechos relevantes permite utilizar melhor o contexto disponível, reduzindo informações desnecessárias e favorecendo respostas fundamentadas nas fontes consultadas.

A sobreposição de aproximadamente 80 a 100 tokens busca preservar a continuidade entre trechos consecutivos, reduzindo o risco de perda de informações relevantes durante a segmentação.

A segmentação deverá respeitar a estrutura dos documentos e considerar as limitações técnicas do modelo de embeddings BGE-M3, evitando ultrapassar seu limite de entrada e comprometer a representação dos trechos.

Esses parâmetros são valores iniciais de projeto e poderão ser ajustados durante a implementação e avaliação experimental, considerando os resultados de recuperação, a natureza dos documentos e a integridade das informações recuperadas.

## 5. Metadados previstos

Cada documento ou segmento deverá possuir metadados que permitam filtrar e contextualizar as informações recuperadas.

| Metadado | Finalidade |
|---|---|
| `document_type` | Identificar a categoria do documento, como catálogo, histórico, POP ou boletim de ocorrência. |
| `asset_type` | Identificar o tipo de ativo relacionado ao trecho. |
| `tag` | Relacionar a informação a uma TAG específica, quando aplicável. |
| `date` | Registrar a data relevante para o trecho, como data da ocorrência, elaboração ou atualização, conforme a natureza do documento. |
| `source_type` | Identificar a origem da informação: `simulada` ou `real`. |
| `source_category` | Identificar a categoria da fonte: `fabricante`, `norma`, `briefing`, `tecnica` ou `operacional`. |
| `source_name` | Identificar o nome específico do documento ou da fonte de origem. |
| `version` | Identificar a versão do documento, quando disponível. |
| `validity` | Registrar a situação de validade ou aplicabilidade da informação. |
| `intervention_type` | Identificar a modalidade de intervenção relacionada, quando aplicável. |

**Regras de preenchimento:**

- As datas deverão utilizar um formato padronizado, preferencialmente ISO 8601 quando houver data e horário.
- O significado do campo `date` deverá ser interpretado conforme a natureza do documento. Em registros de ocorrência, representa a data do evento; em documentos técnicos, representa a data de elaboração ou publicação; em documentos revisados, deverá refletir a data de atualização quando essa for a informação relevante.
- O campo `validity` deverá utilizar valores padronizados: `vigente`, `vencido`, `desconhecido` ou `nao_aplicavel`.
- A TAG deverá ser preenchida somente quando o trecho estiver relacionado a um ativo específico.
- Quando um metadado não for aplicável ou não estiver disponível, essa ausência deverá ser preservada, sem preenchimento com informações inventadas.

Os metadados deverão permitir consultas filtradas por TAG, tipo de ativo, data, tipo de documento e origem da informação, conforme solicitado no projeto.

## 6. Cuidados com privacidade e segurança da informação

A preparação da base de conhecimento deverá observar os princípios de necessidade, finalidade e segurança no tratamento das informações.

**Não deverão ser incluídos na base de conhecimento:**

- Dados pessoais de empregados, como CPF, endereço, telefone particular, documentos pessoais ou outras informações que permitam sua identificação desnecessária;
- Imagens de ocupantes de veículos ou de pessoas captadas pelas câmeras CFTV;
- Placas de veículos ou outros dados que permitam identificar pessoas, quando não forem necessários e autorizados para a finalidade do projeto;
- Dados contratuais sensíveis, informações comerciais confidenciais ou documentos restritos sem autorização;
- Senhas, credenciais, chaves de API ou outros dados de autenticação;
- Informações operacionais confidenciais que não tenham autorização para utilização no projeto.

A base deverá priorizar informações técnicas dos ativos, registros de manutenção e dados operacionais necessários à análise de ocorrências, respeitando as autorizações aplicáveis e os requisitos de proteção de dados.
