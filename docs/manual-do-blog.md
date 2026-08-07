# Manual do CertNorth — como operar o blog sozinha

Guia em português para publicar e customizar **sem instalar nada** e **sem depender do Claude**.
Tudo é feito pelo navegador, no site do GitHub.

---

## 1. Como o site funciona (em 1 minuto)

O site não tem painel de administração nem banco de dados. Cada artigo é **um arquivo de
texto** (formato JSON) dentro do repositório. Quando você salva um arquivo novo na branch
`main`, acontece isto sozinho, no servidor do GitHub:

1. O GitHub baixa o projeto e instala o Node
2. Roda o **GATE de qualidade** — confere campos obrigatórios, tamanhos, links, contraste
3. **Se passar**, gera o site e publica no Cloudflare
4. **Se falhar**, nada vai ao ar e o site continua exatamente como estava

Ou seja: **você não consegue quebrar o site publicando algo errado.** O pior que acontece é
a publicação não sair, com o motivo explicado.

Leva cerca de 2 minutos entre salvar e estar no ar.

---

## 2. Publicar um artigo novo (passo a passo)

> **Regra de ouro: nunca escreva do zero. Sempre copie um artigo existente e edite.**
> Assim você herda a estrutura correta e evita 90% dos erros.

1. Abra `github.com/Nana1969-crypto/certnorth`
2. Entre em **`platform`** → **`content`** → **`articles`**
3. Abra um artigo parecido com o que você quer escrever
4. Clique no ícone de **lápis** (canto superior direito) para ver o texto editável
5. Selecione tudo (Ctrl+A) e copie (Ctrl+C)
6. Clique em **`articles`** no caminho lá em cima para voltar à pasta
7. Botão **`Add file`** → **`Create new file`**
8. No campo do nome, escreva: `nome-do-seu-artigo.json`
   *(só letras minúsculas e hífens; sempre terminar em `.json`)*
9. Cole o texto copiado e edite (veja a seção 3)
10. Role até o fim → em **`Commit changes`**, escolha **`Commit directly to the main branch`**
11. Clique em **`Commit changes`**

Pronto. Em ~2 minutos está no ar.

### Como conferir se deu certo

Vá na aba **`Actions`** do repositório e olhe a execução mais recente:

- ✅ **verde** = publicado, já está no ar
- 🟡 **amarelo** = ainda rodando, espere
- ❌ **vermelho** = não foi ao ar. Clique nela, depois no passo vermelho, e role até o fim:
  a última linha diz exatamente o que está errado.

---

## 3. Os campos do artigo

O que você precisa trocar depois de copiar. **Todos são obrigatórios.**

| Campo | O que é | Regra que o GATE cobra |
|---|---|---|
| `id` | Identificador interno | Único no site. Sem espaços, use hífens |
| `slug` | O que aparece no endereço | Único no site. Sem espaços, use hífens |
| `clusterId` | Em qual categoria entra | Tem que existir no `taxonomy.json` (veja seção 4) |
| `title` | Título que aparece na página | — |
| `dek` | Resumo que responde a pergunta logo de cara | **Mínimo 40 caracteres** |
| `authorId` | Autor | Use sempre `author_team` |
| `publishedAt` | Data de publicação | Formato `AAAA-MM-DD` |
| `updatedAt` | Data da última revisão | Igual à `publishedAt` em artigo novo |
| `intent.primaryKeyword` | A busca que o artigo quer atender | **Não pode repetir** nenhuma já usada no site |
| `seo.metaTitle` | Título que aparece no Google | **Máximo 60 caracteres**, único |
| `seo.metaDescription` | Descrição que aparece no Google | **Máximo 155 caracteres**, única |
| `sources` | Lista de fontes | **Pelo menos 1**, com URL real |
| `body` | O conteúdo | **Pelo menos 2 títulos nível 2** e **1 link interno** |

### As três regras que mais reprovam

1. **`metaDescription` passou de 155 caracteres** — o erro mais comum de todos. Conte antes.
2. **`primaryKeyword` repetida** — dois artigos disputando a mesma busca. O GATE bloqueia
   porque isso prejudica os dois no Google (chama-se canibalização).
3. **Menos de 2 títulos nível 2** no corpo, ou nenhum link interno.

---

## 4. As categorias disponíveis (`clusterId`)

| Use este `clusterId` | Onde o artigo aparece | Endereço gerado |
|---|---|---|
| `cl_compare` | Certificações → Comparações | `/certifications/compare/...` |
| `cl_worth` | Certificações → Vale a pena | `/certifications/worth-it/...` |
| `cl_guides` | Certificações → Guias | `/certifications/guides/...` |
| `cl_paths` | Trajetórias de Carreira | `/career-paths/how-to-become/...` |
| `cl_salary` | Salários | `/salaries/guides/...` |
| `cl_skills` | Skills e Métodos | `/skills/learn/...` |

---

## 5. Os blocos de conteúdo (`body`)

O corpo do artigo é uma lista de blocos. Estes são os tipos disponíveis:

**Parágrafo**
```json
{ "type": "paragraph", "richText": "Seu texto aqui." }
```

