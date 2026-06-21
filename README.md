# Miniguia de Educação Financeira Pessoal — NotebookLM

> Projeto prático da [DIO](https://www.dio.me/) — uso de Inteligência Artificial como ferramenta de aprendizagem ativa, com curadoria de fontes oficiais, engenharia de prompts e organização do conhecimento em um caderno temático no NotebookLM.

**Tema:** Educação Financeira Pessoal — reserva de emergência, dívidas e primeiros investimentos

**Ferramenta:** [Google NotebookLM](https://notebooklm.google.com/)

---

## 1. Contexto e Objetivos

### Contexto

Muitas pessoas querem começar a organizar as finanças e investir, mas se perdem entre informações contraditórias nas redes sociais. Este projeto usa o NotebookLM como "assistente de estudo" ancorado em **5 PDFs oficiais** do Banco Central, da CVM e da B3 — não em opiniões aleatórias.

A ideia é tratar a IA como parceira de **aprendizagem ativa**: eu formulo perguntas, valido as respostas nas fontes, registro o que funcionou (e o que não funcionou) e consolido um miniguia reutilizável.

### Objetivos de estudo

Ao final deste caderno temático, busquei:

1. **Entender a ordem lógica** das finanças pessoais: orçamento → controle de dívidas → reserva de emergência → investimentos
2. **Diferenciar conceitos fundamentais** (poupança vs. investimento, juros simples/compostos, inflação, risco)
3. **Saber montar uma reserva de emergência** com critérios objetivos (quanto guardar e onde alocar)
4. **Reconhecer riscos ao investir** (golpes, churning, suitability, senhas, intermediários não autorizados)
5. **Usar crédito de forma consciente** e evitar o superendividamento
6. **Construir um repertório de prompts** para revisar o tema no futuro

---

## 2. Curadoria de Fontes

| # | Documento | Instituição | O que contribui ao caderno |
|---|-----------|-------------|------------------------------|
| 1 | [Caderno de Educação Financeira](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/Cuidando_do_seu_dinheiro_Gestao_de_Financas_Pessoais/caderno_cidadania_financeira.pdf) | BCB | Base completa: 6 módulos (dinheiro, orçamento, crédito, consumo, poupança/investimento, riscos) |
| 2 | [TOP Planejamento Financeiro Pessoal](https://www.gov.br/investidor/pt-br/educacional/publicacoes-educacionais/livros-cvm/livro-top-planejamento-financeiro-pessoal/@@display-file/file) | CVM + Planejar | Visão integrada: gestão financeira, investimentos, aposentadoria, seguros, tributos e sucessão |
| 3 | [Cartilha BSM para o Investidor](https://www.b3.com.br/data/files/30/23/29/45/F5B738101E311E28AC094EA8/bsm-cartilha-do-investidor-2022.pdf) | B3 / BSM | Proteção do investidor: senhas, suitability, AAI, churning, canais de reclamação |
| 4 | [Jornada da Cidadania Financeira](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/Informacoes_gerais/jornada_educacao_financeira.pdf) | BCB | Contexto histórico: inclusão + proteção + educação financeira no Brasil |
| 5 | [Guia de Excelência — Operações de Crédito](https://www.bcb.gov.br/content/cidadaniafinanceira/documentos_cidadania/guia_de_excelencia/guia_de_excelencia_oferta_de_produtos_servi%C3%A7os_financeiros.pdf) | BCB | Crédito responsável: publicidade, contratação, pós-venda e cartão de crédito |

Links detalhados também em [`fontes/README.md`](fontes/README.md).

---

## 3. Engenharia de Prompts e "Cicatrizes"

Registro das perguntas estratégicas testadas no NotebookLM, variações de prompts, respostas obtidas, referências e dificuldades encontradas.

### 3.1 Perguntas estratégicas iniciais

| # | Pergunta estratégica | Objetivo |
|---|---------------------|----------|
| 1 | Qual a ordem correta para organizar finanças pessoais antes de investir? | Mapear a jornada completa |
| 2 | Como calcular e onde guardar a reserva de emergência? | Aplicar conceito na prática |
| 3 | Quais são os principais tipos de investimento para iniciantes no Brasil? | Comparar opções com segurança |
| 4 | Como usar crédito sem cair no superendividamento? | Entender juros e endividamento |
| 5 | Quais cuidados tomar ao abrir conta em corretora? | Proteção no mercado de capitais |

### 3.2 Prompts testados no NotebookLM (com respostas reais)

> Todas as respostas abaixo foram geradas no [NotebookLM](https://notebooklm.google.com/) a partir dos 5 PDFs carregados no caderno temático.

#### Prompt 1 — Resumo estruturado ✅ Funcionou na primeira tentativa

**Prompt enviado:**
```
Com base APENAS nas fontes carregadas, crie um resumo estruturado sobre educação
financeira pessoal para iniciantes, com: (1) ordem de prioridades, (2) erros comuns,
(3) conceitos-chave. Cite a fonte de cada item entre colchetes.
```

**Resposta obtida (trecho consolidado):**

O NotebookLM estruturou a resposta em três blocos. Destaques:

**Ordem de prioridades identificada:**
1. Educação financeira e autoconhecimento
2. Diagnóstico e planejamento (orçamento)
3. Eliminação de dívidas e equilíbrio (orçamento superavitário)
4. Formação da reserva de emergência (regra "pague-se primeiro", 3–6 meses de despesas)
5. Definição de projetos de vida (metas concretas)
6. Investimento e aposentadoria (juros compostos)
7. Proteção do patrimônio (seguros)

**Erros comuns listados:** procrastinar o planejamento, gastar mais do que ganha, confundir necessidade com desejo, esperar sobrar dinheiro para poupar, uso indevido do crédito rotativo, cair no "marketing de sedução", ignorar o CET, negligenciar segurança cibernética.

**Conceitos-chave:** orçamento, troca intertemporal, custo de oportunidade, juros compostos, CET, suitability, tripé dos investimentos (liquidez/risco/rentabilidade), consumo consciente, zeragem compulsória.

**Avaliação:** Resposta densa e bem organizada. As fontes foram citadas de forma implícita no corpo do texto. O fluxo de 7 etapas ficou mais completo do que o esperado — incluiu aposentadoria e seguros além do básico.

**Fontes mais citadas:** *Caderno de Educação Financeira* (BCB) e *Livro TOP Planejamento Financeiro Pessoal* (CVM).

---

#### Prompt 2 — Comparativo de investimentos ✅ Funcionou com prompt refinado

**Versão 1 (testada antes — resposta superficial):**
```
Compare poupança, CDB e Tesouro Direto.
```
**Cicatriz:** Resposta genérica, sem tabela, sem detalhes de tributação ou FGC.

**Versão 2 (prompt usado — funcionou):**
```
Usando SOMENTE as fontes deste notebook, compare poupança, CDB e Tesouro Direto
em uma tabela com: liquidez, risco, rentabilidade (como descrita nas fontes),
perfil indicado e limitações. Se alguma informação não estiver nas fontes,
escreva "não encontrado nas fontes".
```

**Resposta obtida:**

| Característica | Caderneta de Poupança | CDB | Tesouro Direto |
| :--- | :--- | :--- | :--- |
| **Liquidez** | Diária, rendimentos no aniversário | Variável; pode ter liquidez diária ou carência | Alta; Tesouro Selic para liquidez diária |
| **Risco** | Baixo; FGC até R$ 250 mil/CPF/instituição | Risco de crédito do banco; FGC até o limite | Menor risco (governo); risco de mercado em prefixados/IPCA na venda antecipada |
| **Rentabilidade** | TR + 0,5% a.m. (Selic > 8,5%) ou TR + 70% Selic (Selic ≤ 8,5%) | Prefixada ou pós-fixada (% CDI ou Selic) | Selic, prefixada ou IPCA conforme o título |
| **Perfil** | Conservador | Conservador (emissores sólidos) | Conservador (Selic); IPCA/Prefixados podem ser moderados ou arrojados |
| **Limitações** | Penaliza saques fora do aniversário; menor rentabilidade | IR regressivo + IOF antes de 30 dias | IR, IOF, taxa B3; venda antecipada pode gerar perdas |

**Detalhes adicionais da resposta:**
- Poupança e CDB protegidos pelo **FGC** (R$ 250 mil); Tesouro sem FGC, mas garantido pelo Tesouro Nacional
- Poupança isenta de IR; CDB e Tesouro seguem **tabela regressiva de IR** (22,5% até 180 dias → 15% acima de 720 dias)
- Reserva de emergência: **Tesouro Selic** e **CDB DI com liquidez diária**

**Avaliação:** Excelente. A restrição "somente fontes" + formato tabela gerou resposta comparável a material de curso.

---

#### Prompt 3 — Cenário prático ✅ Funcionou muito bem

**Prompt enviado:**
```
Simule o caso de uma pessoa com renda de R$ 4.000, dívidas no cartão rotativo
e sem reserva. Com base nas fontes, proponha um plano em 4 etapas com prazos
sugeridos. Indique qual fonte embasa cada etapa.
```

**Resposta obtida:**

| Etapa | Prazo | Ação principal | Fontes |
|-------|-------|----------------|--------|
| 1 — Diagnóstico | 1ª semana | Mapear dívida (valor, prazo, taxa do rotativo) + registrar receitas/despesas | Caderno BCB + TOP CVM |
| 2 — Estancar dívida | 1º mês | Parar uso do cartão; renegociar ou portabilidade para crédito mais barato (pessoal/consignado) | Caderno BCB + Guia de Excelência + TOP CVM |
| 3 — Orçamento superavitário | Meses 1–3 | Cortar supérfluos; manter endividamento < 30% da renda (máx. R$ 1.200 em parcelas) | TOP CVM + Caderno BCB |
| 4 — Reserva de emergência | Meses 3–12 | "Pague-se primeiro"; meta de R$ 12.000–R$ 24.000 em Tesouro Selic ou CDB DI | TOP CVM + Caderno BCB |

**Avaliação:** Resposta aplicável e com números concretos. O NotebookLM cruzou bem as fontes de crédito (Guia de Excelência) com planejamento (TOP CVM).

---

#### Prompt 4 — Glossário ✅ Funcionou na primeira tentativa

**Prompt enviado:**
```
Liste os 15 conceitos financeiros mais importantes para iniciantes encontrados
nas fontes. Para cada um: definição em 1 frase, exemplo prático e fonte.
```

**Resposta obtida (15 conceitos):**

1. **Educação Financeira** — processo de compreensão de produtos e riscos financeiros
2. **Orçamento** — ferramenta que registra rendas e gastos para equilibrar a vida financeira
3. **Troca Intertemporal** — escolha entre consumir agora (pagando juros) ou poupar para o futuro
4. **Custo de Oportunidade** — benefício renunciado ao fazer uma escolha
5. **Juros Compostos** — juros sobre juros; crescimento exponencial no tempo
6. **Reserva de Emergência** — poupança separada para imprevistos (6 meses de despesas em Tesouro Selic)
7. **CET** — taxa real do empréstimo incluindo juros, tarifas e encargos
8. **Orçamento Superavitário** — receitas > despesas (ex.: R$ 4.000 de renda, R$ 3.500 de gastos, R$ 500 de sobra)
9. **Suitability** — adequação do produto ao perfil e tolerância ao risco do investidor
10. **Liquidez** — facilidade de converter investimento em dinheiro sem perda
11. **Rentabilidade** — retorno esperado sobre o capital investido
12. **Risco** — probabilidade de perdas financeiras
13. **Patrimônio Líquido** — bens e direitos menos dívidas (ex.: carro R$ 40 mil − financiamento R$ 24 mil = R$ 16 mil)
14. **Crédito** — recurso de terceiros com obrigação futura de pagamento + juros
15. **Diversificação** — distribuir recursos em diferentes investimentos para reduzir risco

**Avaliação:** Cada conceito veio com exemplo prático — ideal para fixação. Termos como *suitability* e *diversificação* mostraram integração entre B3, CVM e BCB.

---

#### Prompt 5 — Proteção do investidor ✅ Excelente (Cartilha B3 bem aproveitada)

**Prompt enviado:**
```
Quais são os principais riscos e cuidados ao investir no mercado de capitais
segundo as fontes? Organize em: segurança digital, intermediários, taxas e
práticas abusivas. Cite exemplos mencionados nas fontes.
```

**Resposta obtida (resumo por categoria):**

**Segurança digital:** senha individual e forte, nunca compartilhar; antivírus/firewall atualizados; autenticação de dois fatores; evitar redes públicas; trocar senha e avisar corretora se suspeitar de uso indevido.

**Intermediários:** verificar registro na CVM/BCB; investidor preenche cadastro e suitability sozinho; AAIs não fazem consultoria nem emitem ordens sem comando; consultores/AAIs não podem ser procuradores.

**Taxas:** exigir transparência (administração, custódia, performance, impostos); comparar pelo CET; conhecer taxas de zeragem compulsória; monitorar custo vs. rendimento.

**Práticas abusivas:** churning (excesso de operações para gerar corretagem); indução de perfil de risco; promessas de lucro garantido; marketing de sedução (urgência/escassez); registrar falhas de plataforma com evidências.

**Avaliação:** Resposta mais rica de todas — a Cartilha BSM (B3) foi a fonte dominante, complementada pelo Caderno BCB.

---

### 3.3 Troubleshooting — dificuldades e soluções

| Dificuldade | O que aconteceu | Solução aplicada |
|-------------|-----------------|------------------|
| Prompt vago no comparativo | "Compare poupança, CDB e Tesouro" gerou resposta superficial | Refinar com tabela, restrição "somente fontes" e campo "não encontrado" |
| PDF da CVM muito grande (~314 pág.) | Upload demorado; notebook pesado | Funcionou bem com prompts direcionados; para refinamentos, citar capítulo específico |
| Citações de fonte inconsistentes | Prompt 1 pediu colchetes, mas NotebookLM citou por nome do documento | Aceitável — nomes dos PDFs já identificam a fonte; para rigor, repetir "cite página ou módulo" |
| Sobreposição entre fontes BCB | Caderno e Guia de Excelência repetem temas de crédito | Direcionar: Guia para *contratação de crédito*; Caderno para *finanças do dia a dia* |
| Link CVM com `@@display-file` | Em alguns ambientes retorna HTML em vez de PDF | Baixar pelo navegador e fazer upload local no NotebookLM |

### 3.4 Lições aprendidas sobre engenharia de prompts

1. **Prompts com formato explícito** (tabela, etapas, glossário) geram respostas muito superiores
2. **Cenários com números reais** (R$ 4.000, 30% endividamento) fixam melhor o conteúdo
3. **Restringir às fontes** é essencial em temas financeiros — evita "dicas" inventadas
4. **A Cartilha B3** exige prompts específicos sobre mercado de capitais para ser bem aproveitada
5. **Documentar a versão 1 que falhou** (Prompt 2) demonstra raciocínio — valorizado pelo mercado

---

## 4. Miniguia de Estudo (Entrega Final)

> Consolidado a partir das respostas do NotebookLM (Prompts 1 a 5), validadas contra os 5 PDFs do caderno temático.

### 4.1 Resumos estruturados

#### Ordem de prioridades para iniciantes

```
1. Educação financeira e autoconhecimento
2. Diagnóstico e planejamento (orçamento)
3. Eliminação de dívidas e equilíbrio (orçamento superavitário)
4. Reserva de emergência ("pague-se primeiro" — 3 a 6 meses de despesas)
5. Definição de projetos de vida (metas concretas)
6. Investimento e aposentadoria (aproveitar juros compostos)
7. Proteção do patrimônio (seguros contra riscos)
```

#### Erros que o iniciante deve evitar

- Procrastinar o planejamento financeiro
- Gastar mais do que ganha
- Confundir necessidade com desejo
- Esperar sobrar dinheiro para poupar (regra: separe primeiro)
- Usar crédito rotativo para consumo
- Cair em marketing de sedução (urgência, escassez, status)
- Ignorar o CET ao contratar crédito
- Negligenciar segurança digital (senhas fracas, compartilhamento)

#### Comparativo: onde guardar o dinheiro

| Característica | Poupança | CDB | Tesouro Direto |
| :--- | :--- | :--- | :--- |
| Liquidez | Diária (rendimento no aniversário) | Diária ou com carência | Alta (Selic = liquidez diária) |
| Risco | Baixo + FGC (R$ 250 mil) | Baixo + FGC | Baixo (governo) |
| Rentabilidade | TR + 0,5% ou TR + 70% Selic | % CDI ou prefixada | Selic, prefixada ou IPCA |
| IR | Isento | Regressivo (22,5% → 15%) | Regressivo (22,5% → 15%) |
| Melhor uso | Primeiro contato | Reserva / conservador | Reserva (Selic) / longo prazo (IPCA) |

#### Plano prático — exemplo R$ 4.000/mês endividado

| Fase | Quando | O que fazer |
|------|--------|-------------|
| Diagnóstico | Semana 1 | Mapear dívida (valor, taxa do rotativo) + listar receitas/despesas |
| Renegociação | Mês 1 | Parar cartão; renegociar ou portar para crédito mais barato |
| Equilíbrio | Meses 1–3 | Cortar supérfluos; parcelas ≤ 30% da renda (≤ R$ 1.200) |
| Reserva | Meses 3–12 | "Pague-se primeiro"; meta R$ 12k–24k em Tesouro Selic ou CDB DI |

#### Proteção no mercado de capitais (checklist)

- [ ] Senha forte, individual, com 2FA — nunca compartilhar
- [ ] Verificar registro do intermediário na CVM/BCB
- [ ] Preencher cadastro e suitability sozinho
- [ ] Exigir transparência de taxas (comparar pelo CET)
- [ ] Desconfiar de promessas de lucro garantido
- [ ] Monitorar churning (excesso de operações)
- [ ] Acompanhar operações na área logada da B3

---

### 4.2 Glossário (15 conceitos — Prompt 4)

| # | Conceito | Definição resumida | Exemplo prático |
|---|----------|-------------------|-----------------|
| 1 | Educação Financeira | Processo de compreensão de produtos, riscos e oportunidades financeiras | Estudar modalidades de crédito antes de contratar |
| 2 | Orçamento | Ferramenta que registra rendas e gastos para equilibrar a vida financeira | Anotar gastos diários para ver para onde vai o dinheiro |
| 3 | Troca Intertemporal | Escolha entre consumir agora (com juros) ou poupar para o futuro (com rendimentos) | Adiar compra de um computador para investir e comprar à vista depois |
| 4 | Custo de Oportunidade | Benefício de que se abre mão ao escolher uma alternativa | Usar dinheiro extra para viajar em vez de investir |
| 5 | Juros Compostos | Juros calculados sobre capital + juros acumulados ("juros sobre juros") | R$ 150/mês por 40 anos — a maior parte vem dos juros |
| 6 | Reserva de Emergência | Poupança separada para imprevistos ou perda de renda | 6 meses de despesas no Tesouro Selic |
| 7 | CET | Taxa real do empréstimo (juros + tarifas + encargos) | Banco com juros menores mas CET maior por taxas ocultas |
| 8 | Orçamento Superavitário | Receitas maiores que despesas no período | R$ 4.000 de renda, R$ 3.500 de gastos, R$ 500 de sobra |
| 9 | Suitability | Adequação do produto ao perfil e tolerância ao risco do investidor | Corretora impedir iniciante conservador de comprar ativos voláteis |
| 10 | Liquidez | Facilidade de converter investimento em dinheiro sem perda | Poupança = alta liquidez; imóvel = baixa liquidez |
| 11 | Rentabilidade | Retorno esperado sobre o capital investido | 0,5% ao mês sobre saldo em conta de investimentos |
| 12 | Risco | Probabilidade de perdas financeiras | Ação cair após crise econômica |
| 13 | Patrimônio Líquido | Bens e direitos menos dívidas | Carro R$ 40 mil − financiamento R$ 24 mil = R$ 16 mil |
| 14 | Crédito | Recurso de terceiros com pagamento futuro + juros | Usar cheque especial ou parcelar no cartão |
| 15 | Diversificação | Distribuir recursos em diferentes investimentos para reduzir risco | Dividir entre Tesouro, ações e fundos imobiliários |

---

### 4.3 Prompts reutilizáveis para revisão

Copie e adapte estes prompts no NotebookLM para revisar o tema no futuro:

**Revisão rápida (15 min)**
```
Faça um quiz de 10 perguntas sobre educação financeira pessoal com base nas fontes.
Depois de eu responder, corrija e cite a fonte de cada resposta.
```

**Checklist pré-investimento**
```
Com base nas fontes, crie um checklist de 10 itens que todo iniciante deve verificar
ANTES de fazer o primeiro investimento. Inclua segurança, perfil, taxas e intermediários.
```

**Diagnóstico financeiro**
```
Vou descrever minha situação financeira: [INSERIR DADOS].
Com base nas fontes, identifique pontos de atenção e sugira prioridades em ordem.
Cite a fonte de cada recomendação.
```

**Comparador de investimentos**
```
Compare [INVESTIMENTO A] e [INVESTIMENTO B] usando SOMENTE as fontes.
Avalie: liquidez, risco, custos, perfil indicado e limitações.
```

**Reserva de emergência**
```
Explique como calcular minha reserva de emergência e onde guardá-la,
usando apenas as fontes. Dê um exemplo com renda de R$ [VALOR].
```

**Proteção contra golpes**
```
Liste sinais de alerta e práticas abusivas no mercado financeiro mencionados nas fontes.
Organize por: promessas falsas, intermediários, taxas e segurança digital.
```

**Ficha de revisão mensal**
```
Crie uma ficha de revisão financeira mensal (1 página) com base nas fontes:
orçamento, dívidas, reserva, investimentos e metas. Formato checklist.
```

---

## 5. Como reproduzir este projeto

1. Baixe os 5 PDFs pelos links da seção [Curadoria de Fontes](#2-curadoria-de-fontes)
2. Acesse [notebooklm.google.com](https://notebooklm.google.com/) e crie um novo notebook
3. Faça upload dos 5 PDFs como fontes
4. Use os prompts documentados na [seção 3](#3-engenharia-de-prompts-e-cicatrizes) e adapte ao seu contexto
5. Valide as respostas cruzando com os PDFs originais — a IA é ferramenta, não autoridade

---

## 6. Referências

- Banco Central do Brasil — [Cidadania Financeira](https://www.bcb.gov.br/cidadaniafinanceira)
- CVM — [Portal do Investidor](https://www.gov.br/investidor)
- B3 — [Educação Financeira](https://edu.b3.com.br/)
- DIO — Desafio de Projeto: NotebookLM e Educação Financeira

---

## Licença

Este repositório documenta um projeto educacional. Os PDFs originais pertencem aos respectivos órgãos (BCB, CVM, B3) e são distribuídos gratuitamente pelas instituições. O conteúdo deste README foi produzido como parte do desafio da DIO.

---

**Autor:** Cesar Favero  
**Plataforma:** [DIO](https://www.dio.me/)  
**Data:** Junho/2026