# PREDICTA — Riscos, Ética e LGPD

## 1. Objetivo

Este documento apresenta os principais riscos associados ao uso do PREDICTA no apoio à triagem, análise e priorização de ocorrências relacionadas aos ativos CFTV e ITS. Para cada risco, são descritos os possíveis impactos, as medidas de mitigação e os artefatos do projeto nos quais essas medidas são implementadas.

O PREDICTA é um sistema de apoio à decisão. Suas análises e recomendações não substituem a avaliação, a autorização ou a responsabilidade dos profissionais competentes.

## 2. Mapeamento de riscos

### Risco 1 — Alucinação ou geração de informações não fundamentadas

**Descrição:**

O PREDICTA pode apresentar informações incorretas, afirmar uma causa sem evidências suficientes ou gerar dados inexistentes sobre equipamentos, TAGs, históricos de falhas, procedimentos ou indicadores de confiabilidade.

**Impactos possíveis:**

- **Segurança:** uma falha real pode não receber a atenção necessária ou pode ser tratada de maneira inadequada.
- **Financeiro:** podem ocorrer manutenções desnecessárias, retrabalho ou agravamento de uma falha não identificada corretamente.
- **Legal:** decisões técnicas fundamentadas em informações incorretas podem gerar consequências operacionais e responsabilidades.
- **Reputacional:** erros recorrentes podem reduzir a confiança dos profissionais no assistente.

**Mitigações:**

1. Fundamentar as análises nas informações fornecidas pelo usuário, na base de conhecimento e nos retornos das ferramentas disponíveis.
2. Diferenciar fatos registrados, hipóteses técnicas e informações que não estão disponíveis.
3. Quando os dados forem insuficientes, informar que a conclusão é inconclusiva e solicitar os complementos necessários.
4. Não inventar TAGs, características de ativos, históricos, procedimentos, métricas ou resultados de consultas.
5. Recomendar avaliação por profissional responsável quando as evidências não permitirem uma conclusão segura.
6. Identificar claramente dados simulados, evitando apresentá-los como registros reais da Motiva.

**Rastreabilidade:**

- **System Prompt:** blocos REGRAS, ESCOPO e BORDA.
- **Fluxograma:** verificação da existência e suficiência dos dados antes da análise e da priorização.
- **Eval Set:** EVAL-001, EVAL-002, EVAL-006 e EVAL-008.
- **Base de conhecimento:** identificação da origem, versão e validade das informações utilizadas.
- **Tools:** tratamento de dados ausentes, ativos não encontrados e falhas nas consultas.

### Risco 2 — Prompt Injection e manipulação do assistente

**Descrição:**

O PREDICTA pode receber instruções maliciosas ou manipulativas em mensagens de usuários ou conteúdos recuperados da base de conhecimento. Essas instruções podem tentar alterar o comportamento do assistente, ignorar suas regras ou induzi-lo a fornecer informações e recomendações fora do escopo autorizado.

**Impactos possíveis:**

- **Segurança:** podem ser geradas recomendações perigosas ou tentativas de contornar restrições operacionais.
- **Financeiro:** decisões inadequadas podem causar intervenções desnecessárias ou retrabalho.
- **Legal:** pode ocorrer descumprimento de procedimentos e limites de autorização.
- **Reputacional:** a manipulação do assistente pode comprometer a confiança na segurança do sistema.

**Mitigações:**

1. Tratar mensagens de usuários e conteúdos recuperados da base de conhecimento como dados, não como instruções capazes de substituir o System Prompt.
2. Não permitir que solicitações externas alterem a identidade, os objetivos, as regras ou os limites de atuação do PREDICTA.
3. Não divulgar informações internas, credenciais ou dados protegidos em resposta a instruções manipulativas.
4. Manter a exigência de autorização humana para abertura simulada de OS, independentemente das instruções recebidas.
5. Recusar solicitações que tentem contornar restrições de segurança ou induzir o assistente a executar ações não autorizadas.
6. Avaliar o comportamento do assistente com casos específicos de jailbreak e manipulação.

**Rastreabilidade:**

