# Sprint 1 & 2: PAI - EngMan Copilot | G4 | 1CCPB | 2026.2

## 1. Identificação do projeto e integrantes

**Nome do assistente:** PREDICTA - Plataforma Inteligente de Análise e Priorização da Manutenção.

**Integrantes:**

|Nome completo | RM | Turma | Papéis |
|---|---|---|---|
|Beatriz Lacerda Rodrigues | RM 575082 | 1CCPB| Prompt Engineer + Documentação e Riscos |
| Helaine Gonçalves Mota | RM 576838 | 1CCPB| Product Owner + Documentação e Riscos |
| Mariana Bello Auada | RM 575333 | 1CCPB| Arquiteto/TechLead + Documentação e Riscos |
| Vitória Domingues Alves de Carvalho | RM 574583 | 1CCPB | QA/Avaliação + Documentação e Riscos |

## 2. Problema abordado

Uma concessão rodoviária administra centenas de câmeras CFTV distribuídas por centenas de quilômetros, expostas continuamente a condições como poeira, fuligem de caminhões, chuva, insetos e vibração. Conforme apresentado no briefing da Motiva (Tema 2.1), essas condições podem provocar obstruções nas lentes, acúmulo de sujeira, presença de teias e ninhos e desfoque das imagens. Atualmente, a identificação de problemas que exigem limpeza ou ajuste de foco depende da percepção dos operadores do Centro de Controle Operacional (CCO), tornando a detecção reativa e dificultando a identificação oportuna de degradações visuais. Além disso, fatores como ofuscamento solar, chuva intensa e neblina podem gerar falsos positivos e ocasionar acionamentos de manutenção desnecessários.

Diante desse cenário, o projeto propõe o **PREDICTA — Plataforma Inteligente de Análise e Priorização da Manutenção**, um assistente de IA que apoia a investigação das ocorrências por meio do cruzamento de informações cadastrais, históricos de falhas, registros ambientais e procedimentos técnicos. O objetivo é auxiliar os profissionais na diferenciação entre possíveis falhas técnicas e interferências ambientais, na identificação de reincidências e na priorização dos atendimentos, contribuindo também para a preparação de Ordens de Serviço. O assistente não substitui a avaliação dos profissionais responsáveis nem apresenta hipóteses como falhas confirmadas sem evidências suficientes.

## 3. Recorte escolhido e personas

### 3.1 Recorte escolhido

**Recorte B — Operação e Priorização de Campo.**

O grupo escolheu desenvolver sua solução com base no Tema 2.1 — Saúde Visual dos Ativos ITS, escolhido no Challenge da Motiva. O tema aborda problemas que comprometem a qualidade das imagens das câmeras CFTV instaladas em campo, como lentes obstruídas, presença de teias e ninhos e desfoque, além de interferências ambientais, como chuva, neblina e ofuscamento solar, que podem gerar falsos positivos e dificultar a identificação de falhas reais.

A partir dessa escolha, o grupo definiu o Recorte B — Operação e Priorização de Campo, por sua aderência ao desafio proposto. Esse recorte permite desenvolver uma solução voltada ao apoio à triagem de alarmes e ocorrências, auxiliando na diferenciação entre falhas dos ativos e condições ambientais, bem como na priorização dos atendimentos de manutenção.

Dessa forma, o PREDICTA busca contribuir para uma análise mais criteriosa das ocorrências relacionadas aos ativos ITS, apoiando os profissionais na tomada de decisão e reduzindo acionamentos desnecessários de equipes de campo.

### 3.2 Personas atendidas

**Persona principal — Operador do Centro de Controle Operacional (CCO)**

Recebe alarmes e ocorrências em tempo real e precisa avaliar quais situações exigem acionamento da equipe de manutenção e quais podem ser monitoradas. Seu principal risco é tratar alarmes falsos como falhas reais, provocando deslocamentos desnecessários, ou deixar de encaminhar uma ocorrência que exige atenção.

O PREDICTA apoia esse profissional por meio da análise das informações disponíveis, identificando indícios de falhas técnicas, possíveis interferências ambientais ou situações inconclusivas. Quando houver dados suficientes, indica a prioridade e apresenta um encaminhamento recomendado para validação.

**Persona secundária — Engenheiro de Manutenção**

Analisa o histórico de falhas dos ativos, investiga recorrências e consulta procedimentos técnicos para apoiar decisões de manutenção. Seu principal risco é tomar decisões com base em informações incompletas ou em conclusões sem fundamentação suficiente.

O PREDICTA auxilia esse profissional na consulta de dados dos ativos, na análise de históricos e condições ambientais, na identificação de hipóteses técnicas e na avaliação de possíveis intervenções, sempre distinguindo informações registradas de hipóteses que precisam de validação.

### 3.3 Forma de utilização

As duas personas poderão utilizar a mesma interface conversacional do PREDICTA, desenvolvida em Gradio. A distinção entre os perfis está no contexto de uso e nas necessidades de cada profissional, não em uma restrição de acesso à interface.

