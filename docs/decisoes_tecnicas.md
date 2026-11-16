# Decisões Técnicas — PREDICTA

## 1. Objetivo

Este documento apresenta as principais decisões técnicas e arquiteturais do PREDICTA — Plataforma Inteligente de Análise e Priorização da Manutenção.

São registradas as tecnologias selecionadas, as alternativas consideradas, os critérios de comparação e as justificativas para as escolhas realizadas pelo grupo.

As decisões consideram o escopo acadêmico do projeto, o Recorte B — Operação e Priorização de Campo, os requisitos do desafio da Motiva e a necessidade de desenvolver uma solução modular, acessível e passível de evolução.

## 2. Ambiente e linguagem de desenvolvimento

### 2.1 Ambiente de desenvolvimento

**Tecnologia escolhida: Google Colab.**

O Google Colab foi selecionado como ambiente de desenvolvimento por oferecer suporte à execução de Python e facilitar a experimentação com bibliotecas de Inteligência Artificial e processamento de dados.

**Critérios considerados:**
- Facilidade de acesso e utilização.
- Suporte à linguagem Python.
- Integração com bibliotecas de IA e RAG.
- Possibilidade de executar experimentos sem configurar inicialmente um ambiente local completo.
- Adequação ao desenvolvimento acadêmico.

**Decisão:** utilizar o Google Colab durante o desenvolvimento e a experimentação do PREDICTA.

### 2.2 Linguagem de programação

**Tecnologia escolhida: Python.**

Python foi selecionado por seu ecossistema de bibliotecas para Inteligência Artificial, integração com APIs, manipulação de dados, Engenharia de Confiabilidade e desenvolvimento de interfaces.

A linguagem será utilizada na implementação da lógica da aplicação, integração das ferramentas, processamento dos dados estruturados e comunicação entre os componentes.

**Decisão:** utilizar Python como linguagem principal do projeto.

## 3. Comparação dos modelos de linguagem

Foram selecionados dois candidatos para a execução do assistente inteligente:

- Gemma 4 26B A4B IT, acessado por meio do OpenRouter.
- Nemotron 3.5 Super VL 120B A12B, acessado por meio da NVIDIA NIM.

A seleção considera a necessidade de utilizar modelos capazes de interpretar solicitações técnicas, seguir instruções, trabalhar com ferramentas e produzir respostas estruturadas.

### 3.1 Comparação técnica

| Critério | Gemma 4 26B A4B IT — OpenRouter | Nemotron 3.5 Super VL 120B A12B — NVIDIA NIM |
|---|---|---|
| Provedor considerado | OpenRouter | NVIDIA NIM |
| Custo | Rota gratuita disponível, sujeita a limites e disponibilidade | Endpoint gratuito para experimentação, sujeito aos termos e limites do serviço |
| Licença do modelo | Apache 2.0 | OpenMDW 1.1 |
| Janela de contexto considerada | 262.144 tokens | 262.144 tokens |
| Chamadas de ferramentas | Suporte a function calling na rota considerada | Suporte a chamadas de ferramentas |
| Saídas estruturadas | Aceita saída JSON, sem garantia de validação estrita por JSON Schema na rota considerada | Compatibilidade com o formato estruturado a ser validada experimentalmente |
| Integração Python | API compatível com o formato OpenAI | API compatível com o cliente Python da OpenAI |
| Português brasileiro | Desempenho a ser avaliado | Desempenho a ser avaliado |
| Privacidade | Inferência por API externa, sujeita às políticas do provedor | Inferência por API externa, sujeita às políticas da NVIDIA |
| Documentação | Model Card e documentação do OpenRouter | Model Card, documentação técnica e API Reference da NVIDIA |

Os valores de contexto e os recursos apresentados correspondem aos endpoints considerados durante o planejamento. Podem variar conforme a configuração e as condições de disponibilização dos provedores.

### 3.2 Critérios de avaliação dos modelos

Os dois modelos serão submetidos aos mesmos 14 casos de teste do Eval Set, em condições equivalentes.

