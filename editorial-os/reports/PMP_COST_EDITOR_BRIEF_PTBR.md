# Briefing editorial — reconstrução do artigo `pmp-cost`

**Data:** 04/09/2026
**Revisado:** 04/09/2026 — protocolo de verificação corrigido
**Artigo:** custo da certificação PMP · `/certifications/guides/pmp-certification-cost/`
**Situação:** **pesquisa parcialmente concluída.** Nada foi escrito, nada foi alterado,
nada foi publicado.

---

## Antes de tudo: uma correção no meu próprio método

Na primeira versão desta pesquisa eu dei confiança **MÉDIA** ao preço do exame porque
várias páginas de fornecedores diziam a mesma coisa. **Isso estava errado e foi
retirado.**

Repetição não é verificação. Um número copiado entre sites comerciais é **uma** afirmação
aparecendo muitas vezes — não muitas confirmações independentes. E quando todos os sites
vendem cursos de PMP, a concordância entre eles diz pouco sobre os preços da PMI e nada
sobre qual número está vigente hoje.

**O que mudou por causa disso:**

| Antes | Agora |
|---|---|
| Modelei o exame a $445/$675 | Modelo com **~$425/~$675**, que é o que o nosso site publica |
| Modelei a anuidade a $149 | Modelo com **$140–$150** — e essa faixa **é** a contradição do nosso site |
| Propunha corrigir nossa afirmação sobre reprovação | **Retirado.** A correção vinha de páginas de fornecedores |
| Tinha um cenário com reprovação a $275 | **Retirado** |

A pesquisa ficou **mais fraca em afirmações e mais forte em integridade**. É a direção
certa.

---

## 1. O que sabemos com confiança

Aqui "confiança" significa uma coisa só: **isto é o que o repositório do CertNorth
contém.** Não significa que esteja correto.

### O site é mais coerente do que eu esperava

| Afirmação | Locais que concordam |
|---|---|
| Exame PMP ~$425 membro / ~$675 não membro | **5** — `pmp-cost`, `is-pmp-worth-it`, `pmp-vs-capm`, `is-pmi-membership-worth-it`, `certifications.json` |
| Renovação $60 / $150, 60 PDUs a cada 3 anos, mínimo 8 por área | **3+** |
| Elegibilidade 36/60 meses + 35 horas de formação | **7** |
| CAPM $225 / $300, 23 horas | **4** |
| PMI-ACP $435 / $495, 21 horas | **2** |

### E uma coisa que sabemos em definitivo

**Não existe taxa de aprovação confiável do PMP.** A PMI não publica há cerca de vinte
anos, e o "61%" que circula é uma nota de corte aposentada por volta de 2006. Nosso artigo
`pmp-pass-rate` já demonstra isso.

Isso **não precisa de verificação nenhuma** — a ausência do dado *é* a descoberta. E é o
que autoriza o artigo novo a **se recusar** a calcular "custo esperado" ponderado por
probabilidade. Toda página que faz essa conta usa um número que não existe.

---

## 2. O que conflita internamente

Nove contradições. Encontrei todas dentro do nosso próprio repositório, sem acessar nada
externo.

| # | Contradição | Gravidade | Dá para corrigir só neste artigo? |
|---|---|---|---|
| 1 | **`pmp-cost` afirma três vezes que "todo valor vem da PMI" — e publica preços de treinamento que a PMI não publica** | **Alta** | **Sim — e não precisa de verificação nenhuma** |
| 2 | Anuidade **~$140** (`pmp-cost`) vs **~$150** (`is-pmi-membership-worth-it`) — **citando a mesma URL** | Média-alta | Não — outro artigo |
| 3 | Custo total **$700–$2.500** (`pmp-cost`) vs **$1.000–$3.000** (`how-to-become-project-manager`) | Média | Não — outro artigo |
| 4 | O único número de 10 anos do PMP no site são só as taxas de renovação, numa tabela em que **todas as outras linhas são totais completos** (`is-safe-certification-worth-it`) | Média | Não — outro artigo |
| 5 | `pmp-renewal-pdus` abre dizendo que dá para ganhar PDUs "fazendo o seu próprio trabalho", e o corpo do texto diz que essa via **tem teto** — sem nunca dizer qual | Média | Não — outro artigo |
| 6 | Reprovação descrita como "outra taxa de exame" — **sem fonte**, e é a única menção do site | Média | **Sim** — remover ou qualificar |
| 7 | `pmp-cost` publica regras de renovação **sem citar o CCR Handbook**, que é o documento que as sustenta | Média-baixa | **Sim** — acrescentar a fonte |
| 8 | `pmp-cost` recomenda curso autoinstrucional sem mencionar a mudança de regra do fim de 2026 que o `pmp-eligibility` documenta | Média-baixa | **Sim** |
| 9 | **Nenhuma fonte do site tem data.** São ~160 citações, todas só com rótulo e link | Média, sistêmica | Não — é decisão de esquema |

