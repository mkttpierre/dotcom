# Dotcom: um conselheiro de funil e tráfego para o seu agente de IA

> Skill em português para Claude Code e Codex. Coloca o método do Russell
> Brunson dentro do agente: como o cliente caminha até a compra (funil, escada
> de valor, e-mails) e de onde ele vem (tráfego pago, orgânico e lista própria).

Você pergunta "por que o meu funil não converte?", "de onde eu tiro cliente?"
ou "como monto um webinar que vende?". O agente acha o gargalo, abre só o
capítulo certo, faz a conta com os seus números e devolve o mapa do funil com
o que medir em cada etapa.

---

## De onde vem

A skill foi construída a partir da leitura de dois livros do Russell Brunson,
fundador do ClickFunnels:

| Livro | O que cobre | Arquivo |
|---|---|---|
| **DotCom Secrets** | Escada de valor, temperatura do tráfego, os 7 funis (frete grátis, SLO, continuidade, webinar, webinar invisível, lançamento, aplicação high-ticket), personagem atraente, sequências de e-mail novela e Seinfeld, engenharia reversa de funil | `livros/funis.md` |
| **Traffic Secrets** | Cliente dos sonhos, Dream 100, gancho-história-oferta, tráfego ganho, controlado e próprio, follow-up, Instagram, Facebook, Google, YouTube, podcast, afiliados, tráfego frio | `livros/trafego.md` |

Os resumos são **notas de leitura escritas com palavras próprias**, organizadas
para o agente consultar, sem trechos copiados dos livros. Os números dos livros
são dos EUA, em dólar, dos anos 2010: a skill usa como ordem de grandeza, nunca
como meta. Cada módulo termina com "Lacunas", o que o Brunson não cobre.

Não é material oficial e não tem ligação com o Russell Brunson nem com o
ClickFunnels. Se a skill te ajudar, compre os livros.

---

## Como funciona

1. **Lê o seu negócio.** Usa a memória do negócio da pasta (`_memoria/`) se
   existir, ou o que você contar: produto, ticket, margem, público, canais
   ativos, tamanho da lista e o que é proibido no seu setor ou plataforma.
2. **Acha o gargalo.** O `indice-de-decisao.md` classifica o problema em
   **funil** (a estrutura de venda), **tráfego** (quem chega) ou
   **relacionamento** (o que acontece depois do primeiro contato). Se faltar
   dado, faz até 5 perguntas do `questionario.md`, cada uma com recomendação.
3. **Lê só o capítulo certo.** Nunca carrega os dois livros inteiros.
4. **Monta a resposta:**
   - **Diagnóstico:** o gargalo e o número que o prova (ou o que falta medir).
   - **Jogada:** os passos, com o capítulo de origem.
   - **Conta:** valor médio do carrinho contra custo por aquisição, valor de cada contato da lista, divisão da verba.
   - **Mapa do funil:** tráfego → página → oferta → order bump → upsell → e-mails, com a métrica de cada etapa.
   - **Trava aplicada:** o que foi adaptado por causa da plataforma ou do setor.
   - **Teste:** uma métrica e um prazo.
5. **Revisa** o desenho contra o `revisao.md` antes de entregar.

### As regras que ela não quebra

- **Medir antes de mexer.** Funil que falha tem a causa no gancho, na história
  ou na oferta. Ela acha qual dos três antes de mandar refazer tudo.
- **Uma coisa por vez:** um desejo por mensagem, uma plataforma principal, um
  funil de entrada que se paga antes do próximo.
- **Todo tráfego vira lista própria** o quanto antes.
- **Tráfego frio não vai direto para a página de venda.** Precisa de ponte
  (conteúdo, quiz, artigo).
- **Urgência, escassez e história de origem só se forem verdadeiras.**
- **O que não está nos livros, ela diz que não sabe:** telas de gerenciador de
  anúncio, código de chatbot, SEO técnico.

---

## O que tem na pasta

```
dotcom/
├── SKILL.md               # o roteiro que o agente segue
├── indice-de-decisao.md   # sintoma → arquivo e seção para abrir
├── questionario.md        # perguntas por ramo
├── revisao.md             # checklist final do funil
└── livros/
    ├── funis.md           # DotCom Secrets
    └── trafego.md         # Traffic Secrets
```

---

## Como instalar

**Claude Code** (Mac ou Linux):

```bash
git clone https://github.com/mkttpierre/dotcom ~/.claude/skills/dotcom
```

**Claude Code** (Windows, PowerShell):

```powershell
git clone https://github.com/mkttpierre/dotcom "$env:USERPROFILE\.claude\skills\dotcom"
```

**Codex:** clone em `~/.codex/skills/dotcom`.

Para valer só num projeto, clone dentro de `.claude/skills/` da pasta do
projeto. Reabra o agente depois de instalar.

## Como usar

Digite `/dotcom` ou peça do seu jeito:

- "Desenha um funil para vender meu curso de R$ 497."
- "Meu anúncio custa mais do que o carrinho médio. O que eu mudo?"
- "Monta a sequência de 5 e-mails para quem baixou meu e-book."
- "Quero vender um serviço de R$ 10 mil. Funil de aplicação ou webinar?"
- "Quem são os meus Dream 100 no Instagram?"

Ela tem duas parceiras:

- [`hormozi`](https://github.com/mkttpierre/hormozi): oferta, preço, garantia
  e caixa em 30 dias. O funil do Brunson carrega a oferta do Hormozi: se a
  oferta está fraca, comece por lá.
- `copywriting` (vem no repo [`site-demonstracao`](https://github.com/mkttpierre/site-demonstracao)):
  o texto de cada peça. A `dotcom` decide a estrutura e o roteiro, e o texto
  final sai da `copywriting`.

---

## Licença

MIT. Use, adapte e distribua à vontade. Os livros e o método são do Russell Brunson.
