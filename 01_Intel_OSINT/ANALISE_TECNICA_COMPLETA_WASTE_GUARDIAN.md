# ANÁLISE TÉCNICA COMPLETA — Waste Guardian
## Consolidação de Inteligência: 615 Métricas, 112 Fontes, 8 Batches


> **Status:** 🔴 ANÁLISE FINAL (base de dados — ver precedência abaixo)  
> **Last Updated:** 2026-06-12  
> **Priority:** P1  
> **Data:** 2026-06-12  
> **Versão:** 2.1 — Consolidação Completa  
> **Projeto:** Waste Guardian — Liga Jovem DLJ4  
> **Propósito:** Documentar todas as descobertas, gaps e recomendações para refatoração da proposta de valor  

> **⚖️ PRECEDÊNCIA (v2.1):** os **números e o modelo canónicos** do Waste Guardian estão na **Análise Narrativa v4.0** (`ANALISE_NARRATIVA_WASTE_GUARDIAN.md` §15.1, §15.2 e §15.6) e na **projeção financeira do pitch** (`02_Estrategia_Vencedora/PITCH_Waste_Guardian_Liga_Jovem.md`). Este documento é a **base de dados** (615 métricas, 112 fontes, 8 batches) — **não é o quadro canónico**. Onde este documento e a narrativa divergirem, **a narrativa v4.0 prevalece**. As §8.2 (mix de receita) e §8.3 (roadmap) foram alinhadas ao quadro canónico; as §5.3 mantém-se como decomposição operacional dos mesmos 6 modelos.

---

## 1. SUMÁRIO EXECUTIVO

### 1.1 O Que Temos (Conjunto de Dados)

| Batch | Tema | Métricas | Fontes | Status |
|-------|------|----------|--------|--------|
| 1 | Macro Context (Desperdício BR) | 23 | 11 | ✅ Concluído |
| 2 | Environmental Impact (CO₂) | 37 | 14 | ✅ Concluído |
| 3 | Business Market (TAM/SAM/SOM) | 32 | 15 | ✅ Concluído |
| 4 | Consumer Behavior (Personas) | 421 | 13 | ✅ Concluído |
| 5 | ODS Alignment | 30 | 12 | ✅ Concluído |
| 6 | Regulatory (Leis/Brasil) | 28 | 12 | ✅ Concluído |
| 7 | Competitors | 12 | 17 | ✅ Concluído |
| 8 | ESG Brands | 32 | 18 | ✅ Concluído |
| **TOTAL** | | **615** | **112** | ✅ |

### 1.2 Tese Central

**Waste Guardian ocupa um quadrante que NINGUÉM no mundo ocupa:**

```
(Household Focus) + (AI Scanner) + (Gamificação) + (PT-BR) + (B2B Data)

O Brasil tem uma janela de 12-18 meses antes que players globais entrem.
```

### 1.3 Números Mais Validados (Alta Confiança)

| Métrica | Valor | Fonte | Confiança |
|---------|-------|-------|-----------|
| Desperdício doméstico BR | 94 kg/pessoa/ano | Embrapa/UNEP 2024 | Alta |
| Perda econômica BR | R$ 61,3 bi/ano | Embrapa/FAO/Senado 2018 | Média |
| TAM Global Food Waste | USD 75-87 bi | 3 fontes independentes | Alta |
| SAM BR (app consumer) | R$ 400-900M | Bottom-up + top-down | Média |
| WTP premium | R$ 9,90/mês | Benchmark + renda | Média |
| B2B ticket médio | R$ 200-500K/ano | 20 prospects validados | Média |
| Lei 14.016/2020 | Vige desde 2020 | Plano.gov.br | Alta |

---

## 2. ANÁLISE DE MERCADO

### 2.1 TAM/SAM/SOM — Mercado de Gestão de Desperdício Alimentar

#### TAM Global
```
TAM Global 2024: USD 75-87 bilhões
CAGR: 5,4-6,5% até 2033-2034
3 fontes independentes convergem
```

#### TAM Brasil (Food Waste Management Total)
```
LatAm = 6,4% do TAM global = USD 4,6 bi = R$ 22,9 bi
Brasil ~50% do LatAm = R$ 11,5 bi (market research direto)
Ajustado para subset desperdício: R$ 18,4-32 bi
```