- **System Prompt:** blocos REGRAS e BORDA.
- **Fluxograma:** validação das solicitações e manutenção dos limites de autorização antes de qualquer ação.
- **Eval Set:** EVAL-008 e EVAL-009.
- **Base de conhecimento:** tratamento dos documentos recuperados como fontes de informação, não como instruções para o assistente.
- **Tools:** regras de acionamento e autorização, especialmente em `abrir_ordem_servico`.

### Risco 3 — Risco operacional e de segurança nas intervenções

**Descrição:**

O PREDICTA pode produzir recomendações inadequadas para situações que envolvam riscos operacionais, como atividades em altura, instalações elétricas ou intervenções em equipamentos de campo. Uma orientação sem fundamentação em procedimentos de segurança pode expor os profissionais a situações perigosas.

**Impactos possíveis:**

- **Segurança:** acidentes, lesões ou exposição dos profissionais a condições perigosas.
- **Financeiro:** custos com acidentes, afastamentos, danos e interrupções operacionais.
- **Legal:** descumprimento de normas regulamentadoras e procedimentos de segurança aplicáveis.
- **Reputacional:** prejuízo à imagem da organização e à confiança dos colaboradores.

**Mitigações:**

1. Consultar os procedimentos de segurança documentados antes de recomendar intervenções.
2. Fundamentar orientações sobre equipamentos de proteção individual (EPIs) e medidas de segurança em POPs, normas e documentos aplicáveis.
3. Não determinar autonomamente quais EPIs devem ser utilizados quando não houver documentação suficiente para sustentar a orientação.
4. Destacar quando uma atividade exigir capacitação, autorização ou condições especiais.
5. Não substituir treinamentos, análises de risco, procedimentos internos ou normas regulamentadoras.
6. Não orientar pessoas não capacitadas a realizar atividades em altura, instalações elétricas ou outras situações perigosas.
7. Quando não houver procedimento de segurança disponível, informar sua ausência e recomendar avaliação por profissional responsável.
8. Reforçar que a decisão e a execução da intervenção pertencem aos profissionais devidamente habilitados e autorizados.

**Rastreabilidade:**

- **System Prompt:** blocos ESCOPO, REGRAS e BORDA.
- **Fluxograma:** consulta aos procedimentos antes da recomendação de intervenção.
- **Eval Set:** EVAL-003 e EVAL-010.
- **Base de conhecimento:** Procedimentos Operacionais (POPs) e referências de segurança.
- **Tools:** `consultar_procedimento`.

### Risco 4 — Viés na priorização de ocorrências

**Descrição:**

O PREDICTA pode apresentar uma priorização enviesada, favorecendo determinados ativos, trechos ou localidades sem justificativa técnica. Isso pode ocorrer caso a análise considere fatores irrelevantes ou utilize critérios não documentados.

**Impactos possíveis:**

- **Segurança:** ativos que necessitam de atendimento podem receber prioridade inadequada.
- **Financeiro:** a distribuição ineficiente das equipes pode aumentar custos e deslocamentos.
- **Legal:** decisões sem critérios objetivos podem comprometer a transparência e a justificativa dos encaminhamentos.
- **Reputacional:** a percepção de tratamento desigual pode reduzir a confiança dos profissionais no sistema.

**Mitigações:**

1. Utilizar critérios documentados para priorização, como criticidade cadastrada do ativo, gravidade da ocorrência, reincidência e tempo de indisponibilidade, quando disponíveis.
2. Não utilizar a localização geográfica, isoladamente, como justificativa para favorecer ou prejudicar um ativo.
3. Não criar pesos, pontuações ou fórmulas de priorização sem fundamentação documental.
4. Apresentar justificativa verificável para a prioridade recomendada.
5. Quando faltarem dados relevantes, sinalizar a incerteza e evitar uma classificação definitiva sem fundamentação.
6. Manter a decisão final de atendimento sob responsabilidade dos profissionais competentes.

**Rastreabilidade:**