O PREDICTA atua como ferramenta de apoio à análise e à tomada de decisão, sem substituir a avaliação dos profissionais responsáveis nem autorizar intervenções físicas nos ativos.

## 4. Escopo da solução

### 4.1 Funcionalidades previstas

O PREDICTA deverá:

1. Receber ocorrências individuais ou conjuntos de alarmes relacionados aos ativos CFTV e ITS contemplados no projeto.
2. Consultar os dados cadastrais e técnicos dos ativos por meio de suas TAGs.
3. Consultar o histórico de falhas e identificar possíveis reincidências e padrões de ocorrência.
4. Consultar registros de condições ambientais próximos ao horário da ocorrência.
5. Consultar procedimentos técnicos e demais informações documentadas aplicáveis ao ativo e à intervenção.
6. Analisar as informações disponíveis, identificando possíveis causas e distinguindo evidências confirmadas de hipóteses.
7. Recomendar prioridades de atendimento considerando, quando disponíveis, a criticidade cadastrada do ativo, a gravidade da ocorrência, a reincidência e o tempo de indisponibilidade. Quando os dados forem insuficientes, deverá explicitar essa limitação e solicitar validação.
8. Apoiar a escolha da modalidade de intervenção mais adequada: corretiva, preventiva, inspeção ou manutenção baseada na condição (CBM), considerando as evidências disponíveis e os procedimentos documentados.
9. Preparar descrições e resumos técnicos para subsidiar a elaboração de Ordens de Serviço (OS).
10. Permitir a abertura de OS exclusivamente simulada, condicionada à autorização humana explícita e à validação dessa autorização pela aplicação.

### 4.2 Limites de atuação

O PREDICTA não deverá:

1. Inventar informações sobre ativos, TAGs, históricos, procedimentos, condições ambientais ou indicadores de confiabilidade.
2. Apresentar diagnósticos definitivos quando as evidências disponíveis forem insuficientes.
3. Executar intervenções físicas ou substituir a avaliação dos profissionais responsáveis.
4. Liberar, bloquear ou comandar equipamentos.
5. Substituir normas regulamentadoras, treinamentos ou procedimentos de segurança.
6. Emitir laudos, Anotações de Responsabilidade Técnica (ARTs) ou pareceres legais.
7. Tratar dados pessoais ou informações confidenciais sem necessidade e autorização adequadas.
8. Omitir limitações ou deixar de solicitar validação profissional quando os dados forem insuficientes, inconsistentes ou conflitantes.
9. Realizar abertura de Ordens de Serviço reais ou executar ações diretamente nos sistemas operacionais da Motiva.

## 5. Arquitetura e funcionamento da solução

### 5.1 Fluxo operacional

1. **Recebimento:** o usuário informa a ocorrência, os alarmes e a TAG do ativo, quando disponível.
2. **Validação:** o sistema verifica se a identificação do ativo é suficiente.
3. **Consulta cadastral:** a ferramenta `consultar_ativo` recupera os dados do equipamento.
4. **Investigação:** conforme a necessidade, o assistente consulta o histórico de falhas, as condições ambientais, os procedimentos e as métricas de confiabilidade.
5. **Análise:** as informações são cruzadas para identificar causas prováveis, limitações e evidências.
6. **Priorização:** a ocorrência é analisada considerando criticidade, gravidade, reincidência e tempo de indisponibilidade.
7. **Resposta:** o assistente apresenta a análise da ocorrência, as evidências consultadas, as hipóteses identificadas, a prioridade recomendada, as limitações dos dados e o encaminhamento sugerido.

As ferramentas são acionadas de forma condicional, conforme a necessidade da ocorrência. O assistente não precisa executar todas as consultas em todos os atendimentos.

### 5.2 Integração com métricas de confiabilidade

O PREDICTA prevê a utilização de métodos e métricas de Engenharia de Confiabilidade para complementar a análise histórica dos ativos CFTV e apoiar decisões de manutenção.

A ferramenta `calcular_metricas_confiabilidade` será responsável por realizar os cálculos e análises compatíveis com os dados históricos e operacionais disponíveis, contemplando:

- **Taxa de falhas (λ):** calculada pela relação entre o número de falhas registradas e o tempo total válido de operação, considerando o mesmo conjunto de ativos e período de observação. O resultado deverá apresentar a unidade utilizada e as limitações dos dados. Quando não houver falhas registradas, o sistema deverá informar que não foram observadas falhas no período analisado, sem interpretar esse resultado como uma taxa de falhas real igual a zero ou como confiabilidade perfeita.

- **Confiabilidade R(t):** estimada pelo modelo exponencial \(R(t)=e^{-\lambda t}\), conforme previsto no briefing para equipamentos eletroeletrônicos, considerando a hipótese de taxa de falhas constante. Seu cálculo exige uma taxa de falhas válida e um tempo de missão informado, com unidades compatíveis. Quando o tempo de missão não for fornecido ou os dados forem insuficientes, o sistema deverá indicar que o cálculo não foi realizado e explicitar a informação necessária.