#### SAM Brasil (segmento endereçável)
```
SAM B2C household:     R$ 400M  (21,7M famílias × 8% willing to pay × R$ 107/ano)
SAM B2B dashboard:      R$ 500M  (3.750 grandes establishments × R$ 24K/ano)
SAM B2B2C marketplace:  R$ 440M  (8% take rate sobre volume)
SAM TOTAL:              R$ 1,34 bi (cenário convergente)
```

#### SOM (Mercado Obtível nos Primeiros 3 Anos)
```
Conservador:  R$ 2M  (25K users + 80 B2B)
REALISTA:     R$ 5M  (50K users + 150 B2B) ← BASE CASE
Otimista:     R$ 20M (250K users + 300 B2B)
```

### 2.2 Distribuição Setorial do Desperdício (Proxy UNEP)

| Segmento | % Global | Estimativa BR | Volume BR |
|----------|----------|---------------|-----------|
| Domicílios | 60% | ~20-28M t/ano | **PRIORIDADE** |
| Restaurantes/Serviços | 28% | ~9-13M t/ano | Secundário |
| Varejo | 12% | ~4-6M t/ano | Secundário |

**Insight:** 60% do desperdício é doméstico. O app consumer addressing este problema está alinhado com o maior segmento do mercado.

### 2.3 Análise Comparativa: Brasil vs. Global

| Métrica | Brasil | Global | Análise |
|---------|--------|--------|---------|
| Desperdício per capita | 94 kg/pessoa/ano | 132 kg/pessoa/ano | Brasil está 29% MELHOR que média global |
| Perda econômica | R$ 61,3 bi/ano | — | 3% do PIB |

| Tendência | Estável (sem dados) | Estável | Mundo não está reduzindo |
| Regulação | Lei 14.016 + COP30 | — | Brasil avançando |

---

## 3. ANÁLISE DE PERSONAS (Batch 04)

### 3.1 3 Personas Brasileiras

#### Maria Silva — Persona Primária (Classe B1)
```
Perfil:
├── Idade: 35-50 anos
├── Classe: B1 (R$ 10.361/mês)
├── Família: 4 pessoas
├── Smartphone: 98% (iOS 40% / Android 60%)
└── Digital literacy: Alta

Jornada de Compra:
├── Domingo: Compra grande no supermercado (R$ 350, 60% do mês)
├── Terça: Hortifruti (R$ 80)
├── Quinta: Pequenos ajustes (R$ 50)
├── Sábado: Feira mensal com família (R$ 110)
└── Apps: Mercado Livre, iFood, Rappi

Gatilhos de Desperdício:
├── Compra em excesso (planejamento zero)
├── Hortifruti com validade curta
├── "Ai desculpa, achei que ia comer essa semana"
└── Sobras de arroz/feijão que ninguém esquenta

WTP: R$ 9,90-15/mês
Sensibilidade: Cashback, ranking entre amigos, lista compartilhada
```

#### João Santos — Persona Secundária (Classe C1)
```
Perfil:
├── Idade: 25-35 anos
├── Classe: C1 (R$ 3.277/mês)
├── Família: 3 pessoas
├── Smartphone: 91% (Android 85%)
└── Digital literacy: Média

Jornada de Compra:
├── Quinta: Atacadão/Assaí (R$ 450 mensal)
├── Sábado: Feira livre (R$ 80)
├── Diário: Mercearia de bairro para frescos
└── Apps: WhatsApp, Facebook, PicPay, Nubank

Gatilhos de Desperdício:
├── Compra em quantidade (atacadão)
├── "Deu vontade de fazer algo diferente"
├── Esquece o que tem na geladeira
└── Festinha na sexta que não rolou

WTP: R$ 4,90/mês (só se houver cashback)
Sensibilidade: Promoções, cupons, indicação de amigos
```

#### Dona Lourdes — Persona Acessível (Classe C2)
```
Perfil:
├── Idade: 60+ anos
├── Classe: C2 (R$ 1.966/mês)
├── Família: 2 pessoas (só ela e marido)
├── Smartphone: 74% (Android 95%)
└── Digital literacy: Baixa

Jornada de Compra:
├── Sábado: Feira livre (R$ 60)
├── Quarta: Supermercado de bairro (R$ 80)
├── Diário: Padaria (R$ 20)
└── Apps: WhatsApp, YouTube, Facebook (NÃO usa lista digital)

Gatilhos de Desperdício:
├── Letra pequena nos rótulos (não lê)
├── Geladeira antiga (organização ruim)
├── "Eu lembro que comprei... onde está?"
└── Marido que não ajuda na cozinha

WTP: R$ 0 (só adere via família ou B2G)
Sensibilidade: Simplicidade extrema, indicação da filha
```