- **System Prompt:** blocos REGRAS e FORMATO.
- **Fluxograma:** etapa de análise de criticidade e priorização.
- **Eval Set:** EVAL-014, que verifica se ativos com características equivalentes recebem tratamento coerente, sem favorecimento baseado exclusivamente na localização.
- **Base de conhecimento:** Plano de Manutenção e Inventário de Ativos, incluindo a criticidade cadastrada.
- **Tools:** `listar_ativos_por_criticidade`.

### Risco 5 — LGPD: exposição de dados pessoais

**Descrição:**

O PREDICTA pode receber, consultar ou processar dados pessoais sem necessidade ou proteção adequada, ocasionando exposição indevida de informações. Em um contexto de CFTV, isso pode envolver imagens de pessoas, placas de veículos ou outros elementos que permitam identificar indivíduos.

**Impactos possíveis:**

- **Segurança:** a exposição de informações pode comprometer pessoas ou sistemas.
- **Financeiro:** incidentes de segurança e tratamento inadequado de dados podem gerar custos.
- **Legal:** o tratamento de dados pessoais em desacordo com a legislação aplicável pode gerar responsabilização.
- **Reputacional:** a exposição indevida pode comprometer a confiança dos usuários e da organização.

**Mitigações:**

1. Utilizar apenas os dados necessários para as análises de manutenção, observando o princípio da necessidade.
2. Evitar inserir ou divulgar dados pessoais de terceiros, imagens de pessoas, placas de veículos ou informações identificáveis quando não forem necessários à finalidade do sistema.
3. Não armazenar ou expor senhas, chaves de API, tokens ou outras credenciais.
4. Não utilizar dados pessoais em exemplos, testes e demonstrações quando dados fictícios puderem atender à finalidade.
5. Quando necessário, aplicar anonimização ou pseudonimização conforme a finalidade e o risco de reidentificação. A simples substituição de uma placa ou identificador por um código não deve ser considerada anonimização se ainda for possível identificar o titular.
6. Não enviar dados pessoais reais a provedores externos sem autorização e avaliação prévias das condições de tratamento e proteção aplicáveis.
7. Restringir o acesso às informações conforme as permissões e responsabilidades definidas pela organização.
8. Quando houver dúvida sobre a legitimidade ou a autorização para utilizar determinado dado, interromper seu tratamento até a validação adequada.

**Rastreabilidade:**

- **System Prompt:** blocos REGRAS e BORDA, com limites para uso e divulgação de informações.
- **Eval Set:** EVAL-012, teste específico de privacidade e proteção de dados.
- **Base de conhecimento:** critérios de exclusão de dados pessoais desnecessários, credenciais e informações confidenciais sem autorização.
- **Arquitetura:** envio de dados a provedores externos condicionado à autorização e às medidas de proteção aplicáveis.

**Referência normativa:** Lei nº 13.709/2018 — Lei Geral de Proteção de Dados Pessoais (LGPD).

### Risco 6 — Exposição de informações operacionais confidenciais

**Descrição:**

O PREDICTA pode processar ou apresentar informações operacionais confidenciais da organização, como dados de infraestrutura, localização de ativos, registros de falhas, configurações técnicas ou informações sobre vulnerabilidades, sem proteção ou autorização adequada.

Esse risco é distinto da exposição de dados pessoais: mesmo quando uma informação não identifica uma pessoa, ela pode ser sensível para a operação da concessionária.

**Impactos possíveis:**

- **Segurança:** a divulgação de informações sobre ativos e infraestrutura pode facilitar ações indevidas ou comprometer a operação.
- **Financeiro:** a exposição pode gerar prejuízos, custos de resposta a incidentes ou interrupções operacionais.
- **Legal:** o compartilhamento indevido pode violar obrigações contratuais ou políticas internas.
- **Reputacional:** a perda de confidencialidade pode comprometer a confiança na solução e na organização.

**Mitigações:**

