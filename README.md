# Agency Agents v2: atualizações e novos agentes

> Situação do projeto em **17 de novembro de 2026**

## 📊 Resumo em números

| | Antes (até 17/11/2026) | Depois (v2) | Diferença |
|---|---|---|---|
| **Agentes** | **283** | **334** | **+51 novos** |
| **Divisões** | 18 | 26 | +8 novas |
| **Agentes existentes reescritos** | — | 41 | — |
| **Avisos de qualidade do linter** | 58 | 0 | −58 |

- O projeto tinha **283 agentes** em 18 divisões até 17 de novembro de 2026.
- Foram adicionados **51 agentes novos** em **8 divisões novas**.
- **41 agentes existentes** foram reescritos e ampliados. Os nomes continuam iguais, então quem já instalou esses agentes não é afetado.
- O total agora é **334 agentes** em **26 divisões**.

---

## ✅ Verificações de qualidade

Todas as verificações do próprio projeto passaram na versão v2:

| Verificação | Resultado |
|---|---|
| `scripts/lint-agents.sh` | 0 erros e 0 avisos em 334 arquivos (a versão anterior tinha 58 avisos) |
| `scripts/check-agent-originality.sh` | Aprovado, sem agentes duplicados ou "re-skins" |
| `scripts/check-divisions.sh` | Aprovado: as 26 divisões estão consistentes no catálogo, nos scripts e no CI |
| `scripts/check-tools.sh` | Aprovado: as 17 ferramentas estão consistentes |
| `scripts/test-convert-outputs.sh` | 32 testes aprovados, 0 falhas (334 agentes × 15 ferramentas) |

---

## 🔧 Parte 1: Agentes existentes atualizados (41)

Estes agentes tinham seções obrigatórias faltando (Identity, Core Mission e Critical Rules) ou eram curtos demais. Todos agora seguem a estrutura padrão do projeto:

- identidade
- missão
- regras críticas
- entregáveis com modelos e código
- fluxo de trabalho
- estilo de comunicação
- memória e aprendizado
- métricas de sucesso
- capacidades avançadas

O conteúdo bom que já existia foi preservado.

| # | Divisão | Agente | Palavras (antes → depois) |
|---|---|---|---|
| 1 | Engineering | CMS Developer | 2.338 → 2.549 |
| 2 | Engineering | Code Reviewer | 432 → 1.631 |
| 3 | Engineering | Git Workflow Master | 476 → 1.720 |
| 4 | Engineering | Multi-Agent Systems Architect | 4.286 → 5.038 |
| 5 | Engineering | Senior Developer | 789 → 1.962 |
| 6 | Engineering | SRE (Site Reliability Engineer) | 542 → 1.491 |
| 7 | Marketing | Content Creator | 387 → 1.832 |
| 8 | Marketing | Growth Hacker | 392 → 1.790 |
| 9 | Marketing | Social Media Strategist | 914 → 1.848 |
| 10 | Paid Media | Paid Media Auditor | 714 → 1.688 |
| 11 | Paid Media | Ad Creative Strategist | 691 → 2.068 |
| 12 | Paid Media | Paid Social Strategist | 701 → 1.801 |
| 13 | Paid Media | PPC Campaign Strategist | 663 → 1.687 |
| 14 | Paid Media | Programmatic & Display Buyer | 683 → 1.828 |
| 15 | Paid Media | Search Query Analyst | 674 → 1.810 |
| 16 | Paid Media | Tracking & Measurement Specialist | 685 → 1.617 |
| 17 | Product | Feedback Synthesizer | 904 → 1.873 |
| 18 | Product | Sprint Prioritizer | 1.149 → 1.755 |
| 19 | Product | Trend Researcher | 1.239 → 1.599 |
| 20 | Project Management | Senior Project Manager | 719 → 1.764 |
| 21 | Sales | Deal Strategist | 2.008 → 2.839 |
| 22 | Sales | Discovery Coach | 2.179 → 3.450 |
| 23 | Sales | Sales Engineer | 2.031 → 3.204 |
| 24 | Sales | Outbound Strategist | 1.639 → 2.329 |
| 25 | Spatial Computing | Terminal Integration Specialist | 476 → 1.744 |
| 26 | Spatial Computing | visionOS Spatial Engineer | 376 → 1.835 |
| 27 | Spatial Computing | XR Cockpit Interaction Specialist | 232 → 1.960 |
| 28 | Spatial Computing | XR Immersive Developer | 244 → 1.470 |
| 29 | Spatial Computing | XR Interface Architect | 220 → 1.658 |
| 30 | Specialized | Automation Governance Architect | 812 → 1.944 |
| 31 | Specialized | Chief Financial Officer | 2.838 → 3.492 |
| 32 | Specialized | Data Consolidation Agent | 339 → 1.577 |
| 33 | Specialized | Data Privacy Officer | 3.305 → 4.028 |
| 34 | Specialized | ESG & Sustainability Officer | 3.098 → 4.003 |
| 35 | Specialized | M&A Integration Manager | 3.222 → 3.843 |
| 36 | Specialized | Operations Manager | 2.841 → 3.386 |
| 37 | Specialized | Organizational Psychologist | 3.305 → 4.080 |
| 38 | Specialized | Report Distribution Agent | 371 → 1.749 |
| 39 | Specialized | Sales Data Extraction Agent | 410 → 1.558 |
| 40 | Specialized | Document Generator | 308 → 1.560 |
| 41 | Testing | Evidence Collector | 1.155 → 2.012 |