- **MTBF (Mean Time Between Failures):** utilizado como métrica complementar, representa o tempo médio entre falhas e exige registros válidos de falhas e exposição operacional correspondentes ao mesmo conjunto de ativos e período. Seu cálculo deverá respeitar a consistência dos dados disponíveis. A ausência de falhas registradas não deverá ser interpretada como MTBF infinito.

- **RGA (Reliability Growth Analysis):** método de análise da evolução da confiabilidade ao longo do tempo, utilizado para avaliar possíveis melhorias no desempenho dos ativos após intervenções ou modificações. Sua aplicação exige histórico cronológico de falhas, exposição operacional comparável e registros das intervenções realizadas. A existência de dados não comprova, por si só, crescimento da confiabilidade; essa conclusão dependerá dos resultados da análise.

- **LDA (Life Data Analysis):** método de análise de dados de vida dos componentes, utilizado para investigar padrões de falhas e estimar características de durabilidade. Sua aplicação exige dados individuais de tempo até a falha ou observações censuradas, identificação dos componentes e informações suficientes para selecionar uma distribuição e um método de estimação adequados. Quando os dados não permitirem uma análise fundamentada, o sistema deverá informar a insuficiência.

Os resultados dessas métricas e análises serão utilizados como informações complementares à avaliação de criticidade, reincidência, gravidade e indisponibilidade dos ativos. Dessa forma, poderão apoiar a identificação de tendências, a avaliação de intervenções anteriores e a escolha entre manutenção preventiva, corretiva, inspeção ou manutenção baseada na condição (CBM).

As análises deverão respeitar a disponibilidade, a consistência e a qualidade dos dados. Os períodos de falha e de exposição operacional deverão ser compatíveis, e informações ausentes não poderão ser interpretadas como valores iguais a zero. Quando não houver dados suficientes, o assistente deverá informar a limitação e não apresentar cálculos, estimativas ou conclusões sem fundamentação.

Os resultados não serão tratados como garantias de comportamento futuro nem substituirão a avaliação dos profissionais responsáveis.

### 5.3 Fluxograma

O fluxo completo da arquitetura está disponível no Miro:

