# Briefing editorial — RECONSTRUÇÃO 01: artigo `pmp-cost`

**Data:** 04/09/2026
**Revisado:** 04/09/2026 — correção das PDUs (seção 0) e as quatro correções editoriais
que você pediu depois do pacote de revisão (seção 0-b)
**Artigo:** custo da certificação PMP · `/certifications/guides/pmp-certification-cost/`
**Rascunho:** `editorial-os/drafts/pmp-cost-rebuilt.json`
**Artigo de produção:** **intacto**, guardado como referência de retorno
**Publicado:** nada · **Mesclado:** nada · **Apagado:** nada · **Outros artigos alterados:** nenhum

---

## 0. A correção que você pediu — e o rascunho estava errado mesmo

Eu tinha escrito que trabalhar na sua função "cobre no máximo 25 das 60 PDUs". **Isso está
errado, e a sua revisão pegou.**

Eu confundi o teto da **categoria** com o teto da **atividade**:

| | |
|---|---|
| **Interpretação antiga (errada)** | Trabalhar na função é Giving Back, logo cobre até **25** das 60 |
| **Por que estava errada** | 25 é o máximo da categoria **inteira** Giving Back. Trabalhar na função é **uma atividade dentro** dela |
| **Interpretação corrigida** | *Work as a Practitioner* tem teto de **8 PDUs por ciclo de três anos**. Ter emprego de gerente de projetos rende **no máximo 8 das 60** — e nada das 35 obrigatórias de Educação |

**Fonte:** PMI — *Continuing Certification Requirements (CCR) Handbook*, edição 2026.
Atualizei o rótulo da fonte no artigo para nomear a edição. Nenhum fornecedor de curso e
nenhum resultado de busca foi usado como autoridade.

**Por que a distinção precisa ficar explícita.** Os limites são aninhados, e é aí que todo
resumo apressado erra:

```
60 PDUs por ciclo
  ├─ no mínimo 35 de Educação          (piso, não teto)
  └─ no máximo 25 de Giving Back        (teto da categoria)
        └─ no máximo 8 de Work as a Practitioner   (uma atividade dentro dela)
```

O artigo agora traz isso como uma tabela de quatro linhas citando o manual, para a relação
ficar visível em vez de afirmada em prosa.

**A conclusão editorial se manteve — e ficou mais forte.** Ter o emprego não satisfaz a
renovação do PMP, e o número certo diz isso melhor que o errado: **8 de 60, cerca de uma
PDU em oito**, não 25.

### Um segundo problema que apareceu na varredura

O artigo tem **dois "35 de Educação" diferentes**: as **35 horas de formação** exigidas
antes da prova, e as **35 PDUs de Educação** exigidas em cada ciclo de renovação depois.
Os dois aparecem várias vezes e é fácil o leitor juntar as coisas.

Acrescentei uma frase separando: são exigências diferentes, em momentos diferentes — uma é
condição para se inscrever, a outra para manter a credencial. **Isso não estava no seu
pedido; a varredura é que trouxe.**

**Custo da correção:** +174 palavras (1.594 → 1.768) — a tabela e a desambiguação.

---

## 0-b. As quatro correções editoriais que você pediu

Edições cirúrgicas só no rascunho. **Nenhuma seção foi criada ou removida, nenhum cálculo
foi tocado, nenhum preço verificado foi tocado, e a análise das PDUs continua idêntica.**

| # | O que você apontou | Como ficou |
|---|---|---|
| 1 | **"Every applicant" era absoluto demais**, já que o próprio parágrafo dá a exceção do CAPM | Virou *"Most applicants need 35 contact hours… se você já tem um CAPM ativo, essa exigência está coberta"*. A exceção agora vem **logo depois** da regra |
| 2 | **A redação podia ser lida como afirmação sobre o negócio de treinamento da PMI** | O título virou **"Four kinds of cost, but only some are priced by PMI"**. E a abertura virou *"a PMI exige a formação, mas não publica um preço único para as 35 horas… Os fornecedores definem os próprios preços, então não existe um 'custo de treinamento PMP' emitido pela PMI"* |
| 3 | **A frase sobre PDUs grátis não tinha sustentação** | **Apagada.** Nada entrou no lugar. A frase seguinte foi ajustada só para ficar gramatical: *"The consequence for your calendar is real: at least 35 Education PDUs is a floor, and no job clears it on its own"* |
| 4 | **Preservar a análise das PDUs** | **Sem alteração.** Conferido: 60 → mínimo 35 Educação → máximo 25 Giving Back → máximo 8 Work as a Practitioner, com a distinção categoria/atividade intacta |