A comparação deverá considerar:

1. Precisão das respostas técnicas.
2. Capacidade de identificar informações insuficientes.
3. Qualidade da classificação de prioridade.
4. Capacidade de diferenciar interferências ambientais de possíveis falhas técnicas.
5. Respeito às instruções e aos limites definidos no System Prompt.
6. Utilização correta das sete ferramentas.
7. Compatibilidade com os esquemas JSON definidos para as ferramentas.
8. Qualidade das respostas estruturadas.
9. Latência e estabilidade das chamadas.
10. Consumo de tokens e disponibilidade de utilização.

### 3.3 Decisão sobre os modelos

**Status: escolha pendente de avaliação experimental.**

Os dois modelos permanecem como candidatos. Não há definição de um modelo principal e outro alternativo, pois essa decisão dependerá dos resultados obtidos nos testes com os 14 casos do Eval Set.

A estratégia permite comparar o comportamento dos modelos em situações específicas do PREDICTA, em vez de escolher exclusivamente com base em características gerais ou informações dos fornecedores.

## 4. Comparação das bibliotecas e tecnologias

### 4.1 Orquestração: LangChain LCEL

**Tecnologia escolhida: LangChain, utilizando LCEL (LangChain Expression Language).**

O LangChain foi selecionado para organizar os fluxos de processamento e integrar o modelo de linguagem, a recuperação de informações por RAG e as ferramentas do PREDICTA.

O LCEL permite combinar componentes em sequências reutilizáveis, facilitando a organização dos fluxos de execução.

| Critério | LangChain LCEL | Implementação manual em Python |
|---|---|---|
| Organização dos fluxos | Oferece componentes e estruturas para composição de sequências | Exige implementação própria da organização dos fluxos |
| Integração com modelos | Disponibiliza integrações com diferentes provedores | Exige implementação e manutenção das integrações |
| Integração com RAG | Possui componentes específicos para recuperação de documentos | Exige implementar a recuperação e a conexão com o modelo |
| Integração com ferramentas | Oferece mecanismos de integração e execução de ferramentas | Exige implementar o controle das chamadas e dos resultados |
| Flexibilidade | Permite combinar componentes e personalizar fluxos | Oferece controle direto sobre toda a implementação |
| Complexidade | Exige compreender e configurar a estrutura da biblioteca | Pode aumentar a quantidade de código próprio e de manutenção |

**Justificativa da escolha:**

O LangChain LCEL foi selecionado por facilitar a integração entre os componentes previstos na arquitetura do PREDICTA, reduzindo a necessidade de desenvolver manualmente toda a estrutura de orquestração.

O Python continuará responsável pela lógica específica da aplicação, pelas validações e pelos cálculos de Engenharia de Confiabilidade.

### 4.2 Banco vetorial: ChromaDB versus FAISS

Foram considerados dois recursos para armazenamento e recuperação de representações vetoriais dos documentos da base de conhecimento.

| Critério | ChromaDB | FAISS |
|---|---|---|
| Custo | Gratuito e open source na modalidade local | Gratuito e open source |
| Licença | Apache 2.0 | MIT |
| Finalidade | Gerenciamento de coleções, documentos, embeddings e metadados | Indexação e busca por similaridade vetorial |
| Filtros por metadados | Suporte integrado | Exige implementação complementar |
| Persistência | Persistência local integrada | Permite salvar e carregar índices, mas exige organização complementar dos documentos e metadados |
| Integração Python | SDK próprio e integração com LangChain | Biblioteca Python e integração com LangChain |
| Processamento local | Pode operar localmente | Pode operar localmente |
| Aplicação em RAG | Oferece recursos integrados para gerenciamento e recuperação documental | Exige componentes adicionais para gerenciar documentos e metadados |

**Justificativa da escolha:**

O ChromaDB foi selecionado por oferecer uma estrutura mais integrada às necessidades do PREDICTA, especialmente no gerenciamento de documentos, embeddings, metadados, filtros e persistência.