### A número 1 merece parágrafo próprio

O artigo diz, em três lugares diferentes, que **todo valor veio da PMI**. E na mesma tabela
que carrega esse selo há a linha:

> Formação obrigatória (35 horas) — **$0–$600 dependendo do fornecedor**

A PMI não vende treinamento de PMP e não publica esse preço. A segunda tabela do artigo, de
$700 a $2.500+, é inteiramente preço de terceiros.

**A afirmação e o conteúdo que a desmente estão no mesmo arquivo.** É uma declaração sobre
a nossa própria integridade de fontes, num site cuja posição inteira é independência e
verificabilidade, na página que a auditoria já tinha apontado como a mais fraca.

**Minha recomendação: tirar isso independentemente de tudo o mais.** É a única correção
deste plano que não depende de verificar nada.

---

## 3. O que não é possível verificar neste ambiente

**Nada de preço.** O ambiente onde trabalho bloqueia todo acesso externo — testei
`pmi.org` e recebi bloqueio explícito, e o mesmo vale para qualquer outro domínio.

A única coisa que me resta é uma busca que devolve **resumos** de páginas de terceiros. E
todas as fontes que ela devolve são empresas que vendem cursos de PMP — na nossa própria
hierarquia, o pior tipo de fonte possível para falar do produto que vendem.

**Elas discordam entre si**, e eu não escolhi nenhuma:

| Pergunta que a busca levantou | O que apareceu | O que fiz |
|---|---|---|
| A taxa mudou em agosto de 2026? | Várias páginas dizem que sim, para outros valores | **Anotei como pergunta.** Não adotei |
| Qual a taxa de membro? | $405 · $425 · $445 | **Três valores, nenhum escolhido** |
| Qual a anuidade? | $129 · $139 · $149 · $154 · $159 | **Cinco valores, nenhum escolhido** |
| **A PMI cobra preços diferentes por país?** | **Uma fonte diz que sim. Outra diz que não.** | **Sem resolução — e é a pergunta que mais importa** |
| Existe taxa reduzida de reprovação? | Sugerem que sim | **Não adotado** |
| Qual o alcance da regra de treinamento de 2026? | Duas leituras diferentes | **Sem resolução** |

**Deliberadamente não escolhi o valor mais repetido.** Você pediu isso e está certa: o
número que mais aparece é apenas o mais copiado.

**Também não posso verificar:** a política de reprovação, os tetos de PDU, o alcance da
regra de treinamento, e se os nossos ~$425/~$675 continuam corretos.

**E uma coisa que ninguém consegue verificar:** um preço médio de treinamento. Não existe
dado neutro — toda fonte que publica uma média vende o produto que precifica.

---

## 4. O que precisa ser verificado manualmente antes de publicar

Entre no site da PMI **logada, do país para o qual o leitor está sendo orientado**, e
anote com a data:

| # | O que checar | Por que importa |
|---|---|---|
| 1 | Taxa do exame, membro e não membro, **como aparece na tela de pagamento** | É o número da página |
| 2 | **Se esse valor e essa moeda são diferentes do valor em dólar da página geral** | **Decide se o artigo pode afirmar qualquer número universal.** É o item mais importante da lista |
| 3 | Anuidade **e o valor da taxa de inscrição** | Nosso site nunca quantificou a taxa de inscrição |
| 4 | Taxa de renovação, membro e não membro | Alimenta o modelo de dez anos |
| 5 | **Taxa de reprovação, quantas tentativas e em que prazo** (PMP Handbook) | Hoje não temos nada com fonte |
| 6 | **Mínimos e máximos por categoria de PDU** (CCR Handbook) | Decide o que podemos dizer sobre PDU |
| 7 | **A redação exata da regra de treinamento do fim de 2026** — se vale para as 35 horas todas ou só para aula ao vivo | Muda o piso de custo |