### 3.2 Categorias Prioritárias de Desperdício

| Categoria | % Orçamento | Risco Desperdício | App Pode Resolver? |
|-----------|------------|-------------------|-------------------|
| Carnes | 23% | Alto (validade curta) | Parcialmente |
| Hortifruti | 16% | **Muito Alto** (40-50% famílias) | ✅ SIM |
| Laticínios | 12% | Alto | ✅ SIM |
| Panificados | 9% | **Muito Alto** (validade curta) | ✅ SIM |
| Básicos (arroz, feijão) | 8% | Médio (sobras) | ✅ SIM |

**MVP Priority:** Foco em hortifruti + panificados + laticínios.

---

## 4. ANÁLISE COMPETITIVA

### 4.1 Mapa de Players Globais e Brasil

| Player | Modelo | Focus | Tecnologia | Brasil | TAM |
|--------|--------|-------|------------|--------|-----|
| Too Good To Go | Marketplace | Comercial | Moderada | ❌ Não opera | USD 105M |
| OLIO | Gratuito + B2B | **Doméstico** | Baixa | ❌ Não opera | < USD 10M |
| Food To Save | Marketplace | Comercial | Moderada | ✅ Líder BR | R$ 72M |
| Comida Invisível | B2B SaaS | Rastreabilidade | Alta | ✅ McDonald's BR | ~R$ 4M |
| Karma | B2B SaaS | Restaurantes | AI (KAIA) | ❌ Não opera | N/D |
| Nosh | Freemium | Household | **AI/OCR** | ❌ UK only | N/D |
| Yindii | Marketplace | Comercial | Gamificação | ❌ Não opera | N/D |

### 4.2 Quadrante Competitivo (Por que Waste Guardian é Blue Ocean)

```
                            Tech sophistication (AI/OCR/Gamificação)
                            Low                              High
                            
Foco    High     OLIO                        WASTE GUARDIAN
Desper-           (baixo tech,               (ALTO TECH +
dício             alto focus domestico)       ALTO FOCUS DOMÉSTICO)
Domés-                                              ← BLUE OCEAN
tico
                            
                             Food To Save              Comida Invisível
                             (médio tech,             (médio tech,
                              baixo focus domestico)   baixo focus domestico)

Foco    Low      Phenix, Flashfood            Too Good To Go
Desper- (baixo tech,                   (alto tech,
dício    baixo focus domestico)         baixo focus domestico)
Comerc.
```


### 🔲 Onde o Waste Guardian Se Posiciona

```mermaid
flowchart TB
    AXIS["Eixo X: foco (baixo → alto)<br/>Eixo Y: sofisticação tecnológica (baixa → alta)"]
    AXIS --- H1["Alto foco / Alta tech<br/>★ WASTE GUARDIAN<br/>household + AI + gamificação + PT-BR"]
    AXIS --- H2["Alto foco / Média tech<br/>Comida Invisível (B2B SaaS)"]
    AXIS --- H3["Baixo foco / Alta tech<br/>Too Good To Go"]
    AXIS --- H4["Baixo foco / Média tech<br/>Food To Save"]
    AXIS --- H5["Alto foco / Baixa tech<br/>OLIO"]
```

**Leitura:** o quadrante vazio é **household + AI + PT-BR**. É uma janela de 12-18 meses antes que um player global entre com IA — não uma barreira técnica permanente.

### 4.3 Diferencial Único do Waste Guardian

**Waste Guardian é o ÚNICO app no mundo que combina:**
1. ✅ Foco em desperdício DOMÉSTICO (não comercial)
2. ✅ AI Scanner para detectar validade (NLP)
3. ✅ Gamificação (rankings, badges, missões)
4. ✅ Mercado Brasileiro (PT-BR, PIX, cultura local)
5. ✅ Conexão com rede de doação (via Comida Invisível)

**Nenhum player global tem os 5 juntos.** A janela de 12-18 meses antes que TGTG ou OLIO entrem no Brasil é real.