**A correção 2 é a que mais importa.** O artigo agora afirma só o que a evidência sustenta —
que não existe um preço único publicado pela PMI para as 35 horas — e **não afirma nada**
sobre a PMI oferecer ou não produtos de treinamento.

**A correção 3 tirou a última afirmação de custo sem fonte do artigo.** A seção agora não
diz mais nada sobre quanto as PDUs custam, só sobre o que elas exigem em tempo.

**Tamanho:** 1.768 → **1.743 palavras**. A seção "Money and time are separate budgets" foi
**mantida**, conforme você decidiu.

**Validação depois das edições:** build verde, check verde, JSON-LD válido, títulos em
ordem, 8 links internos funcionando, sem overflow a 375px. Pattern Guardian sem regressão —
e a sobreposição de frases até **caiu** (13 artigos, antes 15).

**Continua pendente, e não foi tocado:** o preço antigo do exame em `is-pmp-worth-it`,
`pmp-vs-capm`, `is-pmi-membership-worth-it`, `certifications.json` e, via tabela, em
`best-pm-certifications-beginners`. É tarefa separada.

---

## 1. O que mudou em relação ao artigo antigo

| | Antigo | Novo |
|---|---|---|
| Palavras | 477 | 1.743 |
| Títulos de seção | 3 | 8 |
| Links internos | 3 | 8, para 7 artigos |
| Fontes | 2 | 5 — os dois manuais da PMI entraram |
| Bloco de FAQ | Tinha | **Não tem** |
| Segundo bloco | Destaque colorido | **Título** |
| Trechos idênticos ao texto antigo | — | **Zero** |

**Sete correções de conteúdo:**

1. **Tirei a frase "todo valor vem da PMI"** — ela aparecia três vezes e era falsa
2. **Corrigi a taxa do exame** de ~$425/~$675 para **$405/$655**
3. **Corrigi a anuidade** de ~$140 para **$139**
4. **Removi a afirmação sobre reprovação**, que não tinha fonte
5. **Removi a faixa de treinamento** ($0–$600) e o total ($700–$2.500) — nenhum tinha fonte
6. **Acrescentei os dois manuais da PMI** às fontes; o artigo antigo publicava regras de
   renovação sem citar o manual que as sustenta
7. **Acrescentei a mudança de regra do fim de 2026**, marcada como futura, não vigente

---

## 2. Por que o novo artigo tem mais valor

O problema apontado na auditoria **não era o tamanho**. Era que a página não tinha motivo
para existir ao lado da página de preços da PMI — ela listava taxas que a PMI publica.

**Uma versão de 1.743 palavras da mesma lista de taxas falharia no mesmo teste.** O que
mudou foi a pergunta:

| Artigo antigo | Artigo novo |
|---|---|
| "Quanto custa o PMP?" | "Quanto vou gastar para tirar e manter, e o que estou subestimando?" |
| Lista as taxas e para | Classifica os custos por quem os define e o que os dispara |
| Diz que todo valor vem da PMI (falso) | Diz quais valores vêm da PMI e quais não podem vir |
| Publica faixa de treinamento sem fonte | Não publica nenhuma — e explica por quê |
| Termina na compra | Vai até a manutenção e o tempo |

---

## 3. Qual é a análise original do CertNorth

Oito coisas que a página da PMI não dá. A mais forte é a terceira:

1. **Classificação dos custos** — obrigatório, condicional, opcional, recorrente — dizendo
   quem define o preço de cada um
2. **O cálculo da anuidade na hora da prova**, separando essa pergunta estreita da pergunta
   maior "vale a pena ser membro?"
3. **A análise da composição das PDUs.** São 60 por ciclo: **no mínimo 35 de Educação, no
   máximo 25 de Giving Back — e, dentro dessa categoria, no máximo 8 de Work as a
   Practitioner**, que é o crédito por exercer a função. Ou seja: ter o emprego rende **no
   máximo 8 das 60**, e nada das 35 obrigatórias. A ideia repetida em toda parte de que
   "trabalhar já cobre a renovação" é estruturalmente falsa — por uma margem bem maior do
   que eu mesmo tinha calculado antes da sua correção
4. **Dinheiro e tempo separados**, sem converter hora em dinheiro
5. **A recusa em publicar um total de dez anos**, com os três motivos
6. **A mudança de 2026 tratada como variável de orçamento**, distinguindo regra atual de
   regra anunciada
