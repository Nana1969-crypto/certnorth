# CertNorth Editorial OS — guia da Editora-Chefe

Este arquivo é referenciado pelo `CLAUDE.md` e existe para uma pessoa só: **você**.
Ele explica o que pedir, o que você recebe de volta, e o que **nunca** acontece sem a
sua autorização.

Escrito em português porque é a você que ele serve. Todo o resto do sistema está em
inglês porque o site é em inglês.

---

## O que pedir, em linguagem normal

Você não precisa saber os nomes dos arquivos. Peça o resultado; o sistema escolhe o
caminho.

| Se você disser… | O sistema roda | O que você recebe |
|---|---|---|
| "publique o artigo de hoje" | `new-article` | Artigo publicado + relatório |
| "este artigo está bom?" | `audit-content` | Diagnóstico e recomendação |
| "revise o site inteiro" | `audit-existing-site` | Inventário completo, sem alterar nada |
| "conserte o artigo X" | `rebuild-article` | Reconstrução, não maquiagem |
| "o preço do PMP mudou" | `update-article` | Correção + data de revisão real |
| "esses dois artigos são iguais" | `merge-articles` | Proposta de consolidação |

---

## Os quatro momentos em que você decide

O sistema **não** age sozinho nestes pontos. Se ele agir, está quebrado.

1. **Publicar** — nada chega ao site sem passar pelo `final-publish`, e nada passa
   pelo `final-publish` sem você.
2. **Juntar artigos** — consolidar duas páginas em uma apaga uma URL. Sempre sua decisão.
3. **Apagar ou redirecionar** — nunca automático.
4. **Mudar navegação, categorias ou URLs canônicas** — nunca automático.

Além disso: **qualquer coisa voltada para fora** (publicar, mesclar, remover) exige
você. Pesquisar, analisar, verificar e escrever são livres.

---

## O que você recebe antes de aprovar

Um **briefing editorial em português** (`skills/editor-brief-ptbr`). Ele foi feito para
que você decida **sem** precisar entender SEO, terminologia de certificação,
metodologia de pesquisa ou os sistemas do Google.

O briefing sempre diz:

- Qual pergunta do leitor o artigo responde
- O que o CertNorth acrescenta que a fonte original não dá
- De onde vem cada número, e o que **não** foi possível verificar
- O que ainda está incerto
- A recomendação — e quando ela é "não publique"

Se um briefing não te deixar decidir com segurança, **ele falhou**. Diga, e ele é reescrito.

---

## As regras que o sistema não pode violar

Você não precisa vigiar isso, mas deve saber que existe:

- **Nada inventado.** Nunca autores, credenciais, entrevistas, pesquisas, depoimentos,
  citações, estatísticas, estudos, experiência ou relações comerciais.
- **Se não deu para verificar, ele diz `UNVERIFIED`** e explica o que falta — em vez de
  preencher com um número plausível.
- **Data só muda com revisão real.** Nunca "atualizado" cosmético.
- **Uma pergunta, uma página.** Dois artigos disputando a mesma busca prejudicam os dois.
- **Sem enchimento.** Se a resposta honesta cabe em 600 palavras, são 600 palavras — ou o
  artigo é mesclado. Não existe contagem de palavras que produza aprovação no AdSense.
- **Divulgação honesta.** Nunca afirmar uma relação comercial que não existe, nem omitir
  uma que existe.

---

## Os limiares — e o que eles não são

`config/quality-thresholds.yaml` traz números como "revisar se abaixo de 800 palavras"
e "mínimo 60% de fontes oficiais".

**São diagnósticos, não metas.** Servem para marcar um artigo para revisão humana. Um
artigo abaixo do limiar não é automaticamente ruim, e inflá-lo para passar do limiar é
explicitamente proibido — é exatamente o comportamento que o sistema existe para evitar.

---

## Sobre AdSense — a parte honesta

O sistema tem uma skill de qualidade para publicadores (`skills/adsense-quality`). Ela
abre dizendo, corretamente:

> Não é um método para obter aprovação no AdSense. **Nenhuma mudança editorial garante
> aprovação.** Não existe tamanho de artigo nem quantidade de artigos que a produza.

O que ela faz é reduzir risco real de qualidade e aumentar valor real para o leitor.
Se alguém — inclusive eu — te prometer aprovação, está chutando.

---

## Onde as coisas ficam

| Pasta | O que é |
|---|---|
| `workflows/` | Os procedimentos (publicar, auditar, corrigir, mesclar) |
| `agents/` | Os papéis especializados (verificador de fatos, editor final, etc.) |
| `skills/` | Os métodos reutilizáveis (pesquisa em fonte primária, SEO, anti-template) |
| `templates/` | Os formatos de saída, incluindo o briefing em português |
| `config/` | Limiares, hierarquia de fontes, tipos de conteúdo |
| `reports/` | Auditorias já feitas — **leia estas** |
| `research/` | Dossiês de pesquisa por artigo |

**Os relatórios em `reports/` são o material mais útil para você agora.** Eles contêm
achados sobre o site como ele está, incluindo um de severidade alta sobre divulgação
que já foi corrigido.

---

## Se você quiser operar sem o Claude

Existe um manual separado, também em português, em **`docs/manual-do-blog.md`**. Ele
ensina a publicar e editar direto pelo navegador, no site do GitHub, sem instalar nada
e sem depender de mim.

---

## Como pedir correção do próprio sistema

Se um workflow te entregar algo confuso, um briefing não te deixar decidir, ou um
limiar parecer errado — diga. Estes arquivos são editáveis e devem mudar quando não
servirem. O sistema é uma ferramenta sua, não uma autoridade sobre você.