**Título** (`level` pode ser 2, 3 ou 4 — use 2 para as seções principais)
```json
{ "type": "heading", "level": 2, "text": "Título da seção" }
```

**Lista**
```json
{ "type": "list", "ordered": false, "items": ["Primeiro item", "Segundo item"] }
```

**Destaque** (`variant`: `info` = azul, `tip` = dica, `warn` = alerta)
```json
{ "type": "callout", "variant": "tip", "richText": "Texto do destaque." }
```

**Tabela** (a legenda `caption` é obrigatória)
```json
{ "type": "table", "caption": "Do que trata a tabela.",
  "headers": ["Coluna A", "Coluna B"],
  "rows": [["linha 1 A", "linha 1 B"], ["linha 2 A", "linha 2 B"]] }
```

**Perguntas frequentes** (todo artigo deve ter um)
```json
{ "type": "faq", "items": [
  { "question": "A pergunta?", "answerRichText": "A resposta." }
] }
```

### Link interno (obrigatório: pelo menos 1 por artigo)

Dentro de um parágrafo, o texto vira uma lista com as partes separadas:

```json
{ "type": "paragraph", "richText": [
  "Texto antes do link ",
  { "link": { "ref": "article:is-psm-worth-it", "text": "texto clicável" } },
  " texto depois do link."
] }
```

O `ref` usa o **`id`** do artigo de destino (não o slug), sempre com `article:` na frente.
Se o artigo de destino não existir, o GATE bloqueia — isso impede link quebrado.

### Link externo

Usa o **mesmo campo `ref`**, só que com o endereço completo no lugar de `article:`:

```json
{ "link": { "ref": "https://www.pmi.org/", "text": "texto clicável" } }
```

Ou seja: `ref` começando com `article:` → link interno; `ref` começando com `https://` →
link externo (o motor já adiciona a proteção de segurança sozinho).

---

## 6. Customizar o site

| O que mudar | Arquivo |
|---|---|
| Nome, slogan, promessa, política editorial, e-mail | `platform/content/site.json` |
| Páginas de Privacidade e Contato | `platform/content/pages.json` |
| Preços e requisitos das certificações | `platform/content/certifications.json` |
| Pilares e categorias | `platform/content/taxonomy.json` |
| Autor | `platform/content/authors.json` |
| Cores do site | `platform/src/tokens.js` |

### Atualizar o preço de uma certificação

Os artigos e tabelas leem do arquivo `certifications.json`. Mude **um número num lugar** e
todo o site se atualiza no próximo build.

Ao mudar um preço, **troque também o `verifiedOn`** para o mês em que você conferiu
(formato `AAAA-MM`). Esse campo significa "uma pessoa olhou na fonte oficial" — por isso
só uma pessoa pode preenchê-lo.

O build avisa quando algum dado passa de **6 meses** sem verificação. É só um lembrete,
não trava nada.

---

## 7. Corrigir ou apagar

**Corrigir um artigo:** abra o arquivo, clique no lápis, edite, commit na `main`.
Se mudar o conteúdo de verdade, atualize o `updatedAt` para a data de hoje.

**Apagar um artigo:** abra o arquivo, clique no ícone de **lixeira**, commit na `main`.
O site remove a página e tira do sitemap sozinho.
⚠️ Antes de apagar, confira se nenhum outro artigo linka para ele — senão o GATE bloqueia
o build inteiro (o que é bom: evita link quebrado, mas trava até você tirar o link também).

**Desfazer uma publicação inteira:** aba `Pull requests` → `Closed` → abra a publicação →
botão `Revert`. Isso desfaz tudo daquela publicação e republica a versão anterior.

---

## 8. As regras editoriais (o que não fazer)

Estas não são cobradas pelo programa — são a promessa do CertNorth ao leitor.
Elas são o motivo de o site merecer confiança:

- **Nunca invente um número.** Todo preço, requisito e salário sai de uma fonte real,
  nomeada e linkada. Se não achou a fonte, não publique o número.
- **Nunca mude uma data só para parecer atualizado.** `updatedAt` só muda quando o
  conteúdo mudou de verdade.
- **Uma busca, uma página.** Nunca dois artigos disputando a mesma pergunta.
- **Diga para quem a certificação NÃO serve**, não só para quem serve. É o que diferencia
  o site de quem só vende curso.
- **Autoria honesta.** Os artigos são assinados pela equipe editorial, sem inventar
  credenciais pessoais que ninguém tem.

---

## 9. Se der errado

| Sintoma | O que fazer |
|---|---|
| Actions ❌ vermelho | Clique na execução → no passo vermelho → role até o fim. A última linha diz o erro |
| "metaDescription com X chars" | Encurte para 155 ou menos |
| "canibalização: primaryKeyword..." | Já existe artigo com essa busca. Escolha outra |
| "clusterId inexistente" | Erro de digitação. Confira na seção 4 |
| "sem link interno contextual" | Falta o link `article:` no corpo |
| Erro estranho com `{` ou `,` | Erro de JSON: vírgula sobrando ou aspas faltando |
| Publicou mas não aparece no site | Espere 2 min e recarregue com Ctrl+F5 |

O site **nunca fica no ar quebrado**: se o build falha, a versão anterior continua
publicada normalmente.