7. **A correção de que a PMI não precifica o treinamento que exige**
8. **Um procedimento** para o leitor chegar ao próprio número

---

## 4. Quais números foram confirmados

Os que **você** verificou na PMI, fora deste ambiente:

| Item | Valor | Situação |
|---|---|---|
| Exame, membro | **$405** | **CONFIRMADO** |
| Exame, não membro | **$655** | **CONFIRMADO** |
| Anuidade PMI | **$139/ano** | **CONFIRMADO** |
| PDUs por ciclo de 3 anos | **60** | **CONFIRMADO** |
| Mínimo de Educação | **35** | **CONFIRMADO** |
| Máximo de Giving Back (categoria) | **25** | **CONFIRMADO** |
| Máximo de Work as a Practitioner (atividade) | **8** | **CONFIRMADO** — CCR Handbook 2026 |

**Descoberta importante:** o site publicava ~$425/~$675 em **cinco lugares**, de forma
coerente entre si — e **errada nos dois números**, por $20 cada.

E isso confirma que eu estava certo em recusar o "$445 a partir de 6 de agosto" que as
buscas sugeriam. Aquele número também estava errado.

---

## 5. Quais números continuam dependentes de região ou conta

- **A taxa do exame.** A PMI serve preço pela sua conta, então o que aparece no
  fechamento pode depender de onde você está. O artigo diz isso e manda o leitor conferir
  na própria conta.
- **A taxa de renovação.** É separada da anuidade e depende do seu status de membro **e**
  da região. **Não foi possível estabelecer um valor** — e por isso não há total de dez
  anos no artigo.
- **A taxa de reprovação.** Não confirmada. O artigo diz que existe e que não sabemos
  quanto é.
- **A taxa de inscrição** de novo membro. Não confirmada — fica de fora do cálculo, e o
  artigo declara isso.

---

## 6. Quais informações foram removidas por falta de evidência

| Removido | Por quê |
|---|---|
| "Todo valor vem da PMI" (3 lugares) | **Falso** — a mesma tabela trazia preço de treinamento de terceiros |
| Formação: "$0–$600 dependendo do fornecedor" | Sem fonte. A PMI não publica isso |
| Orçamento total: "$700–$2.500" | Sem fonte |
| "Reprovar acrescenta outra taxa de exame" | Sem fonte |
| Qualquer total de 5 ou 10 anos | A renovação não foi confirmada, e ela se repete três vezes numa década |

**Nenhuma afirmação sem sustentação do artigo antigo sobreviveu.**

---

## 7. Quais cálculos foram feitos pelo CertNorth

Cinco, todos rotulados como nossos — **nenhum atribuído à PMI**:

| Cálculo | Conta | Resultado |
|---|---|---|
| Rota do membro | $139 + $405 | $544 |
| Vantagem de entrar na PMI | $655 − $544 | **$111** |
| Diferença entre as duas taxas | $655 − $405 | $250 |
| Carga anual de PDU | 60 ÷ 3 | 20 horas/ano |
| Teto do Giving Back | 25 de 60 | 41,7% no máximo |

---

## 8. Quais premissas foram utilizadas

Todas aparecem no próprio texto, não em nota de rodapé:

- Preços atuais publicados pela PMI
- **Uma** tentativa de prova
- Sem variação regional
- **Taxa de inscrição excluída**, porque não conseguimos confirmar o valor
- PDUs obtidas sem custo
- As 35 horas de formação **não são precificadas** — o leitor põe a cotação dele

---

## 9. Quais são as limitações

1. ~~Uma premissa sustenta a melhor seção do artigo.~~ **Resolvido — e estava errada.**
   A premissa foi conferida no manual da PMI, mostrou-se incorreta e o trecho foi
   corrigido. Vale registrar o que isso significa: o rascunho anterior teria publicado um
   erro factual, e foi a revisão humana que impediu.
2. **Não há total de longo prazo.** É uma entrega menor e honesta.
3. **A originalidade foi avaliada por inspeção**, não contra as páginas que hoje rankeiam —
   este ambiente não consegue buscá-las.
4. **O artigo tem 1.743 palavras.** Se você achar longo, a seção mais cortável continua
   sendo "Money and time are separate budgets" — cerca de 180 palavras, e é a que menos
   sustenta. A tabela nova das PDUs eu não cortaria: é ela que torna o erro impossível de
   repetir.

---

## 10. Quais artigos receberam links

Oito links, todos **dentro de frases que já tratavam do assunto**. Sem bloco de "artigos
relacionados".