### 4.4 Análise SWOT

| FORÇAS | FRAQUEZAS |
|--------|-----------|
| Blue ocean (nenhum competitor BR) | Zero tração (protótipo Figma) |
| 94 kg/pessoa dado robusto | Sem rede de parceiros |
| Alinhamento COP30 + ODS 12.3 | Time desconhecido (precisa orientadora) |
| Lei 14.016 vigente (compliance) | MVP não construído ainda |
| 615 métricas de research | Não há dado de impacto real |

| OPORTUNIDADES | AMEAÇAS |
|--------------|---------|
| TGTG/OLIO não operam no Brasil | TGTG entrar no Brasil com AI |
| Comida Invisível como parceiro (20K ONGs) | Food To Save adicionar AI |
| Mercado em crescimento 5,5% CAGR | Grandes varejistas lançarem solução própria |
| COP30 visibilidade ODS | Execução em 12 semanas |

---

## 5. MODELO DE RECEITA — ANÁLISE PROFUNDA

### 5.1 O Que Nós Recomendamos (B2B como Receita Principal)

**Não é "empresa patrocina para famílias usarem". É "empresa paga por dados e inteligência."**


### 5.2 6 Modelos B2B Explicados Detalhadamente

### 🔀 Arquitetura de Dados e Receita — Qual modelo se apoia em quê

```mermaid
flowchart LR
    subgraph ENTRADA["Fontes de dado"]
        S1["POS / ERP do supermercado"]
        S2["Escaneamento do consumidor<br/>(parcial, não-B2B)"]
    end
    S1 --> W["Waste Guardian<br/>coleta, agrega, classifica"]
    S2 -.->|"sinal fraco<br/>não sustenta o B2B"| W
    W --> O1["Dashboard de waste<br/>(B2B Supermarkets)"]
    W --> O2["Insight as a Service<br/>(B2B Brands)"]
    W --> O3["Consumer Premium<br/>(WhatsApp)"]
    W --> O4["Matching de doação<br/>(I2C)"]
```

**Leitura:** apenas o ramo do supermercado alimenta os dois quadrantes que carregam 80%+ da receita. O ramo do consumidor é dependência **parcial** — nunca foi a base do B2B.

#### Modelo 1: DATA AS A SERVICE (Supermercados)
```
O QUE É:
├── WG coleta dados ANÔNIMOS de escaneamentos
├── Agrega: "Clientes estão jogando fora 40% mais iogurte que pão"
├── Vende: Relatório mensal de insights para supermercados
└── Preço: R$ 2.000-5.000/mês por estabelecimento

EXEMPLO CONCRETO:
Um supermercado parceira (Pão de Açúcar, Carrefour, etc):
├── Paga R$ 3K/mês por acesso ao dashboard
├── Recebe: Quais produtos expiram mais, quando, por quê
├── Ação: Repositiona produtos, ajusta markdowns, otimiza estoque
├── ROI: Poupa R$ 50K/mês em desperdício reduzido
└── Custo do dado: R$ 3K = 6% do retorno

POR QUE COMPANHIA PAGA:
├── Reduzir perdas na loja (5-15% do inventory)
├── Dados para negociar melhor com fabricantes
├── Métricas ESG próprias para Relatório de Sustentabilidade
└── "Landing page" para consumidores (QR code no produto)
```

#### Modelo 2: INSIGHT AS A SERVICE (Marcas de Alimentos)
```
O QUE É:
├── WG sabe quais RECEITAS estão sendo feitas com quais produtos
├── Agrega: "Mulheres de 35-50 anos estão descartando banana porque não sabem o que fazer com 2 bananas"
├── Vende: Insights de comportamento do consumidor para marcas
└── Preço: R$ 5.000-15.000/mês por marca

EXEMPLO CONCRETO:
Nestlé Brasil (exemplo):
├── Paga R$ 10K/mês por insights sobre iogurte natural
├── Recebe: Clientes descartam iogurte 3 dias antes da validade
├── Insight: Embalagem grande demais para famílias pequenas
├── Ação: Criar linha "porção única" ou "2 unidades"
├── ROI: Vendas + redução de descarte = R$ 200K/mês
└── Custo do dado: R$ 10K = 5% do retorno
```