### Principais correções de conteúdo

- **Marketing e mídia paga:**
  - Foram removidos recursos que não existem mais: Universal Analytics, os públicos semelhantes do Google Ads, os desafios de hashtag do TikTok e as InMail Ads do LinkedIn.
  - As referências foram atualizadas para GA4, Advantage+ (Meta), Smart+ (TikTok) e X (antigo Twitter).
  - Metas irreais, como 25% de engajamento, foram trocadas por valores plausíveis.
- **Privacidade (GDPR):** o aviso às pessoas afetadas por um vazamento de dados estava descrito de forma errada. Agora segue a regra "sem demora injustificada", que é separada do prazo de 72 horas para o regulador.
- **ESG:**
  - A regra climática da SEC, que na prática não está em vigor, agora aparece como tal.
  - O adiamento e a redução de escopo da CSRD foram registrados.
  - As datas das leis climáticas da Califórnia foram corrigidas.
  - O TCFD aparece como incorporado ao ISSB (IFRS S1/S2).
  - A escala de notas do CDP foi corrigida.
- **Computação espacial (XR):**
  - O Safari do iPhone não tem WebXR, então o substituto indicado agora é o AR Quick Look.
  - O HoloLens aparece como dispositivo legado.
  - O agente de visionOS agora vale para o visionOS 26 e versões posteriores.
- **SRE:** o objetivo de latência (SLO) foi corrigido, e entrou o terceiro par de alertas de consumo da margem de erro (error budget).
- **Vendas:**
  - Números sem fonte foram removidos.
  - Entraram as regras de anti-spam e privacidade (CAN-SPAM, GDPR/PECR, CASL) e os limites de envio de e-mail do Google e do Yahoo.
- **Psicologia organizacional:**
  - Modelos populares sem validação científica agora aparecem como tal.
  - Entrou o anonimato mínimo de 5 pessoas em pesquisas internas.
  - Casos de risco são escalados imediatamente.
- **Outros:**
  - Blocos de código sem linguagem foram marcados.
  - Referências a arquivos que não existiam foram removidas.
  - O Senior Project Manager agora usa os caminhos de pasta do Agents Orchestrator.

---

## 🆕 Parte 2: Novas divisões e agentes (51)

### ⚖️ Legal (7 agentes)

Raciocínio jurídico de nível profissional, com base em leis dos EUA, da União Europeia e do Reino Unido. Os agentes sinalizam quando é preciso um advogado local e sempre deixam claro que não substituem um advogado.

| Agente | O que faz |
|---|---|
| 🤝 Contract Negotiator | Revisão e negociação de contratos comerciais (SaaS, MSA, DPA), posições de recuo e limites de responsabilidade |
| ™️ IP & Trademark Strategist | Registro de marcas (USPTO, EUIPO, Protocolo de Madri), direitos autorais, segredos comerciais e licenças open source |
| 🧑‍⚖️ Employment Law Advisor | Contratação, classificação entre funcionário e prestador, demissões e trabalho remoto |
| 🏛️ Litigation Strategist | Avaliação inicial de casos, preservação de provas, e-discovery e decisão entre acordo e litígio |
| 🏢 Corporate Governance Counsel | Abertura de empresas, cap table, atos do conselho, SAFE e Série A |
| 📡 Regulatory Affairs Specialist | Monitoramento regulatório, licenças, defesa do consumidor e publicidade |
| 🤖 AI Governance Counsel | EU AI Act (com o cronograma revisado em 2026), NIST AI RMF, ISO/IEC 42001 e contratos com fornecedores de IA |