1. Utilizar somente as informações operacionais necessárias à finalidade da análise.
2. Não divulgar dados de infraestrutura, configurações, vulnerabilidades ou registros internos a usuários sem autorização.
3. Não inserir credenciais, tokens ou chaves de API em prompts, documentos ou respostas.
4. Avaliar as condições de segurança, privacidade, retenção e tratamento de dados dos provedores externos utilizados pela arquitetura API-first, antes de transmitir informações operacionais.
5. Não presumir que o uso de uma API externa é automaticamente seguro ou autorizado para qualquer tipo de dado.
6. Utilizar dados fictícios ou adequadamente desidentificados nos testes e demonstrações.
7. Restringir o acesso às informações conforme as permissões e responsabilidades definidas pela organização.
8. Registrar, no desenho da solução, quais categorias de dados podem ser processadas e quais não devem ser transmitidas aos provedores.

**Rastreabilidade:**

- **System Prompt:** blocos ESCOPO e REGRAS.
- **Fluxograma:** controle das informações utilizadas nas consultas e transmitidas ao modelo.
- **Eval Set:** não há, na versão atual, um caso específico que teste isoladamente a confidencialidade operacional. A mitigação é contemplada principalmente pelas regras de arquitetura, proteção de dados e gestão de credenciais.
- **Arquitetura:** avaliação das condições de segurança e tratamento de dados dos provedores de API selecionados.
- **Repositório:** proteção de segredos e credenciais, sem inserção de chaves no código ou em arquivos públicos.

### Risco 7 — Excesso de confiança nas respostas do assistente

**Descrição:**

Os usuários podem interpretar as respostas do PREDICTA como diagnósticos definitivos ou decisões técnicas validadas, mesmo quando as informações disponíveis forem insuficientes, contraditórias ou baseadas apenas em hipóteses.

**Impactos possíveis:**

- **Segurança:** uma recomendação não confirmada pode levar a uma intervenção inadequada ou à negligência de uma falha real.
- **Financeiro:** decisões baseadas em conclusões precipitadas podem gerar custos, deslocamentos e retrabalho.
- **Legal:** a utilização de recomendações não validadas pode comprometer a responsabilidade técnica e operacional.
- **Reputacional:** a confiança excessiva no assistente pode comprometer a credibilidade do sistema.

**Mitigações:**

1. Identificar claramente fatos registrados, hipóteses, conclusões provisórias e informações inconclusivas.
2. Não apresentar uma hipótese como causa confirmada.
3. Informar o nível de confiança da análise, acompanhado de justificativa baseada nas evidências disponíveis.
4. Destacar dados ausentes, divergências entre fontes e limitações das ferramentas utilizadas.
5. Recomendar validação humana quando a decisão envolver segurança, intervenção técnica ou priorização relevante.
6. Reforçar que o PREDICTA apoia a decisão, mas não substitui a avaliação dos profissionais competentes.
7. Não apresentar a prioridade recomendada como uma ordem automática de execução.

**Rastreabilidade:**

- **System Prompt:** blocos REGRAS, FORMATO e TOM.
- **Fluxograma:** apresentação da análise, das evidências, das hipóteses e das limitações antes do encaminhamento.
- **Eval Set:** EVAL-002, EVAL-008 e EVAL-011. O EVAL-014 também oferece verificação complementar sobre a necessidade de critérios objetivos na priorização.
- **Base de conhecimento:** identificação da origem e da confiabilidade das informações utilizadas.

### Risco 8 — Estouro da janela de contexto e perda de informações relevantes

**Descrição:**

Durante conversas extensas, o volume de mensagens, documentos recuperados e resultados de ferramentas pode ultrapassar a capacidade de contexto disponível para o modelo. Isso pode ocasionar perda de informações relevantes, esquecimento de restrições anteriores ou respostas baseadas em um histórico incompleto.

**Impactos possíveis:**

- **Segurança:** a perda de uma informação relevante pode comprometer uma análise ou recomendação.
- **Financeiro:** interpretações incompletas podem gerar retrabalho e decisões ineficientes.
- **Legal:** a omissão de restrições ou autorizações anteriores pode comprometer a rastreabilidade da decisão.
- **Reputacional:** respostas inconsistentes ao longo de uma conversa podem reduzir a confiança no assistente.

**Mitigações:**