#### Modelo 3: COMPLIANCE AS A SERVICE (Bancos/Instituições)
```
O QUE É:
├── Empresas precisam reportar ODS 12.3 (meta ONU: reduzir 50% desperdício até 2030)
├── WG fornece: Dashboard de impacto social com métricas auditáveis
├── Vende: Assinatura + fee de compliance reporting
└── Preço: R$ 3.000-8.000/mês

EXEMPLO CONCRETO:
Itaú Unibanco (exemplo):
├── Paga R$ 5K/mês por "Programa de Sustentabilidade para Funcionários"
├── Funcionários usam app para rastrear desperdício em casa
├── WG gera relatório: "12.500 funcionários evitaram R$ 2.3M em desperdício"
├── Itaú reporta: "Impacto social de R$ 2.3M" no Relatório de Sustentabilidade
├── ROI para Itaú: R$ 5K = exposição de marca + compliance ODS
└── Custo para Itaú: Menor que uma Campanha de Marketing
```

#### Modelo 4: API AS A SERVICE (Plataformas/Integradores)
```
O QUE É:
├── WG abre API para integrations
├── iFood, Mercado Livre, Rappi pagam para integrar scanner
├── Vende: Fee por API call ou por transação
└── Preço: R$ 0,50-2,00 por transação integrada

EXEMPLO CONCRETO:
iFood (integração potencial):
├── iFood integra scanner WG no app
├── Cliente escaneia produto do Supermercado
├── Dado: "Cliente compra iogurte 2x/semana, descarta 40%"
├── iFood melhora: Recomendações + targeted offers
├── WG recebe: R$ 0,50 por escaneamento
├── Volume: 100K escaneamentos/mês = R$ 50K/mês
└── iFood paga: Menos que custo de Churn
```

#### Modelo 5: REFERRAL FEE (Marketplace de Doação)
```
O QUE É:
├── WG conecta: Família com produto próximo da validade → ONG que precisa
├── Quando match ocorre: Taxa sobre valor do produto doado
└── Preço: 15-25% do valor de mercado do produto

EXEMPLO CONCRETO:
Família doa iogurte de R$ 8,90:
├── WG conecta com Banco de Alimentos SP
├── Banco recebe iogurte (distribui para população carente)
├── WG cobra: R$ 1,78 (20% do valor)
├── Custo para família: ZERO
├── Custo para ONG: ZERO
└── Volume: 10K doações/mês × R$ 8,90 = R$ 89K × 20% = R$ 17,8K/mês
```

#### Modelo 6: ENTERPRISE LICENSE (Grandes Fabricantes)
```
O QUE É:
├── Versão white-label do app para grandes marcas
├── "Marca X: Gestão de Desperdício para Seus Clientes"
├── Inclui: Branding, dashboard customizado, integrações
└── Preço: R$ 50.000-200.000/ano

EXEMPLO CONCRETO:
Danone Brasil (exemplo):
├── Compra licença enterprise por 1 ano: R$ 120K
├── Renova licença "Lançamento Sustentável 2027"
├── Clientes Danone recebem app personalizado
├── WG tem: Receita garantida + dados de marca
└── Danone tem: Diferencial competitivo + compliance ODS
```

### 5.3 Mix de Receita Realista (Ano 3)

| Modelo | % Receita | Valor Ano 3 | Clientes |
|--------|-----------|-------------|----------|
| Data as a Service (Supers) | 30% | R$ 1,5M | 50 |
| Insight as a Service (Marcas) | 25% | R$ 1,25M | 25 |
| Compliance as a Service (Bancos) | 20% | R$ 1M | 40 |
| API as a Service (Plataformas) | 15% | R$ 750K | 5 |
| Referral Fee (Doação) | 10% | R$ 500K | — |

| **TOTAL** | **100%** | **R$ 5M** | **120** |

> **Reconciliação com o quadro canônico (v4.0 §15.1):** os 6 modelos acima são a **decomposição operacional** do mesmo revenue pool; o **split canónico é o de 4 quadrantes** (B2B Supermarkets / B2B Brands / Consumer Premium / Donation-I2C) definido na narrativa v4.0 e materializado na projeção do pitch. "Compliance as a Service" e "API as a Service" são extensões dentro de B2B, não quadrantes separados, e o Consumer Premium (B2C) entra no quadro canónico à parte (faixa 10-15%).