| Artigo | Onde | Por quê |
|---|---|---|
| `pmp-eligibility` | 2 lugares | Dono das regras e da dispensa via CAPM |
| `is-pmi-membership-worth-it` | Seção da anuidade | Dono da pergunta "vale a pena ser membro?", que este artigo **não** responde |
| `pmp-renewal-pdus` | Seção das PDUs | Dono da mecânica |
| `pmp-pass-rate` | Seção dos dez anos | É a prova de por que não calculamos custo esperado |
| `is-pmp-worth-it` | Fechamento | Dono do "vale a pena?" |
| `pmp-vs-capm` | Fechamento | A credencial mais barata enquanto você qualifica |
| `how-to-prepare-for-pmp-exam` | Fechamento | Onde o orçamento de tempo vira plano |

Os **11 links que apontam para esta página continuam funcionando** — URL, slug e
palavra-chave não mudaram.

---

## 11. Quais riscos ainda existem

1. ~~A premissa do Giving Back~~ — **resolvido**, ver seção 0
2. **A taxa do exame errada está no ar em mais quatro lugares:** `is-pmp-worth-it`,
   `pmp-vs-capm`, `is-pmi-membership-worth-it` e `certifications.json` — que alimenta uma
   tabela em `best-pm-certifications-beginners`, ou seja, **uma quinta página**.
   **Isso é maior que esta reconstrução e é o mais urgente**
3. **O `pmp-renewal-pdus`** diz na abertura que dá para ganhar PDUs "fazendo o seu próprio
   trabalho" — com o teto de 25 agora confirmado, isso exagera
4. **Preços envelhecem.** O artigo diz para conferir na própria conta, mas alguém precisa
   revisar periodicamente
5. **Nenhuma das ~160 citações do site tem data**

---

## 12. Se o artigo passou em todos os gates

**Sim — com uma marcação.**

| Gate | Resultado |
|---|---|
| Research | Passou |
| Source | Passou — 5 fontes, todas da PMI, **nenhum fornecedor citado** |
| Original Value | Passou — 8 contribuições |
| Editorial | Passou |
| **Fact Check** | **Passou** — nenhuma afirmação INCORRETA ou SEM SUSTENTAÇÃO restou. A marcação anterior foi conferida, estava errada e virou correção |
| Pattern | **Passou, sem regressão** — zero colisão contra 215 títulos; nenhuma sobreposição de frase nova depois da correção; primeiro artigo do site sem FAQ |
| SEO | Passou — título 52/60, descrição 137/155, sem keyword stuffing |
| AdSense Quality | Passou em substância — **e nenhuma mudança editorial garante aprovação** |
| Build + check | Passou, validado em cópia isolada; **produção nunca foi tocada** |

**Pattern Guardian achou três problemas no meu próprio rascunho e eu corrigi os três:** a
abertura usava uma fórmula retórica da casa; a frase de elegibilidade estava idêntica em
quatro artigos; e o parágrafo de 2026 repetia o `pmp-eligibility` quase palavra por palavra.

---

## 13. O que precisa da aprovação do Editor-in-Chief

| # | Decisão | Recomendação |
|---|---|---|
| 1 | ~~Confirmar o teto de Work as a Practitioner~~ | **Feito.** Conferido, estava errado, corrigido — ver seção 0 |
| 2 | Aprovar o rascunho para substituir o artigo | Sua decisão. Está pronto |
| 3 | Aprovar a remoção do FAQ | Recomendo. Custo: perde a marcação `FAQPage`; seria o primeiro artigo do site sem |
| 4 | **Corrigir a taxa do exame nos outros quatro lugares** | **Fortemente recomendado e urgente — há preço errado no ar em cinco páginas** |
| 5 | Corrigir o `certifications.json` e avançar o `verifiedOn` honestamente | Recomendado, junto com o 4 |
| 6 | Corrigir a abertura do `pmp-renewal-pdus` | Recomendado |
| 7 | Tirar a faixa sem fonte do `how-to-become-project-manager` | Recomendado |
| 8 | Acertar a linha de dez anos do `is-safe-certification-worth-it` | Recomendado |
| 9 | Passar a registrar a data de cada fonte | Decisão sistêmica |

---

## Como voltar atrás

O artigo de produção está **intacto e no ar**. O rascunho vive só em
`editorial-os/drafts/pmp-cost-rebuilt.json`, fora do build. Nada foi publicado, mesclado,
redirecionado ou apagado. Desfazer é apagar um arquivo.