### 🧑‍🤝‍🧑 People Ops (6 agentes)

Gestão de pessoas e RH estratégico.

| Agente | O que faz |
|---|---|
| 💰 Compensation & Benefits Analyst | Faixas salariais, pesquisas de mercado, auditoria de equidade salarial e diretiva europeia de transparência salarial |
| 📊 People Analytics Scientist | Modelos de rotatividade (turnover), pesquisas de engajamento e análises em SQL e Python com privacidade |
| ⚖️ Performance Management Architect | Ciclos de avaliação, calibração, OKRs e redução de vieses |
| 🕊️ Employee Relations Mediator | Investigações internas, mediação de conflitos e documentação |
| 🧮 Workforce Planner | Planejamento de quadro de pessoal, desenho organizacional e decisão entre contratar, desenvolver ou terceirizar |
| 🧭 Employee Experience Designer | Jornada do colaborador, momentos que importam e desligamento |

### 🎓 Education (6 agentes)

Educação básica, ensino superior e aprendizagem ao longo da vida.

| Agente | O que faz |
|---|---|
| 🧩 Instructional Designer | Desenho reverso (backward design), ADDIE/SAM, Taxonomia de Bloom e planos de aula |
| 🗺️ Curriculum Architect | Sequência curricular e alinhamento à BNCC, Common Core e NGSS |
| 📐 Assessment Designer | Avaliações, rubricas, análise de itens e integridade acadêmica na era da IA |
| 🦉 Socratic Tutor | Tutoria que guia sem entregar a resposta, segura para menores de idade |
| 🛠️ EdTech & LMS Specialist | Moodle, Canvas, Google Classroom, LTI 1.3, xAPI e SCORM |
| 🌱 Inclusive Learning Specialist | Desenho Universal para a Aprendizagem (DUA/UDL), planos individuais (IEP/504), dislexia, TDAH e tecnologia assistiva |

### 📈 Data Science (6 agentes)

Ciência de dados com exemplos de código em Python e SQL.

| Agente | O que faz |
|---|---|
| 🧬 Causal Inference Scientist | Diferenças em diferenças (DiD), controle sintético, variáveis instrumentais, regressão descontínua (RDD) e escore de propensão |
| 🧱 Analytics Engineer | Modelagem em dbt, testes, camada semântica e contratos de dados |
| 🛠️ MLOps Engineer | Registro de modelos, CI/CD de modelos, detecção de drift e MLflow |
| 🔮 Forecasting Specialist | Séries temporais, backtesting, WAPE/MASE e reconciliação hierárquica |
| 🗂️ Data Governance Steward | Catálogo de dados, linhagem, classificação e políticas de acesso |
| 🧭 Decision Analyst | Árvores de métricas, definição de KPIs e memorandos executivos |

### 🏭 Manufacturing (7 agentes)

Indústria e operações de chão de fábrica.

| Agente | O que faz |
|---|---|
| 📉 Lean Six Sigma Black Belt | DMAIC, mapeamento de fluxo de valor (VSM), controle estatístico de processo (CEP), Cp/Cpk e kaizen |
| 🛡️ Quality Engineer | ISO 9001:2026, IATF 16949, APQP, PPAP, FMEA, 8D e ações corretivas (CAPA) |
| 🗓️ Production Planner | MPS/MRP, S&OP, OEE, takt time e balanceamento de linha |
| 🔧 Reliability Engineer | Manutenção produtiva total (TPM), RCM, manutenção preditiva, MTBF/MTTR e Weibull |
| 🦺 EHS Safety Manager | Análise de riscos (APR/JSA, HAZOP), bloqueio e etiquetagem (LOTO), ISO 45001, OSHA e NRs brasileiras |
| 🤝 Strategic Sourcing Manager | Estratégia de categorias, modelos de custo, matriz de Kraljic e negociação |
| 🏭 Industry 4.0 Automation Engineer | CLPs (IEC 61131-3), SCADA/MES, ISA-95, OPC UA, MQTT e segurança de redes industriais (IEC 62443) |

### 🌾 Agribusiness (6 agentes)

Agronegócio tropical e temperado, com exemplos do Brasil, dos EUA e da Argentina.