### 5.4 Por Que B2B é Mais Estável que B2C

| Aspecto | B2C | B2B |
|---------|-----|-----|
| Ticket médio | R$ 9,90/mês | R$ 3.000-15.000/mês |
| Churn | Alto (60-80% em 3 meses) | Baixo (contrato anual) |
| Ciclo de venda | Curto (app store) | Médio (3-6 meses) |
| Receita previsível | Volátil | Contrato garantido |
| Custo de aquisição | Alto (R$ 8-25/user) | Alto (R$ 5-15K/venda) |
| Satisfação do cliente | Variável | Alta (pagador ≠ usuário) |

**Resumo:** B2C tem escala mas volatilidade. B2B tem estabilidade mas exige venda consultativa. O ideal é AMBOS.

---

## 6. ANÁLISE REGULATÓRIA

### 6.1 Marco Legal Brasileiro

| Lei | Ano | Descrição | Impacto |
|-----|-----|-----------|---------|
| Lei 14.016 | 2020 | Marco de Doação de Alimentos | Remove responsabilidade civil do doador de boa-fé |
| Lei 15.224 | 2025 | II Estratégia PDA | Meta de reduzir 50% desperdício até 2030 |
| PNRS | 2010 | Política Nacional de Resíduos Sólidos | Hierarquia de gestão (prevenção → reciclagem → descarte) |

### 6.2 Lei 14.016/2020 — Detalhamento

```
PROTEÇÕES:
├── Doador de boa-fé ISENTO de responsabilidade civil e penal
├── Requisitos: Alimento próprio para consumo humano
├── Documentação: Nota fiscal + termo de doação
├── Limite dedução: 2% do lucro operacional
└── Não exige seguro para alimentos doados

OBRIGAÇÕES:
├── Alimento dentro do prazo de validade
├── Transporte adequado (cold chain se necessário)
├── Receitas: Entidades de assistência social cadastradas
└── Registrar: Quem doou, o quê, quando, para quem

O QUE A LEI NÃO COBRE:
├── Alimentos fora do prazo de validade
├── Produtos sem nota fiscal
├── Veículos de entrega inadequados
└── Alimentação preparada (restaurantes)
```

### 6.3 COP30 e Contexto Global

```
Brasil sediará COP30 em 2025 (Belém/PA)
├── ODS 12.3: "Até 2030, reduzir pela metade o desperdício global de alimentos"
├── Meta ratificada por 193 países
├── Brasil: Signatário + membro Champions 12.3
└── Oportunidade: Empresas precisam mostrar ação para cumprir metas

MOMENTO BRASILEIRO:

├── Lei 14.016 existe desde 2020 (faltava execução)
├── II Estratégia PDA (2025): Meta formalizada
├── COP30: Visibilidade global para quem age primeiro
└── Janela: Empresas que começarem agora serão as "pioneiras" no Brasil
```

---

## 7. ANÁLISE DOS 7 GAPS CRÍTICOS

### 7.1 Gap 1: Mapa de ONGs de Redistribuição 🔴 ALTA


**O que sabemos:**
- Comida Invisível: 20K ONGs, 2K ativas, 13M refeições redistribuídas
- Banco de Alimentos SP: ~50 toneladas/mês

**O que não sabemos:**
- Volume real processado pelo **Mesa Brasil Sesc**: a estimativa de 15.000-20.000 **toneladas/ano** (não toneladas/mês) **não foi verificada** por fonte primária — ver narrativa v4.0 §6.1
- Qual o volume real que ONGs precisam?
- Qual o custo logístico por kg coletado?
- Quais alimentos as ONGs NÃO estão conseguindo?

**Ação:**Mapear 10-20 ONGs via LinkedIn + Google para validar demanda real.

### 7.2 Gap 2: Willingness to Pay Específico 🔴 ALTA

**Dados que temos:**
- WTP Consumer: R$ 9,90/mês (benchmark + renda)
- 60-80% da receita vem de B2B, não assinatura
- SAM B2C: R$ 400M (mas dependemos de 8% willing to pay)

**Análise de sensibilidade:**
| Cenário | WTP | SAM B2C |
|---------|-----|---------|
| Otimista | 15% | R$ 400M |
| Realista | 8% | R$ 181M |
| Conservador | 3% | R$ 68M |

**Decisão:** Aceitar incerteza; focar receita em B2B.