Esses recursos facilitam a organização da base de conhecimento e a recuperação de informações relacionadas aos ativos CFTV e ITS.

O FAISS permanece como alternativa tecnicamente viável, especialmente em aplicações que priorizam a busca vetorial de alto desempenho. Entretanto, sua utilização exigiria maior implementação complementar para o gerenciamento dos documentos e metadados.

**Status: ChromaDB selecionado.**

### 4.3 Embeddings: Sentence Transformers e BAAI/bge-m3

**Tecnologia escolhida: Sentence Transformers com o modelo BAAI/bge-m3.**

O Sentence Transformers será utilizado para gerar embeddings, que são representações numéricas dos conteúdos documentais. Essas representações permitem realizar buscas por similaridade semântica na base de conhecimento.

O BAAI/bge-m3 foi selecionado como modelo de embeddings para o PREDICTA.

| Critério | Sentence Transformers com BAAI/bge-m3 |
|---|---|
| Finalidade | Geração de embeddings para recuperação semântica |
| Execução | Localmente no ambiente de desenvolvimento |
| Integração | Biblioteca Python |
| Aplicação | Transformação dos documentos e consultas em vetores |
| Integração com o banco vetorial | Armazenamento dos vetores no ChromaDB |
| Dependência de API externa | Não exige uma API externa específica para a geração dos embeddings |

**Justificativa da escolha:**

A combinação foi escolhida por permitir a geração de embeddings diretamente no ambiente do Google Colab, reduzindo a dependência de serviços externos nessa etapa.

O BAAI/bge-m3 será utilizado para representar os documentos e as consultas, enquanto o ChromaDB ficará responsável pelo armazenamento e pela recuperação dos vetores e metadados.

### 4.4 Interface: Gradio

**Tecnologia escolhida: Gradio.**

O Gradio foi selecionado para desenvolver a interface conversacional do PREDICTA.

A aplicação deverá atender às duas personas do projeto: o Operador do Centro de Controle Operacional (CCO), como usuário principal, e o Engenheiro de Manutenção, como usuário secundário.

| Critério | Gradio |
|---|---|
| Finalidade | Desenvolvimento de interfaces para aplicações de IA |
| Integração | Python |
| Interface prevista | Conversacional |
| Aplicação no PREDICTA | Interação com o assistente e acesso às funcionalidades previstas |
| Desenvolvimento | Permite estruturar interfaces sem exigir a construção de um frontend independente |

**Justificativa da escolha:**

O Gradio foi escolhido por facilitar a construção de uma interface conversacional integrada ao código Python e aos componentes de Inteligência Artificial.

As duas personas utilizarão a mesma interface, com diferentes necessidades e contextos de utilização, sem restrições de acesso por perfil previstas nesta etapa.

### 4.5 Versionamento: Git e GitHub

**Tecnologias escolhidas: Git e GitHub.**

O Git será utilizado para controle de versão dos arquivos do projeto, enquanto o GitHub será utilizado para hospedar o repositório e disponibilizar os artefatos.

| Tecnologia | Função no projeto |
|---|---|
| Git | Controle de versões, histórico de alterações e organização do desenvolvimento |
| GitHub | Hospedagem do repositório e compartilhamento dos arquivos |

**Justificativa da escolha:**

A combinação permite manter o histórico de desenvolvimento, facilitar a colaboração entre os integrantes e organizar os documentos e artefatos do PREDICTA.

## 5. Arquitetura tecnológica definida

A arquitetura planejada reúne as tecnologias selecionadas da seguinte forma:

| Camada | Tecnologia | Responsabilidade |
|---|---|---|
| Ambiente | Google Colab | Ambiente de desenvolvimento e execução |
| Linguagem | Python | Lógica da aplicação e processamento de dados |
| Modelo de linguagem | Gemma 4 ou Nemotron 3.5 Super VL | Interpretação das solicitações e geração de respostas |
| Acesso aos modelos | OpenRouter ou NVIDIA NIM | Disponibilização dos modelos por API |
| Orquestração | LangChain LCEL | Organização dos fluxos e integração dos componentes |
| Embeddings | Sentence Transformers — BAAI/bge-m3 | Conversão dos documentos e consultas em vetores |
| Banco vetorial | ChromaDB | Armazenamento e recuperação de vetores e metadados |
| Interface | Gradio | Interação conversacional com os usuários |
| Versionamento | Git e GitHub | Controle de versões e hospedagem do projeto |

## 6. Decisões sobre o processamento dos dados

Além das tecnologias, foram estabelecidas decisões relacionadas à forma como as informações serão processadas.

### 6.1 Separação entre RAG e cálculos de confiabilidade

Os cálculos de Engenharia de Confiabilidade não serão realizados diretamente sobre fragmentos textuais recuperados pelo RAG.

A arquitetura separa duas responsabilidades:

- **RAG:** recuperação de documentos e informações técnicas, operacionais e cadastrais.
- **Funções Python:** processamento de dados estruturados e validados para calcular ou analisar λ, R(t), MTBF, RGA e LDA.

Essa separação busca garantir maior consistência matemática, rastreabilidade e controle sobre os dados utilizados.

### 6.2 Tratamento de informações insuficientes

O PREDICTA não deverá inventar informações nem interpretar dados ausentes como valores iguais a zero.

Quando os registros forem insuficientes, inconsistentes ou incompatíveis, o assistente deverá informar a limitação e evitar apresentar cálculos ou conclusões sem fundamentação.

### 6.3 Utilização de dados simulados

Nesta etapa, serão utilizados dados simulados para demonstração e testes.

Esses registros deverão ser identificados como fictícios, sem atribuição de informações inventadas à operação real da Motiva.

### 6.4 Abertura de Ordens de Serviço

A abertura de Ordens de Serviço será exclusivamente simulada.

A operação dependerá de autorização humana explícita e de validação independente realizada pela aplicação. O assistente não terá autorização para executar ações reais nos sistemas operacionais da Motiva.

## 7. Trade-offs e limitações aceitas

As escolhas técnicas priorizam acessibilidade, integração entre componentes e possibilidade de evolução. Entretanto, foram reconhecidas algumas limitações:

- **Dependência de APIs externas:** os modelos de linguagem dependem da disponibilidade e das condições dos provedores.
- **Limites de utilização:** as modalidades gratuitas podem apresentar restrições de requisições, tokens e disponibilidade.
- **Dependência do Google Colab:** as sessões podem ser interrompidas ou reiniciadas, exigindo cuidados com a persistência dos arquivos.
- **Complexidade de integração:** a utilização conjunta das bibliotecas exige validação de compatibilidade e configuração.
- **Dependência da qualidade dos dados:** documentos e registros incompletos podem comprometer a recuperação de informações e os cálculos.
- **Necessidade de avaliação experimental:** o desempenho dos modelos ainda precisa ser verificado nos casos específicos do PREDICTA.

Essas limitações foram consideradas aceitáveis para o escopo acadêmico do projeto.

## 8. Resumo do status das decisões

| Decisão | Tecnologia ou alternativa | Status |
|---|---|---|
| Ambiente de desenvolvimento | Google Colab | Selecionado |
| Linguagem | Python | Selecionada |
| Orquestração | LangChain LCEL | Selecionada |
| Banco vetorial | ChromaDB | Selecionado |
| Alternativa de banco vetorial | FAISS | Avaliado |
| Embeddings | Sentence Transformers — BAAI/bge-m3 | Selecionados |
| Interface | Gradio | Selecionado |
| Versionamento | Git e GitHub | Selecionados |
| Modelo de linguagem | Gemma 4 26B A4B IT | Candidato |
| Modelo de linguagem | Nemotron 3.5 Super VL 120B A12B | Candidato |
| Modelo principal e alternativo | Definição após avaliação dos 14 casos | Pendente |