1. Definir uma política de gerenciamento de contexto e tokens, considerando os limites do modelo e do provedor utilizado.
2. Priorizar informações diretamente relacionadas à ocorrência em análise.
3. Recuperar documentos e históricos de forma seletiva, evitando inserir conteúdo desnecessário no contexto.
4. Preservar informações essenciais da conversa, como TAG, sintomas, horário, evidências, restrições e decisões já tomadas.
5. Quando houver risco de perda de contexto, produzir um resumo estruturado e solicitar confirmação do usuário antes de continuar com informações críticas.
6. Não presumir que o assistente mantém memória persistente entre sessões.
7. Informar quando não for possível recuperar uma informação anterior com segurança.
8. Testar o comportamento do sistema em conversas extensas e situações próximas ao limite de contexto.

**Rastreabilidade:**

- **System Prompt:** bloco BORDA, com orientações para continuidade e recuperação do contexto da conversa.
- **Eval Set:** EVAL-011 verifica a recuperação de informações dentro da mesma sessão, mas não testa diretamente o estouro da janela de contexto.
- **Arquitetura:** gerenciamento de contexto, recuperação seletiva de informações e limites de tokens.
- **Política de contexto:** será detalhada no tratamento do bônus de gerenciamento quantitativo de contexto e tokens.

### Risco 9 — Interpretação ambiental equivocada

**Descrição:**

O PREDICTA pode confundir uma degradação de imagem causada por condições ambientais — como chuva, neblina, umidade ou incidência solar — com uma falha real do equipamento. Também pode atribuir indevidamente ao ambiente uma degradação causada por uma falha técnica.

**Impactos possíveis:**

- **Segurança:** uma falha real pode passar despercebida, comprometendo o monitoramento viário.
- **Financeiro:** podem ocorrer manutenções desnecessárias ou atrasos na correção de falhas.
- **Legal:** decisões operacionais baseadas em diagnósticos equivocados podem gerar consequências e responsabilidades.
- **Reputacional:** interpretações incorretas podem reduzir a confiança dos profissionais no assistente.

**Mitigações:**

1. Consultar os registros ambientais considerando a janela padrão de 30 minutos antes e depois do horário da ocorrência.
2. Cruzar os dados ambientais com os sintomas registrados e o histórico de falhas.
3. Não considerar chuva, neblina, umidade ou luminosidade como confirmação isolada da causa.
4. Diferenciar causas ambientais prováveis de falhas técnicas confirmadas.
5. Identificar a origem dos dados ambientais e distinguir registros oficiais de informações complementares ou simuladas.
6. Na ausência de registros ambientais suficientes, informar a limitação e evitar conclusões definitivas.
7. Recomendar inspeção ou avaliação profissional quando não for possível distinguir a causa com segurança.

**Rastreabilidade:**

- **System Prompt:** blocos REGRAS e FORMATO, com distinção entre evidências e hipóteses.
- **Fluxograma:** etapa de investigação técnica e comparação de evidências ambientais e históricas.
- **Eval Set:** EVAL-004.
- **Base de conhecimento:** Registro de Condições Ambientais e Histórico de Falhas.
- **Tools:** `consultar_condicoes_ambientais` e `consultar_historico_falhas`.

### Risco 10 — Dados incompletos, inconsistentes ou desatualizados

**Descrição:**

O PREDICTA pode produzir análises inadequadas ao utilizar informações incompletas, desatualizadas ou inconsistentes sobre ativos CFTV e ITS, históricos de falhas, procedimentos ou condições operacionais.

**Impactos possíveis:**

- **Segurança:** recomendações inadequadas podem atrasar a identificação ou a correção de falhas relevantes.
- **Financeiro:** podem ocorrer intervenções desnecessárias, retrabalho ou aumento do tempo de indisponibilidade.
- **Legal:** decisões baseadas em registros incorretos podem gerar consequências e responsabilidades.
- **Reputacional:** informações pouco confiáveis podem reduzir a confiança no sistema.

**Mitigações:**