### 7.3 Gap 3: Dados Setoriais Brasileiros 🟡 MÉDIA

**Problema:** Brasil não tem dados oficiais desagregados por segmento.
**Solução:** Usar proxy UNEP 60/28/12 com disclaimer.

### 7.4 Gap 4: Série Temporal 🟡 MÉDIA

**Problema:** Não existe série histórica brasileira de desperdício.
**Solução:** Usar exemplos de países que mediram (UK -18%, Japão -31%).

### 7.5 Gap 5: LTV/CAC Official 🟡 MÉDIA

**Problema:** Players não divulgam números.
**Solução:** Usar benchmark 3-5x para consumer freemium.

### 7.6 Gap 6: Modelo I2C (Industry-to-Charity) 🔴 CRÍTICA

**Análise:**
```
MODELO I2C:
Fábrica (excedentes) → WG (matching) → ONG → População carente

VIABILIDADE:
├── ONGs já fazem redistribuição (Comida Invisível: 13M refeições)
├── Lei 14.016 protege doador de boa-fé
├── Tax incentive: 2% dedução sobre lucro operacional
└── Gap: Logística e rastreamento

PARA O MVP DLJ4:
├── NÃO é viável como MVP (exige infraestrutura)
├── É viável como ROADMAP (Fase 2-3)
├── Pré-requisito: Validação com Comida Invisível primeiro
└── Recomendação: Incluir no pitch como visão de longo prazo
```

### 7.7 Gap 7: Impacto Social Demonstrável 🔴 CRÍTICA

**Problema:** Métricas de impacto dependem de uso real do app.
**Solução:** Criar projeção baseada em dados Embrapa:
```
Se 1.000 famílias usassem o app por 1 mês:
├── Desperdício evitado: ~150 kg/mês
├── Economia por família: ~R$ 125/mês
├── CO₂ evitado: ~250 kg/mês
└── Total economia: R$ 125.000/mês
```
**Disclaimer:** Projeção baseada em dados Embrapa; validação real após piloto.

---

## 8. RECOMENDAÇÕES ESTRATÉGICAS

### 8.1 Proposta de Valor Refatorada

**De:** "Escaneie, receita, doe, salve o planeta"
**Para:** "Poupe R$ 100-200 por mês em comida que você ia jogar fora"

**Justificativa (dados):**
- R$ 100-150/mês perdido por família (Batch 01)
- Gatilho monetário > gatilho ideológico (Batch 04)
- WTP funciona quando há ROI direto (Benchmark)


### 8.2 Mix de Receita Recomendado (quadro canônico v4.0 §15.1)

| Prioridade | Fonte (quadrante canônico) | % Ano 1 | ARR Ano 1 | % Ano 3 | ARR Ano 3 |
|------------|---------------------------|----------|-----------|----------|-----------|
| 🥇 1 | B2B Supermarkets — Data as a Service | 67,3% | R$ 1,20M | 60-70% | R$ 3,0-3,5M |
| 🥈 2 | B2B Brands — Insight as a Service | 20,2% | R$ 360K | 20-30% | R$ 1,0-1,5M |
| 🥉 3 | Consumer Premium (R$ 9,90/mês) | 10,0% | R$ 178K | 10-15% | R$ 500-750K |
| 4 | Donation/I2C — Referral Fee | 2,5% | R$ 44K | ~5% | R$ 250K |
| | **TOTAL** | **100%** | **R$ 1,782M** | **100%** | **R$ 5M** |

> **Reconciliação com o quadro canônico:** a taxonomia de 4 quadrantes substitui a de 4 linhas de receita da v2.0 (55/25/15/5). O **split canónico é o da narrativa v4.0** (B2B Supermarkets / B2B Brands / Consumer Premium / Donation-I2C). O Ano 1 vem da projeção do pitch: **R$ 148.500/mês = R$ 1.782.000 ARR** (os valores por quadrante na tabela estão arredondados; a soma exata é R$ 1.782.000).


### 8.3 Roadmap de 3 Anos (alinhado ao quadro canônico v4.0)

```mermaid
flowchart LR
    A1["Ano 1<br/>MVP + validação B2B<br/>R$ 1,782M ARR"] --> A2["Ano 2<br/>Validação e escala<br/>R$ 3M ARR"] --> A3["Ano 3<br/>Escala LATAM + I2C<br/>R$ 5M ARR"]
```