Os itens **2, 5, 6 e 7 mudam o que o artigo pode dizer.** Os itens 1, 3 e 4 mudam só os
números dentro dele.

---

## 5. Dá para desenhar a arquitetura mesmo com isso tudo em aberto?

**Sim. Está pronta — só os números estão bloqueados.**

| Elemento | Situação |
|---|---|
| Pergunta editorial e ângulo | **Fechado** |
| Ordem das seções e títulos | **Fechado** — conferi contra os 215 títulos H2 do site: zero repetições |
| Taxonomia dos custos | **Fechado** — independe de qualquer preço |
| Decisões estruturais anti-template | **Fechado** |
| Links internos e mapa de consolidação | **Fechado** |
| Lista de fontes | **Fechado** — precisa acrescentar o CCR Handbook e o PMP Handbook |
| Separação dinheiro × tempo | **Fechado** |
| A recusa em calcular custo esperado | **Fechado** — se apoia numa descoberta permanente |
| **Todo valor em dinheiro** | **Bloqueado** até alguém ler na PMI |

**O artigo pode ser desenhado. Não pode ser publicado.**

### A estrutura, em resumo

Nove seções. As quebras de padrão em relação aos outros 50 artigos:

- O segundo bloco é um **título**, não um destaque colorido — hoje são **50 de 50** artigos
  abrindo com parágrafo seguido de destaque
- Abre com uma **tabela de incerteza**, não com uma tabela de preços
- **Um único destaque** no artigo inteiro
- **Sem bloco de FAQ.** Li o motor: ele não exige. Seria o primeiro artigo do site sem
- **Sem "2026" no título**, num texto que argumenta que números fixos envelhecem

### O resultado que vale publicar

**CÁLCULO CERTNORTH**, com as entradas do nosso próprio site — todas ainda por verificar:

| Cenário | 5 anos | 10 anos |
|---|---|---|
| **A** — entra na PMI só no ano da prova, depois deixa vencer | $715–$725 | **$1.015–$1.025** |
| **B** — mantém a anuidade o tempo todo | $1.185–$1.235 | **$2.005–$2.105** |

**Manter a anuidade por dez anos custa cerca de $990–$1.080 a mais e economiza $270 em
renovações.**

**Não modelei:** reprovação (taxa não verificada, e nossa própria afirmação não tem fonte)
e treinamento (não existe dado neutro). O artigo vai dizer isso, em vez de chutar.

---

## 6. O que precisa da sua aprovação

| # | Decisão | Recomendação |
|---|---|---|
| 1 | **Tirar a frase "todo valor vem da PMI"** | **Sim, independentemente de tudo.** É falsa e não precisa de verificação |
| 2 | Verificar os preços na PMI antes de escrever? | **Sim.** Uma sessão resolve oito perguntas em aberto |
| 3 | Tirar o bloco de FAQ? | **Sim.** Repetiria o corpo do texto. Custo: perdemos uma marcação para o Google |
| 4 | Corrigir a anuidade no `is-pmi-membership-worth-it`? | **Segundo artigo — precisa da sua aprovação** |
| 5 | Corrigir a faixa de custo no `how-to-become-project-manager`? | **Segundo artigo — precisa da sua aprovação** |
| 6 | Acertar a linha de 10 anos no `is-safe-certification-worth-it`? | **Segundo artigo — precisa da sua aprovação** |
| 7 | Corrigir a abertura do `pmp-renewal-pdus`? | **Segundo artigo — precisa da sua aprovação** |
| 8 | Atualizar o `certifications.json`? | **Muda uma segunda página publicada — precisa da sua aprovação** |
| 9 | **Passar a registrar a data de cada fonte?** | **Decisão sistêmica.** Hoje são ~160 citações sem data nenhuma |

---

## Se você só puder fazer duas coisas

**Primeira, hoje, sem depender de ninguém:** autorizar a remoção da frase "todo valor vem
da PMI". Ela é falsa, está publicada, e é sobre a nossa honestidade.

**Segunda:** entrar na PMI logada, do Brasil, e me dizer **qual preço aparece na tela**.
Isso responde à pergunta que hoje impede o artigo de afirmar qualquer número — a PMI cobra
diferente por país ou não?