[**Fluxograma PREDICTA — Miro**](https://miro.com/app/board/uXjVEOQoQP8=/?share_link_id=216098199104)

### 5.4 Wireframe da interface

O wireframe apresenta a proposta visual da interface conversacional do PREDICTA, desenvolvida com Gradio, considerando as necessidades das duas personas atendidas pelo projeto: o Operador do Centro de Controle Operacional (CCO) e o Engenheiro de Manutenção.

A interface foi planejada para centralizar a interação com o assistente em um ambiente conversacional, facilitando o acesso às funcionalidades previstas no escopo da solução.

O wireframe representa uma proposta de interface e não uma aplicação funcional. Sua implementação será realizada posteriormente, durante a etapa de desenvolvimento.

**Protótipo visual:** [Wireframe PREDICTA — Figma](https://www.figma.com/community/file/1703831255078875482/wireframe-predicta-sprint-1-2-2026-2-pai).

## 6. Stack tecnológico e justificativa técnica

A arquitetura foi planejada para execução no Google Colab, priorizando ferramentas gratuitas ou com modalidades gratuitas de uso, integração por API e possibilidade de evolução. A utilização desses serviços está sujeita aos limites, à disponibilidade e às condições estabelecidas por cada provedor.

| Camada | Tecnologia escolhida | Justificativa |
|---|---|---|
| Ambiente | Google Colab | Ambiente acessível para desenvolvimento e experimentação em Python. |
| Linguagem | Python | Ecossistema amplo para integração com IA, RAG e ferramentas. |
| Modelos de linguagem candidatos | Gemma 4 26B A4B IT (OpenRouter) e Nemotron 3.5 Super VL 120B A12B (NVIDIA NIM) | Dois candidatos mantidos para avaliação experimental. A escolha do modelo principal e do alternativo será realizada posteriormente, após a execução dos testes com os 14 casos do Eval Set. |
| Orquestração | LangChain (LCEL) | Organização dos fluxos de processamento e integração entre o modelo de linguagem, a recuperação de informações por RAG e as ferramentas do PREDICTA. O LCEL permite combinar componentes em sequências reutilizáveis, enquanto o Python permanece responsável pela lógica geral da aplicação. |
| Banco vetorial | ChromaDB | Armazenamento e recuperação de documentos com metadados. |
| Embeddings | Sentence Transformers — BAAI/bge-m3 | Geração de embeddings no ambiente do Google Colab, reduzindo a dependência de serviços externos para essa etapa. |
| Interface | Gradio | Interface conversacional única para interação dos usuários com o PREDICTA. |
| Versionamento | Git e GitHub | Organização, rastreabilidade e disponibilização pública dos artefatos. |

### 6.1 Comparação de modelos de linguagem

Os modelos Gemma 4 26B A4B IT, disponibilizado pelo OpenRouter, e Nemotron 3.5 Super VL 120B A12B, disponibilizado pela NVIDIA NIM, foram selecionados como candidatos à avaliação experimental.

Ambos serão avaliados utilizando os mesmos 14 casos do Eval Set, com condições de teste equivalentes e critérios padronizados. A escolha do modelo principal e do alternativo será realizada posteriormente, durante a etapa de implementação e testes, após a comparação dos resultados obtidos.

| Critério | Gemma 4 26B A4B IT (OpenRouter) | Nemotron 3.5 Super VL 120B A12B (NVIDIA NIM) |
|---|---|---|
| Custo | Rota gratuita disponível, sujeita a limites de utilização e disponibilidade do provedor. | Endpoint gratuito para experimentação, sujeito aos termos e limites do serviço de teste da NVIDIA. |
| Licença do modelo | Apache 2.0. | OpenMDW 1.1. |
| Janela de contexto no endpoint considerado | 262.144 tokens. | 262.144 tokens. |
| Chamadas de ferramentas | Suporte a function calling na rota gratuita. | Suporte a chamadas de ferramentas. |
| Saídas estruturadas | Aceita saída JSON, sem garantia de validação estrita por JSON Schema na rota gratuita. | Compatibilidade com o formato estruturado exigido pelo projeto a ser validada experimentalmente. |
| Qualidade em português brasileiro | Desempenho a ser avaliado nos casos do Eval Set. | Desempenho a ser avaliado nos casos do Eval Set. |
| Integração Python | API compatível com o formato OpenAI. | API compatível com o cliente Python da OpenAI. |
| Privacidade e processamento | Inferência por API externa; tratamento de dados sujeito às políticas e aos termos do provedor. | Inferência por API externa; tratamento de dados sujeito às políticas e aos termos da NVIDIA. |
| Maturidade e documentação | Documentação oficial do modelo e da API do OpenRouter. | Model Card, documentação técnica e API Reference da NVIDIA. |

Os valores apresentados para a janela de contexto correspondem aos endpoints considerados na comparação. Os limites podem variar conforme o provedor, a configuração e a modalidade de implantação.

**Critérios de avaliação experimental:**

- Precisão das respostas técnicas;
- Capacidade de identificar dados insuficientes;
- Qualidade da classificação de prioridade;
- Capacidade de diferenciar condições ambientais de falhas técnicas;
- Respeito às restrições do System Prompt;
- Uso correto das sete ferramentas;
- Compatibilidade com os esquemas JSON definidos para as ferramentas;
- Qualidade das respostas estruturadas;
- Latência e estabilidade;
- Consumo de tokens e disponibilidade de uso gratuito.

**Decisão:** os dois modelos permanecem como candidatos. A definição do modelo principal e do alternativo dependerá dos resultados obtidos durante a execução dos testes com os 14 casos do Eval Set.

### 6.2 Comparação de bancos vetoriais

| Critério | ChromaDB | FAISS |
|---|---|---|
| Custo | Gratuito e open source na modalidade local. | Gratuito e open source. |
| Licença | Apache 2.0. | MIT. |
| Finalidade | Banco vetorial que gerencia coleções, documentos, embeddings e metadados. | Biblioteca especializada em indexação e busca por similaridade vetorial. |
| Filtros por metadados | Suporte integrado a filtros por metadados e conteúdo dos documentos. | Exige implementação complementar para associar metadados e realizar filtros por atributos. |
| Persistência | Suporta persistência local integrada, permitindo salvar e recuperar coleções. | Permite salvar e carregar índices, mas a aplicação precisa organizar separadamente os documentos e metadados associados. |
| Integração Python | SDK próprio e integração com LangChain. | Biblioteca Python e integração com LangChain. |
| Privacidade e processamento local | Pode operar localmente, mantendo os dados no ambiente de execução. | Pode operar localmente, mantendo os índices no ambiente de execução. |
| Maturidade e documentação | Documentação oficial, exemplos e recursos voltados a aplicações RAG. | Biblioteca consolidada, com documentação técnica e foco em busca vetorial de alto desempenho. |

**Escolha: ChromaDB**

O ChromaDB foi selecionado por oferecer uma estrutura mais integrada às necessidades do PREDICTA, especialmente pelo gerenciamento de documentos, embeddings, metadados, filtros e persistência. Esses recursos facilitam a organização da base de conhecimento e a recuperação de informações relacionadas aos ativos CFTV.

O FAISS permanece como alternativa tecnicamente viável, especialmente para aplicações que priorizam busca vetorial de alto desempenho. Entretanto, exige maior implementação complementar para o gerenciamento de documentos e metadados, tornando o ChromaDB mais adequado à arquitetura planejada para o projeto.

### 6.3 Trade-offs aceitos

A arquitetura prioriza facilidade de desenvolvimento, integração entre componentes e utilização de recursos gratuitos ou com modalidades gratuitas de uso. Entretanto, algumas limitações são aceitas:

- **Dependência de provedores externos:** a inferência dos modelos de linguagem será realizada por APIs externas, ficando sujeita à disponibilidade, latência e condições de uso dos provedores.
- **Limites de utilização:** as modalidades gratuitas podem apresentar restrições de requisições, tokens e disponibilidade, podendo exigir ajustes durante os testes e a implementação.
- **Dependência do ambiente de execução:** o Google Colab oferece praticidade para desenvolvimento, mas suas sessões podem ser interrompidas ou reiniciadas, exigindo cuidados com a persistência dos arquivos e dos dados.
- **Complexidade de integração:** a utilização conjunta de LangChain, ChromaDB, Sentence Transformers e ferramentas exige validação de compatibilidade e configuração durante a implementação.
- **Contingência entre provedores:** a avaliação de dois provedores distintos permite considerar uma estratégia de alternância em caso de indisponibilidade. Entretanto, sua implementação dependerá dos resultados dos testes e da compatibilidade das APIs.

Esses trade-offs foram considerados aceitáveis para o escopo acadêmico do PREDICTA, priorizando uma arquitetura acessível, modular e passível de evolução. A disponibilidade de serviços gratuitos e a viabilidade das integrações deverão ser verificadas durante a implementação.

## 7. Base de conhecimento

A base de conhecimento do PREDICTA foi planejada para fornecer informações técnicas, operacionais e cadastrais necessárias às análises dos ativos CFTV e ITS, por meio de recuperação aumentada por geração (RAG).

O inventário contempla dez categorias documentais:

1. Inventário de ativos CFTV e ITS.
2. Plano de manutenção preventiva.
3. Histórico de falhas dos ativos.
4. Registros de exposição operacional e horas de funcionamento.
5. Procedimentos Operacionais Padrão (POPs).
6. Fichas técnicas dos equipamentos.
7. Matriz de criticidade.
8. Glossário técnico.
9. Normas, requisitos de segurança e documentos do briefing da Motiva.
10. Relatórios de campo.

Os documentos simulados serão identificados como fictícios, sem atribuição de dados inventados à Motiva. As informações reais e simuladas serão diferenciadas por meio de metadados, permitindo identificar a origem e a natureza dos registros.

A estratégia de preparação documental prevê:

- Divisão dos documentos em blocos de aproximadamente 500 a 800 tokens.
- Sobreposição de aproximadamente 80 a 100 tokens entre blocos consecutivos.
- Preservação de títulos, subtítulos e do contexto das informações.
- Utilização de metadados como tipo documental, tipo de ativo, TAG, data, origem, versão, validade e tipo de intervenção, quando aplicáveis.
- Preservação da rastreabilidade das informações, permitindo identificar o documento de origem dos conteúdos recuperados.

O modelo de embeddings selecionado é o BAAI/bge-m3, executado no ambiente do Google Colab por meio da biblioteca Sentence Transformers, sem necessidade de contratar um serviço externo específico para a geração de embeddings.

O ChromaDB será utilizado para armazenar os vetores e metadados, permitindo recuperar documentos e trechos relevantes conforme o contexto de cada consulta.

**Tratamento dos dados para cálculos de confiabilidade:**

Os cálculos de Engenharia de Confiabilidade não serão realizados diretamente sobre fragmentos textuais recuperados pelo RAG. Para essa finalidade, o PREDICTA utilizará dados estruturados e validados, processados por funções Python específicas.

Essas funções serão responsáveis por calcular ou analisar λ, R(t), MTBF, RGA e LDA, respeitando os requisitos de cada método, a consistência dos períodos de observação e a disponibilidade dos registros de falhas e exposição operacional. Quando os dados forem insuficientes, o sistema deverá informar a limitação, sem gerar estimativas sem fundamentação.

Dessa forma, a arquitetura separa a recuperação de informações documentais, realizada pelo RAG, do processamento matemático dos dados estruturados, garantindo maior consistência e rastreabilidade nas análises.

**Artefato:** [Inventário da base de conhecimento](data/knowledge_base/inventario.md).

## 8. System Prompt

O System Prompt define a identidade, o objetivo, o escopo, as regras de atuação, o formato das respostas, o tom de comunicação e os limites do PREDICTA.

Foi estruturado em sete blocos:

- **PAPEL:** define a identidade do PREDICTA, seu contexto de atuação e os profissionais atendidos.
- **OBJETIVO:** estabelece os resultados esperados e as contribuições da solução para a operação e a priorização da manutenção.
- **ESCOPO:** delimita os ativos contemplados, as atividades permitidas e as situações que estão fora do campo de atuação do assistente.
- **REGRAS:** estabelece diretrizes para análise técnica, prevenção de alucinações, utilização das ferramentas, tratamento de divergências entre fontes e respeito aos limites de atuação.
- **FORMATO:** padroniza a organização das respostas e contempla exemplos few-shot para classificação de prioridade e análise estruturada de falhas intermitentes.
- **TOM:** define a linguagem técnica, objetiva e profissional, adequada ao contexto operacional e de Engenharia de Manutenção.
- **BORDA:** estabelece o comportamento do assistente em situações de saudação, dúvidas ambíguas, ausência de dados, encerramento de conversas e solicitações fora do escopo.

O System Prompt também contempla:

- **Few-shot:** exemplos de entrada e saída para orientar a classificação de ocorrências em diferentes níveis de prioridade.
- **Análise estruturada de falhas intermitentes:** sequência sistemática para investigar ocorrências, correlacionando histórico, condições ambientais e informações técnicas, sem apresentar hipóteses como causas confirmadas.
- **Tratamento de divergências entre fontes:** critérios para identificar conflitos, avaliar a confiabilidade das informações e solicitar validação profissional quando necessário.
- **Prevenção de alucinações:** regras para impedir a invenção de dados, diagnósticos e informações técnicas.
- **Proteção contra prompt injection:** instruções para desconsiderar tentativas de modificar as regras e os limites definidos para o assistente.
- **Frase padrão de recusa:** resposta padronizada para solicitações fora do escopo do PREDICTA.
- **Controle de Ordens de Serviço:** restrição à abertura simulada de OS, condicionada à autorização humana explícita e à validação pela aplicação.

**Artefato:** [System Prompt do PREDICTA](prompts/system_prompt.md).

## 9. Eval Set

O conjunto de avaliação contém 14 casos estruturados para verificar o comportamento esperado do assistente em diferentes situações.

Os testes abrangem:

- Triagem e diagnóstico.
- Priorização de ocorrências.
- Interpretação de condições ambientais.
- Histórico e confiabilidade.
- Dados insuficientes.
- Jailbreak e manipulação.
- Riscos operacionais.
- Privacidade e LGPD.

Cada caso contém os campos definidos pelo enunciado: identificação, categoria, entrada do usuário, contexto esperado, resposta ideal, critérios de avaliação e indicação de recusa.

O Eval Set está documentado, mas sua execução experimental contra os modelos será realizada posteriormente.

**Artefato:** [Eval Set — 14 casos de teste](evals/sprint1_eval_set.json).

## 10. Tools especificadas

O PREDICTA possui sete ferramentas planejadas para apoiar as consultas, análises e operações previstas no escopo do projeto.

| Ferramenta | Função |
|---|---|
| `consultar_ativo` | Consulta os dados cadastrais e técnicos de um ativo CFTV ou ITS por meio de sua TAG. |
| `consultar_historico_falhas` | Consulta ocorrências anteriores, permitindo identificar possíveis reincidências e padrões de falhas. |
| `consultar_condicoes_ambientais` | Recupera registros de condições ambientais próximos ao horário da ocorrência, considerando uma janela padrão de 30 minutos antes e depois. |
| `consultar_procedimento` | Consulta procedimentos técnicos e orientações documentadas aplicáveis ao ativo e ao tipo de intervenção. |
| `calcular_metricas_confiabilidade` | Calcula indicadores de confiabilidade, como λ, R(t), RGA e LDA, utilizando o MTBF como métrica complementar, desde que existam dados suficientes. |
| `listar_ativos_por_criticidade` | Organiza e consulta ativos conforme os critérios de criticidade cadastrados, permitindo apoiar a priorização de atendimentos. |
| `abrir_ordem_servico` | Prepara e realiza a abertura exclusivamente simulada de uma OS, condicionada à autorização humana explícita e à validação dessa autorização pela aplicação. |

As ferramentas foram especificadas em JSON Schema, com definição dos parâmetros de entrada, tipos de dados, campos obrigatórios, restrições, enums e comportamentos previstos para situações de erro ou ausência de informações.

As respostas das ferramentas seguem estruturas definidas durante a implementação, sem exigência de schemas JSON de saída nesta especificação.

A utilização das ferramentas deve respeitar as regras do System Prompt, especialmente quanto à disponibilidade dos dados, à rastreabilidade das informações e à necessidade de validação humana para operações que envolvam Ordens de Serviço.

**Artefato:** [Especificação das sete Tools](tools/tools_spec.json).

## 11. Riscos e mitigações

O projeto contempla o mapeamento de onze riscos relacionados ao uso de Inteligência Artificial no contexto operacional e de Engenharia de Manutenção:

1. **Alucinação e informações não fundamentadas:** possibilidade de o assistente gerar informações incorretas, inventar dados ou apresentar conclusões sem evidências suficientes.
2. **Prompt injection e manipulação do assistente:** tentativas de modificar as instruções, contornar as regras estabelecidas ou induzir o sistema a executar ações indevidas.
3. **Riscos operacionais e de segurança:** possibilidade de recomendações inadequadas comprometerem a operação dos ativos ou a segurança dos profissionais.
4. **Viés na priorização de ocorrências:** risco de classificação inadequada das prioridades devido a critérios incompletos, dados enviesados ou informações inconsistentes.
5. **Exposição de dados pessoais e riscos à LGPD:** tratamento inadequado de dados pessoais, imagens de pessoas ou informações que permitam sua identificação.
6. **Exposição de informações operacionais confidenciais:** acesso, utilização ou divulgação indevida de informações internas e dados sensíveis da operação.
7. **Excesso de confiança nas respostas da IA:** possibilidade de usuários interpretarem hipóteses ou recomendações do assistente como diagnósticos definitivos.
8. **Perda ou extrapolação indevida de contexto:** risco de o assistente deixar de considerar informações relevantes ou utilizar informações anteriores de maneira inadequada durante a conversa.
9. **Interpretação ambiental equivocada:** possibilidade de confundir interferências ambientais, como chuva, neblina e ofuscamento solar, com falhas técnicas dos equipamentos, ou vice-versa.
10. **Dados incompletos, inconsistentes ou desatualizados:** informações insuficientes ou divergentes podem comprometer as análises, os cálculos de confiabilidade e as recomendações.
11. **Ação operacional não autorizada:** possibilidade de execução de operações sem a autorização humana exigida, especialmente no fluxo de abertura simulada de Ordens de Serviço.

Para cada risco foram definidos descrição, possíveis impactos, medidas concretas de mitigação e rastreabilidade nos artefatos do projeto.

Entre as principais medidas adotadas estão a supervisão humana, a prevenção de informações não fundamentadas, a identificação explícita de incertezas, a consulta a procedimentos documentados, a minimização de dados, a proteção de informações confidenciais e a validação da autorização antes da abertura simulada de Ordens de Serviço.

O projeto considera a Lei nº 13.709/2018 — Lei Geral de Proteção de Dados Pessoais (LGPD), adotando princípios de necessidade, finalidade e proteção dos dados tratados.

**Artefato:** [Riscos, Ética e LGPD](docs/riscos_lgpd.md).

## 12. Limitações conhecidas

O PREDICTA depende da qualidade, disponibilidade e atualização dos documentos e registros utilizados pela base de conhecimento. Informações ausentes, inconsistentes ou desatualizadas podem limitar a precisão das análises e das recomendações apresentadas.

A interpretação de condições ambientais depende da existência de registros próximos ao horário da ocorrência. A ausência desses registros não significa que as condições ambientais estavam normais, devendo essa limitação ser explicitada pelo assistente.

Os cálculos e as análises de Engenharia de Confiabilidade dependem da disponibilidade, consistência e validade dos dados estruturados de falhas e exposição operacional. A ausência de informações suficientes pode impedir a realização de determinados cálculos ou comprometer a fundamentação dos resultados.

A qualidade das respostas também depende do modelo de linguagem utilizado, dos limites de contexto, da disponibilidade das APIs e da correta configuração das ferramentas. Indisponibilidades ou limitações desses componentes podem afetar o funcionamento da aplicação.

Nesta etapa, o projeto possui caráter acadêmico e documental, com utilização de dados simulados para demonstração e testes. Não existe integração operacional com sistemas reais da Motiva, execução de intervenções físicas ou abertura de Ordens de Serviço reais. As Ordens de Serviço previstas no projeto são exclusivamente simuladas, mediante autorização humana explícita e validação pela aplicação.

A aplicação em ambiente real exigiria validação técnica, operacional, institucional e de segurança da informação, além de avaliação da qualidade dos dados, integração com os sistemas existentes e autorização dos responsáveis..

## 13. Referências

AGÊNCIA NACIONAL DE TRANSPORTES TERRESTRES (ANTT). *Resolução nº 6.000, de 2022*. Brasília, DF: ANTT, 2022. Disponível em: https://anttlegis.antt.gov.br/action/ActionDatalegis.php?acao=abrirTextoAto&cod_menu=7796&cod_modulo=161&link=S&numeroAto=00006000&orgao=DG%2FANTT%2FMI&seqAto=000&tipo=RES&valorAno=2022. Acesso em: 9 nov. 2026.

AGÊNCIA NACIONAL DE TRANSPORTES TERRESTRES (ANTT). *PER atualizado — contrato reestruturado: Motiva Minas-SP*. Brasília, DF: ANTT, [s. d.]. Disponível em: https://www.gov.br/antt/pt-br/assuntos/rodovias/concessionarias/lista-de-concessoes/motiva-minas-sp/documentos-de-gestao/contrato-e-anexos/anexos-do-contrato/per-atualizado-contrato-reestruturado.pdf. Acesso em: 10 nov. 2026.

AXIS COMMUNICATIONS. *AXIS Q1635: user manual*. Lund: Axis Communications, [s. d.]. Disponível em: https://www.axis.com/dam/public/c7/78/d5/axis-q1635--user-manual-en-US-103962.pdf. Acesso em: 9 nov. 2026.

AXIS COMMUNICATIONS. *Troubleshooting image quality*. Lund: Axis Communications, [s. d.]. Disponível em: https://help.axis.com/en-us/troubleshooting-image-quality. Acesso em: 10 nov. 2026.

CCR. *Relatório integrado 2023 (RAI)*. [S. l.]: CCR, 2024. Disponível em: https://rodovias.motiva.com.br/content/dam/sites-modulares/pt/media/documentos/esg/nossas-praticas/relatorios-de-sustentabilidade/Relatorio%20Integrado%202023%20%28RAI%29%20-%20CCR.pdf. Acesso em: 10 nov. 2026.

GOOGLE. *Gemma 4: model card*. Google AI for Developers, [s. d.]. Disponível em: https://ai.google.dev/gemma/docs/core/model_card_4?hl=pt-br. Acesso em: 9 nov. 2026.

INSTITUTO NACIONAL DE METEOROLOGIA (INMET). *BDMEP: dados históricos*. Brasília, DF: INMET, [s. d.]. Disponível em: https://portal.inmet.gov.br/servicos/bdmep-dados-historicos. Acesso em: 13 nov. 2026.

INTELBRAS. *CFTV: saiba tudo sobre esse sistema*. [S. l.]: Intelbras, [s. d.]. Disponível em: https://www.intelbras.com/pt-br/blog/cftv-saiba-tudo-sobre-esse-sistema/. Acesso em: 10 nov. 2026.

MICROSOFT. *Network cameras*. Microsoft Learn, [s. d.]. Disponível em: https://learn.microsoft.com/en-us/windows-hardware/drivers/stream/network-cameras. Acesso em: 12 nov. 2026.

MINISTÉRIO DO TRABALHO E EMPREGO (Brasil). *Norma Regulamentadora nº 35 (NR-35): trabalho em altura*. Brasília, DF: Ministério do Trabalho e Emprego, [s. d.]. Disponível em: https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/participacao-social/conselhos-e-orgaos-colegiados/comissao-tripartite-partitaria-permanente/normas-regulamentadora/normas-regulamentadoras-vigentes/norma-regulamentadora-no-35-nr-35. Acesso em: 12 nov. 2026.

MINISTÉRIO DO TRABALHO E EMPREGO (Brasil). *Norma Regulamentadora nº 35 (NR-35): versão atualizada 2025*. Brasília, DF: Ministério do Trabalho e Emprego, 2025. Disponível em: https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/participacao-social/conselhos-e-orgaos-colegiados/comissao-tripartite-partitaria-permanente/normas-regulamentadora/normas-regulamentadoras-vigentes/nr-35-atualizada-2025.pdf. Acesso em: 12 nov. 2026.

MOTIVA. *Carta de serviços ao usuário: AutoBAn*. [S. l.]: Motiva, 2026. Disponível em: https://rodovias.motiva.com.br/content/dam/conteudo-multicanal/rodovias/conteudo/pt/midia/autoban/carta-aos-usuarios/CARTA%20DE%20SERVI%C3%87OS%20AO%20USU%C3%81RIO%20-%20Atualizada_jan_2026.pdf. Acesso em: 11 nov. 2026.

MOTIVA. *Documentos técnicos*. [S. l.]: Motiva, [s. d.]. Disponível em: https://rodovias.motiva.com.br/documentos-tecnicos/. Acesso em: 11 nov. 2026.

MOTIVA. *Nossas práticas de ESG*. [S. l.]: Motiva, [s. d.]. Disponível em: https://www.motiva.com.br/esg/nossas-praticas/. Acesso em: 11 nov. 2026.

MOTIVA. *Sobre a Motiva*. [S. l.]: Motiva, [s. d.]. Disponível em: https://rodovias.motiva.com.br/. Acesso em: 9 nov. 2026.

MOTIVA. *Sobre a Motiva Paraná*. [S. l.]: Motiva, [s. d.]. Disponível em: https://rodovias.motiva.com.br/parana/sobre/sobre-parana/. Acesso em: 11 nov. 2026.

MOTIVA. *Sobre a RIOSP*. [S. l.]: Motiva, [s. d.]. Disponível em: https://rodovias.motiva.com.br/riosp/sobre/sobre-riosp/. Acesso em: 11 nov. 2026.

MOTIVA PARANÁ. *Carta de serviços*. [S. l.]: Motiva Paraná, [s. d.]. Disponível em: https://rodovias.motiva.com.br/content/dam/conteudo-multicanal/rodovias/conteudo/pt/midia/prvias/carta-aos-usuarios/Carta%20de%20Servi%C3%A7os%20Motiva%20Paran%C3%A1%202.pdf. Acesso em: 11 nov. 2026.

NVIDIA. *Nemotron 3.5 Super VL 120B A12B*. NVIDIA NIM, 2026. Disponível em: https://build.nvidia.com/nvidia/nemotron-3.5-super-vl-120b-a12b. Acesso em: 13 nov. 2026.

NVIDIA. *NVIDIA NIM for large language models: API reference*. NVIDIA Documentation, [s. d.]. Disponível em: https://docs.nvidia.com/nim/large-language-models/latest/reference/api-reference.html. Acesso em: 13 nov. 2026.

OPENROUTER. *Gemma 4 26B A4B IT*. OpenRouter, [s. d.]. Disponível em: https://openrouter.ai/google/gemma-4-26b-a4b-it. Acesso em: 13 nov. 2026.

OPENROUTER. *Terms of service*. OpenRouter, 2026. Disponível em: https://openrouter.ai/terms. Acesso em: 13 nov. 2026.

NETWORK OPTIX. *Troubleshoot ONVIF camera issues*. Nx Support, 2026. Disponível em: https://support.networkoptix.com/hc/en-us/articles/216517857-Troubleshoot-ONVIF-camera-issues. Acesso em: 11 nov. 2026.

VELSIS. *PMV: painel de mensagem variável fixo ou móvel*. [S. l.]: Velsis, [s. d.]. Disponível em: https://velsis.com.br/pmv-painel-de-mensagem-variavel-fixo-ou-movel/. Acesso em: 11 nov. 2026.