1. Identificar, sempre que disponíveis, a origem, a versão, a data e a validade dos documentos consultados.
2. Verificar se os dados correspondem à TAG e ao modelo do equipamento analisado.
3. Sinalizar informações ausentes, incompletas, desatualizadas ou inconsistentes.
4. Não preencher lacunas com suposições apresentadas como fatos.
5. Quando houver divergência entre fontes, apresentar o conflito e solicitar validação profissional se ele puder afetar a decisão.
6. Diferenciar um ativo inexistente na base de um ativo cuja consulta não pôde ser concluída.
7. Recomendar a atualização ou conferência dos registros antes de emitir conclusões que dependam dessas informações.

**Rastreabilidade:**

- **System Prompt:** blocos REGRAS e BORDA, incluindo tratamento de dados insuficientes e conflitos entre fontes.
- **Fluxograma:** verificação das informações do ativo e da suficiência dos dados.
- **Eval Set:** EVAL-005 e EVAL-006.
- **Base de conhecimento:** metadados de origem, versão, validade e data dos documentos.
- **Tools:** regras de retorno e tratamento de informações ausentes nas consultas.

### Risco 11 — Ação operacional não autorizada

**Descrição:**

O PREDICTA pode executar ou aparentar executar uma ação operacional sem autorização explícita de um profissional responsável, especialmente durante a preparação ou a abertura simulada de Ordens de Serviço (OS).

**Impactos possíveis:**

- **Segurança:** uma intervenção inadequada ou não autorizada pode colocar equipamentos e profissionais em risco.
- **Financeiro:** pode ocorrer mobilização indevida de equipes, recursos e materiais.
- **Legal:** pode haver descumprimento de procedimentos internos e dos limites de autorização.
- **Reputacional:** a ausência de controle sobre ações operacionais pode comprometer a confiança no assistente.

**Mitigações:**

1. Exigir autorização humana explícita antes de acionar `abrir_ordem_servico`.
2. Apresentar previamente os dados da OS para revisão do profissional responsável.
3. Nunca abrir uma OS por iniciativa própria, mesmo quando a ocorrência parecer urgente.
4. Manter a abertura de OS exclusivamente em modo simulado nesta etapa do projeto.
5. Não interpretar solicitações ambíguas como autorização.
6. Validar a autorização de forma independente na aplicação, antes de permitir a execução da ferramenta. A validação não deve depender apenas da interpretação do modelo ou de um parâmetro presente no JSON Schema.
7. Informar claramente se a OS foi apenas preparada, autorizada ou aberta em modo simulado.
8. Não executar intervenções físicas, liberar equipamentos ou substituir decisões dos profissionais responsáveis.

**Rastreabilidade:**

- **System Prompt:** blocos ESCOPO, REGRAS e BORDA.
- **Fluxograma:** revisão da proposta e validação da autorização antes da abertura simulada.
- **Eval Set:** EVAL-009.
- **Tools:** `abrir_ordem_servico`, condicionada à autorização humana explícita e à validação independente pela aplicação.

## 3. Diretrizes gerais de proteção e uso responsável

Além das medidas específicas de cada risco, o projeto adota as seguintes diretrizes:

- **Supervisão humana:** recomendações de diagnóstico e priorização são apoio à decisão; a responsabilidade final permanece com os profissionais competentes.
- **Minimização de dados:** utilizar somente informações necessárias à finalidade de manutenção.
- **Rastreabilidade:** preservar, no desenho da solução, a identificação das fontes consultadas e das limitações relevantes para a análise.
- **Transparência:** comunicar incertezas, dados ausentes, divergências e limitações das ferramentas.
- **Segurança operacional:** não executar intervenções físicas nem abrir Ordens de Serviço reais nesta etapa do projeto.
- **Proteção de credenciais:** não inserir chaves, tokens ou senhas nos documentos, exemplos ou repositório público.
- **Dados fictícios:** identificar claramente os dados simulados e não apresentá-los como registros reais da Motiva.
- **Proteção de informações:** avaliar os dados transmitidos aos provedores externos e não compartilhar informações pessoais ou operacionais confidenciais sem autorização e controles adequados.
- **Limites de atuação:** não permitir que o assistente substitua procedimentos oficiais, profissionais habilitados ou decisões operacionais.