| Agente | O que faz |
|---|---|
| 🌱 Agronomist | Fertilidade do solo, calagem e gessagem, nutrição de plantas e manejo integrado de pragas (MIP) |
| 🛰️ Precision Ag Specialist | Mapas de produtividade, aplicação em taxa variável, NDVI e zonas de manejo |
| 🐄 Livestock Production Advisor | Indicadores de corte, leite e aves, eficiência alimentar, bem-estar animal e biossegurança |
| 📉 Commodity Risk Manager | Hedge de soja, milho e boi na B3 e na CBOT, base, opções e CPR |
| 🚜 Farm Business Manager | Custo por hectare e por saca, orçamentos, crédito, máquinas e sucessão familiar |
| 🔎 Food Safety & Traceability Specialist | APPCC (HACCP), GlobalG.A.P., FSMA, EUDR e rastreabilidade |

### 📰 Media & Journalism (6 agentes)

Prática de redação jornalística (não marketing).

| Agente | O que faz |
|---|---|
| 🔎 Investigative Reporter | Fontes, pedidos de acesso a informação (FOIA), OSINT e direito de resposta |
| ✅ Fact-Checker | Checagem de fatos, verificação de imagens e vídeos e princípios da IFCN |
| 🗞️ Managing Editor | Critério de notícia, pauta, edição, títulos e AP Style |
| 📊 Data Journalist | Reportagens a partir de dados, pandas e SQL, metodologia e gráficos honestos |
| 🎙️ Audio Documentary Producer | Narrativa em áudio, entrevistas, roteiro para o ouvido e ética de gravação |
| ⚖️ Standards & Ethics Editor | Código da SPJ, fontes anônimas, risco de difamação e uso de IA na redação |

### 🌎 LATAM (7 agentes)

Especialistas em América Latina, com foco no Brasil e no México.

| Agente | O que faz |
|---|---|
| 🧾 Brazil Tax Specialist | Simples Nacional, Lucro Presumido e Real, NF-e, SPED e Reforma Tributária (CBS, IBS e IS, com a transição de 2026 a 2033) |
| 🛡️ LGPD Compliance Officer | Bases legais, resoluções da ANPD, comunicação de incidentes, RIPD e transferências internacionais |
| ⚡ Pix & Open Finance Engineer | Arquitetura do Pix, BR Code com CRC16, Pix Automático, MED 2.0 e APIs do Open Finance Brasil |
| 🤝 Mercado Livre Growth Strategist | Reputação, Mercado Envios e Full, Mercado Ads e precificação no Brasil, México e Argentina |
| 💬 WhatsApp Commerce Strategist | WhatsApp Business Platform, preço por mensagem, modelos de mensagem, regras de opt-in e catálogo |
| 🧮 Mexico CFDI Compliance Specialist | CFDI 4.0, SAT, RFC, complemento de pago, Carta Porte e RESICO |
| 👷 Brazil Labor & CLT Advisor | CLT, eSocial, 13º salário, férias, FGTS, rescisões e risco de pejotização |

---

## 📁 Resumo das novas divisões

| Divisão | Pasta | Agentes |
|---|---|---|
| ⚖️ Legal | `legal/` | 7 |
| 🧑‍🤝‍🧑 People Ops | `people-ops/` | 6 |
| 🎓 Education | `education/` | 6 |
| 📈 Data Science | `data-science/` | 6 |
| 🏭 Manufacturing | `manufacturing/` | 7 |
| 🌾 Agribusiness | `agribusiness/` | 6 |
| 📰 Media & Journalism | `media-journalism/` | 6 |
| 🌎 LATAM | `latam/` | 7 |
| **Total** | | **51** |

As 8 divisões novas foram registradas em `divisions.json`, `scripts/lint-agents.sh`, `scripts/convert.sh` e `.github/workflows/lint-agents.yml`. O README principal ganhou as tabelas das novas divisões e o total atualizado.

---

## ⚠️ Observações importantes

- **Idioma:** os agentes estão em inglês, como o resto do projeto. Termos locais como NF-e, CNPJ, eSocial e CFDI aparecem no original.
- **Datas e valores legais:** a maioria foi conferida na web em novembro de 2026. Alguns foram escritos de memória, como especificações de contratos da B3 e certos detalhes do CFDI. Nesses casos o próprio agente orienta a confirmar antes de usar.
- **Áreas reguladas:** os agentes jurídicos, fiscais, trabalhistas, financeiros e de saúde animal sempre encaminham a decisão final a um profissional habilitado (advogado, contador, veterinário ou corretor).
- **Código não executado:** a maioria dos exemplos em Python foi executada e funciona. Os que dependem de bibliotecas como MLflow, dbt, statsmodels ou GDAL foram escritos conforme a documentação oficial, mas não foram executados.