```
ANO 1 (Fase MVP + Validação B2B):
├── MVP: Dashboard de waste + alertas de validade (B2B)
├── Piloto: 1-2 redes de supermercado (5-10 lojas) + 50 famílias
├── Base do cenário: 10 redes × 5 lojas × R$ 2.000/loja
├── Validação: 2-3 entrevistas com gestores + 1º contrato B2B
└── Receita: R$ 1,782M ARR (R$ 148,5K/mês — canônico v4.0 / pitch)

ANO 2 (Fase Validação):
├── Expansão: 5.000-10.000 famílias
├── 10-20 parceiros B2B
├── Integração: Comida Invisível (20K ONGs)
├── Lançamento: API para plataformas
└── Receita: R$ 3M ARR

ANO 3 (Fase Escala):
├── 50.000+ famílias
├── 50+ parceiros B2B
├── Integração: Excedentes industriais (I2C)
├── Expansão: LATAM (português/espanhol)
└── Receita: R$ 5M ARR
```

> **Nota:** o Ano 1 foi corrigido de R$ 250K ARR para **R$ 1,782M ARR**. O valor anterior vinha da taxonomia de receita da v2.0 (55/25/15/5) e não fechava com a projeção do pitch. O Ano 1 canónico é o da narrativa v4.0: **R$ 148.500/mês**.

---

## 9. ANÁLISE DE RISCOS

### 9.1 Riscos de Mercado

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| TGTG entrar no Brasil | Média | Alto | Primeiro-mover advantage + relationships |
| Food To Save adicionar AI | Alta | Médio | Diferenciar em household focus |
| Varejistas criarem solução própria | Baixa | Alto | Parceria em vez de competição |

### 9.2 Riscos de Execução

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| MVP não ficar pronto | Alta | Crítico | Focar no essencial |
| Orientadora não inscrita | Crítica | Crítico | Resolver IMEDIATAMENTE |
| Não validar PMF | Alta | Alto | Medir desde o dia 1 |

### 9.3 Riscos Financeiros

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| SAM superestimado (WTP < 8%) | Média | Alto | B2B como receita primária |
| Churn B2C alto (>60%) | Alta | Médio | Focar B2B estável |
| Ciclo B2B longo (>6 meses) | Alta | Médio | Começar vendas agora |

---

## 10. CONCLUSÃO

### 10.1 Caso para Continuar

**Por que o Waste Guardian NÃO é um projeto moribundo:**

1. **Mercado existe e é validado:** TAM USD 75-87 bi, CAGR 5,5%, Brasil R$ 22 bi
2. **Blue ocean real:** Nenhum player combina household + AI + gamificação no mundo
3. **Regulação a favor:** Lei 14.016 + COP30 + ODS 12.3
4. **Receita viável:** B2B pode ser R$ 2-5M em 3 anos sem depender de WTP consumer
5. **Dados sólidos:** 615 métricas, 112 fontes, 8 batches completos
6. **Janela de tempo:** TGTG e OLIO não operam no Brasil — 12-18 meses de vantagem

### 10.2 O Que Precisa para Ganhar

| Requisito | Status | Prioridade |
|-----------|--------|------------|
| MVP funcional (scanner + receitas) | ⚠️ Parcial | 🔴 CRÍTICA |
| Orientadora inscrita no portal | ❌ Falta | 🔴 CRÍTICA |
| Pitch com valor claro (poupança R$) | ⚠️ Parcial | 🔴 CRÍTICA |
| 1 partnership B2B validada | ❌ Falta | 🟡 ALTA |
| Dados de impacto (mesmo que projetados) | ⚠️ Parcial | 🟡 ALTA |

### 10.3 Próximo Passo Imediato

**Se você tiver que escolher apenas UMA coisa para fazer agora:**

> **"Crie um slide que mostre: Se 1.000 famílias usassem o app por 1 mês, poupariam R$ 125.000 e evitariam 250kg de CO₂. Esse é o poder do Waste Guardian."**

Isso é tangível, fundamentado nos dados, e mostra que você entendeu o problema.

---

*Documento gerado: 2026-06-12*
*Versão: 2.0*
*Base: 615 métricas, 112 fontes, 8 batches*
*Status: PRONTO PARA ATUALIZAR PITCH*
