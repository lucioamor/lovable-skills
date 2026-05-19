# NXLV.AI — Wireframe Esquemático Completo

> Mapa estrutural de todas as páginas, seções, componentes, títulos, subtítulos, microcopy e CTAs.
> Reflete o estado atual do código. Notação visual usa `[ELEMENTO]`. Layout: topo → base, esquerda → direita.
> Idiomas: EN (default) / PT-BR (auto-detect via `navigator.language`). Páginas legais sempre em PT-BR.

---

## 0. MAPA DE ROTAS

| Rota | Página | Descrição | Acesso |
|------|--------|-----------|--------|
| `/` | **Index** | Home institucional NXLV (one-pager) | Público |
| `/saas` | **SaaS** | Landing especializada B2B SaaS Growth | Público |
| `/thank-you` | **ThankYou** | Confirmação pós-envio de contato | Público (noindex) |
| `/privacy` | **Privacy** | Política de Privacidade (LGPD) | Público (noindex) |
| `/tos` | **Terms** | Termos de Serviço | Público (noindex) |
| `/report/:id` | **Report** | Relatório privado de cliente | Autenticado + RLS |
| `/admin` | **Admin** | Painel de gestão de reports | Admin role apenas |
| `*` | **NotFound** | 404 | Público (noindex) |

Domínios: `https://be.nxlv.ai` (canonical) · `https://nxlv.lovable.app` (preview)

---

## 1. HEADER GLOBAL (Index + SaaS)

> Fixo no topo, full-width. Transparente no topo → `bg-background/80 backdrop-blur` ao rolar.

```
┌──────────────────────────────────────────────────────────────────────────┐
│ [LOGO 40x40] nxlv.ai      [Why NXLV] [Services] [Track Record]           │
│   [edit] (admins)         [Hackathons ↗] [Who runs it]   🌐 EN/PT        │
└──────────────────────────────────────────────────────────────────────────┘
```

- **Logo**: PNG turquesa + wordmark `nxlv.ai` em gold (gradient-text).
- **[edit]**: link `text-[10px]` para Lovable project — visível **só para admins logados**.
- **Hackathons**: link externo (`target="_blank"`) para `lovablehackathons.com.br` com ícone ↗.
- **Mobile (<sm)**: nav some, vira `[☰]` Sheet lateral com mesmas entradas + botão `[Contact]`.

---

## 2. PÁGINA: `/` — INDEX (Home NXLV)

### SEÇÃO 2.1 — HERO `<HeroSectionV2>`

> Grid editorial 7+5 colunas. Glow turquesa radial + grid SVG diagonal de fundo.

```
┌─ hairline accent ─────────────────────────────────────────────────┐
│                                                                   │
│  H1 (col-span-7, 88-108px, uppercase)        SUBTITLE (col-5)     │
│  "Your team wants to ship                    "Enablement,          │
│   with Lovable.                              hackathons and        │
│   NXLV makes it happen."                     full solution         │
│                                              development with      │
│  • (gold dot)                                Lovable — in PT,      │
│                                              from Brazil to        │
│                                              the world."           │
│                                                                    │
│                                              "Founded by Lucio     │
│                                              Amorim ·              │
│                                              Lovable Ambassador"   │
│                                                                    │
│                                              [★ Talk to NXLV]      │
│                                              How we work ↓         │
└─ hairline accent ─────────────────────────────────────────────────┘
```

### SEÇÃO 2.2 — WHY NXLV `<WhyNXLVSection>` (anchor `#why-nxlv`)

> Eyebrow + H2, depois grid 3 colunas (cards com hairline divider).

- **Eyebrow**: "Why NXLV"
- **H2**: "Why choose NXLV"

| Card 1 | Card 2 | Card 3 |
|--------|--------|--------|
| 🌐 **Knowledge base in Portuguese** | 🔗 **Close to the Lovable ecosystem** | 🔨 **Complete solutions, not just technical deliverables** |
| Documentation, sprints e suporte no seu idioma e fuso. | Founded by Lucio Amorim, Lovable Ambassador. Imersão contínua na plataforma. | Aplicações em produção com escopo, prazo e dono único. Vamos além do código. |

### SEÇÃO 2.3 — WHAT WE DO `<WhatWeDoSection>` (anchor `#what-we-do`)

- **H2**: "What we do"
- **Subtitle**: "Three service tracks, each with clear scope and deadlines."

> Grid 3 cards `glass-card` com ícone, descrição, proof line e CTA.

| Card | Ícone | Título | Descrição | Proof | CTA |
|------|-------|--------|-----------|-------|-----|
| 1 | 🔨 Hammer | Corporate Lovable hackathons | Hackathons internos, protótipos reais em 24-72h. | Featured product: lovablehackathons.com.br | `Request scope →` (externo) |
| 2 | 🏢 Building2 | Enterprise pilots & GTM | Pilotos AI-native com governança. Solução em produção + plano de scaling. | +US$100M em B2B pipelines | `Book diagnostic →` (modal) |
| 3 | 🔧 Wrench | Strategic execution & training | Auditamos seu Lovable, destravamos pipelines, treinamos seu time. | 600x ROI · 7-43x growth · M&A exits | `Talk to NXLV →` (modal) |

### SEÇÃO 2.4 — FEATURED PRODUCTS `<FeaturedProductsSection>` (anchor `#products`)

- **Eyebrow**: "NXLV products"
- **H2**: "Featured"
- **Subtitle**: "NXLV products you can hire directly."

> Card horizontal único (full-width):

```
┌────────────────────────────────────────────────────────────────┐
│ 🏆 [FLAGSHIP PRODUCT]   80+ events · 24 countries              │
│                                                                │
│ Lovable Hackathons Brasil                                      │
│ Methodology validated and exported from Brazil to 24 countries.│
│                                              [Visit site ↗]    │
└────────────────────────────────────────────────────────────────┘
```

### SEÇÃO 2.5 — TRACK RECORD `<TrackRecordSection>` (anchor `#track-record`)

- **H2**: "Track Record"
- Strip horizontal full-bleed, 3 colunas, números animados (count-up):

| Badge | Métrica | Título | Contexto |
|-------|---------|--------|----------|
| International B2B | **R$ 30MM+** | B2B LATAM Pipeline | Channel creation \| 600x ROI in 6 months |
| Infoproducts → SaaS | **28-43x ROI** | M&A Exit (Empiricus/BTG) | From 3 founders in a room to M&A |
| B2B SaaS | **7x growth** | SaaS Growth | +15% MRR/month sustained for 12+ months |

> Footer link: "Detailed cases and public record on Lucio's profile →" (externo)

### SEÇÃO 2.6 — ABOUT `<AboutSection>` (anchor `#about`)

- **H2**: "Who runs it"

> Card 2-col: [foto Lucio 160x160] + [bio + assinatura]

- **P1**: "NXLV does enablement, runs hackathons and develops complete solutions with Lovable. Founded by Lucio Amorim, Lovable Ambassador."
- **P2**: "20+ years leading BI and GTM at Fortune 100 (Shell, Visa, Bayer, Petrobras), translated into sprints with deadlines, real deliverables and zero theater."
- **Assinatura**: "— Lucio Amorim · Lovable Ambassador · GTM Operator"
- **Botões**: `[in]` LinkedIn (icon-only) · `[Meet Lucio →]` (externo, gold)

### SEÇÃO 2.7 — FINAL CTA `<FinalCTASectionV2>` (anchor `#contact`)

- **H2**: "Where do we start?"
- **Subtitle**: "Pick the path closest to your problem."

> 3 cards lado a lado:

| Path | Ícone | Título | Descrição | CTA |
|------|-------|--------|-----------|-----|
| Sprint | → | I want to hire a sprint | Implementation/pilot Lovable engagement com escopo e prazo. | `[Talk to NXLV]` (modal) |
| Hackathon | 🔨 | I want to run a hackathon | Corporate Lovable hackathon na sua empresa. | `[Visit lovablehackathons.com.br ↗]` |
| Lucio | 👤 | I want to know who Lucio is | Editorial profile, public cases. | `[Meet Lucio ↗]` |

> Footer: "Selective portfolio. If it fits both sides, you'll know in the first conversation."

### FOOTER (Index)

```
┌─────────────────────────────────────────────────────────────┐
│ © 2026 NXLV.AI                       ECOSYSTEM              │
│ Enablement · Hackathons · Solutions  Lucio Amorim ↗         │
│                                      Lovable Hackathons ↗   │
├─────────────────────────────────────────────────────────────┤
│ [Privacy] [Terms]                Built with Lovable.dev     │
└─────────────────────────────────────────────────────────────┘
```

---

## 3. PÁGINA: `/saas` — SaaS Growth Agency

### SEÇÃO 3.1 — HERO `<SaaSHero>`

> Grid 7+5 com badges flutuantes de métricas à direita.

- **Badge**: "● SaaS Growth Agency" (pulse)
- **H1**: "We scale SaaS companies." (40-80px)
- **Subtitle**: "Demand generation, GTM strategy, and growth systems for B2B SaaS."
- **Desc**: "From early-stage to scale-up — we build the marketing engine that drives predictable MRR growth."
- **CTAs**: `[Book a Growth Diagnostic →]` (gold) · `[See Results ↓]` (outline)

> **Métricas flutuantes (direita)**:
> - 📈 Avg. MRR Growth — **+15%/mo**
> - 📊 Pipeline Generated — **$100M+**
> - 🎯 Best Client ROI — **600x**

> **Strip inferior**: "20+ years Fortune 100 · SaaS Growth · Demand Generation · GTM Strategy"

### SEÇÃO 3.2 — LOGO CLOUD `<SaaSLogoCloud>`

- Eyebrow: "Trusted by leaders across industries"
- Wordmarks (mute): Shell · Visa · Bayer · Petrobras · Empiricus · BTG Pactual

### SEÇÃO 3.3 — SERVICES `<SaaSServices>` (anchor `#services`)

- Eyebrow: "What We Do"
- **H2**: "Full-Stack SaaS Marketing"
- Subtitle: "Six core capabilities to take your SaaS from traction to scale."

> Grid 3 colunas × 2 linhas:

| Ícone | Serviço | Descrição |
|-------|---------|-----------|
| 📣 | Demand Generation | Inbound + outbound qualified pipeline. |
| 🚀 | Product-Led Growth | Activation funnels, onboarding, self-serve. |
| 🖱 | Paid Acquisition | Google, LinkedIn, Meta otimizados por CAC. |
| 🔍 | SEO & Content | Bottom-of-funnel content que converte. |
| 📊 | Revenue Analytics | Attribution, cohorts, ARR dashboards. |
| 📈 | GTM Strategy | Positioning, ICP, competitive playbooks. |

### SEÇÃO 3.4 — TRACK RECORD `<SaaSTrackRecord>` (anchor `#track-record`)

- **H2**: "Proven Results"
- 3 strips com count-up: **7x growth** · **R$ 30MM+** · **28-43x ROI**

### SEÇÃO 3.5 — METHODOLOGY `<SaaSMethodology>` (anchor `#how-we-work`)

- Eyebrow: "Our Process"
- **H2**: "How We Work"
- 4 steps com numeração 01-04:
  1. 🔍 **Diagnose** — Deep analysis of funnel, ICP, blockers.
  2. 💡 **Strategize** — Custom GTM playbook.
  3. 🚀 **Execute** — Build & run, not just advise.
  4. 📊 **Optimize** — Weekly sprints, data-driven.

### SEÇÃO 3.6 — ENGAGEMENTS `<SaaSEngagements>` (anchor `#engagements`)

- **H2**: "Engagement Models"

| Plano | Duração | Tagline | Ideal para | CTA |
|-------|---------|---------|------------|-----|
| **Growth Sprint** | 4 weeks | Quick wins, fast validation | Early-stage SaaS | `[Start Sprint]` |
| **Scale Partner** ⭐ Most Popular | 90 days | Full-stack growth engine | $50K → $500K+ MRR | `[Talk to a Strategist]` (gold) |
| **Fractional CMO** | Ongoing | Strategic marketing leadership | Series A+ | `[Discuss Partnership]` |

### SEÇÃO 3.7 — ABOUT (reusa `<AboutSection>`)

Mesma seção da Index — Lucio + bio + Meet Lucio.

### SEÇÃO 3.8 — FINAL CTA `<SaaSFinalCTA>`

- **H2**: "Ready to scale your SaaS?"
- Bullets: ⏱ 2-hour growth diagnostic · 🎯 Custom GTM roadmap · 🗺 Clear ROI projections
- Footer: "We work with a selective portfolio. If it's a fit, you'll know in the first conversation."
- **CTA**: `[Book Growth Diagnostic]`

### FOOTER (SaaS)

```
© 2026 NXLV.AI                              [Privacy] [Terms]
SaaS Growth Agency | Demand Generation | GTM Strategy
```

### WebMCP (apenas /saas)

> `navigator.modelContext.provideContext()` expõe a tool `request_consultation` para AI agents.
> Schema: `{ name, email, company?, message }` → POST para edge function `send-contact-notification`.

---

## 4. MODAL GLOBAL: ContactDialog

> Disparado por todos os CTAs principais (`Talk to NXLV`, `Book diagnostic`, etc).

```
┌─────────────────────────────────────────────────┐
│ Get in touch                              [×]   │
│ Fill out the form or use Google to speed up.    │
├─────────────────────────────────────────────────┤
│ [G  Continue with Google]                       │
│ We'll use your name and email from Google.      │
│ ─────────────── ou ───────────────              │
│                                                 │
│ Name *      [_________________________]         │
│ Email *     [_________________________]         │
│ Company     [_________________________]         │
│ Message *   [_________________________]         │
│             [_________________________]         │
│                                                 │
│ We respond within 24 business hours.            │
│                                                 │
│                              [Send →]           │
└─────────────────────────────────────────────────┘
```

- Se usuário **já logado** via Google: mostra banner "Google conectado — campos preenchidos".
- Persistência via `localStorage` (`nxlv_contact_open/company/message`) para reabrir após OAuth redirect.
- Submit grava em `nxlv_contacts` (Supabase) + dispara edge function `send-contact-notification` → redireciona para `/thank-you`.

---

## 5. PÁGINA: `/thank-you`

```
┌─────────────────────────────────────────┐
│             ✓ (CheckCircle 64px)        │
│                                         │
│        Thank you for reaching out!      │
│  We received your message and will      │
│  respond within 1 business day.         │
│                                         │
│         Next steps:                     │
│  Follow us on social media to stay      │
│  updated with NEXT LEVEL news           │
│                                         │
│  [📷  Follow on Instagram         ↗]   │
│  [in  Follow on LinkedIn          ↗]   │
│                                         │
│  ─────────────────────────              │
│  ← Back to home                         │
└─────────────────────────────────────────┘
NEXT LEVEL • Artificial intelligence for enterprises
```

---

## 6. PÁGINA: `/privacy` — Política de Privacidade

> **Sempre PT-BR** (validade jurídica). SEO: `noindex`.

**Header simples**: Logo + `[← Back]` + LanguageSwitcher.

**Aviso**: "Este documento está disponível apenas em português para validade jurídica."

**H1**: Política de Privacidade — Next Level (nxlv.ai) · *Última atualização: Janeiro de 2026*

**Seções (H2)**:
1. Quem somos
2. Dados que coletamos (2.1 fornecidos · 2.2 automáticos · 2.3 Login Google OAuth)
3. Finalidade do uso dos dados
4. Compartilhamento de dados
5. Armazenamento e segurança
6. Cookies e tecnologias semelhantes
7. Direitos do titular dos dados (LGPD)
8. Retenção dos dados
9. Alterações nesta Política
10. Contato — contato@nxlv.ai

**Footer**: © 2026 NXLV.AI · [Privacy] [Terms]

---

## 7. PÁGINA: `/tos` — Termos de Serviço

> Mesma estrutura visual da Privacy. **Sempre PT-BR**. `noindex`.

**H1**: Termos de Serviço — Next Level (nxlv.ai)

**Seções (H2)**:
1. Aceitação dos Termos
2. Descrição dos serviços
3. Cadastro e autenticação (Google OAuth)
4. Uso permitido
5. Propriedade intelectual
6. Limitação de responsabilidade
7. Suspensão e encerramento
8. Privacidade e dados pessoais (link → /privacy)
9. Alterações nos Termos
10. Lei aplicável e foro (Brasil)
11. Contato

---

## 8. PÁGINA: `/report/:id` — Relatório do Cliente

> Acesso restrito por RLS Supabase. Exige login.

```
┌─────────────────────────────────────────────────────┐
│ ← nxlv.ai                       [⬇ Download PDF]    │
├─────────────────────────────────────────────────────┤
│ │ TÍTULO DO REPORT (h1, font-display)               │
│ │ Atualizado em DD de mês de YYYY                   │
├─ gradient divider ──────────────────────────────────┤
│                                                     │
│ <ReportContent format="markdown" | "html" />        │
│                                                     │
│ <ReportAttachments reportId="..." />                │
│                                                     │
│ ───────────────                                     │
│ NEXT LEVEL • Inteligência Artificial   © 2026       │
└─────────────────────────────────────────────────────┘
```

- **Sem sessão**: AuthModal abre com `redirectPath=/report/:id`.
- **Sem permissão**: "Report não encontrado ou acesso negado."
- **Download PDF**: invoca edge function `generate-report-pdf` → abre janela de impressão.

---

## 9. PÁGINA: `/admin` — Painel Admin

> Restrito a `user_roles.role = 'admin'`. Layout 2-col.

### Header
`← [Reports Admin]                user@email  [⎋ Logout]`

### Coluna esquerda — Lista de Reports
- Botão `[+ Novo]`
- Cards: título, client_email, data atualização, ações `[Copy] [Open ↗] [Delete]`

### Coluna direita — Editor (quando criando/editando)
- `<ClientPicker>` — seleciona email do cliente
- Input: **Título**
- Toggle: **Formato** [Markdown | HTML]
- Textarea: **Conteúdo** (mono, min-h 300px)
- Botões: `[Salvar]` (gold) · `[Cancelar]`
- **Após salvar**: `<AttachmentManager reportId>` para upload de anexos
- **Bloco de notificação**: input email + toggle [PT | EN] + botão `[Enviar email]` (envia template HTML dark via edge function `send-gmail`)

---

## 10. PÁGINA: `/*` — 404 NotFound

```
┌─────────────────────────┐
│         404             │
│  Oops! Page not found   │
│      Back to home       │
└─────────────────────────┘
```

`noindex`. Loga `console.error` com a rota tentada.

---

## 11. SEO & DISCOVERABILITY (cross-page)

| Recurso | Path | Função |
|---------|------|--------|
| `<SEO>` component | per-route | Title, description, canonical, hreflang, JSON-LD |
| Sitemap | `/sitemap.xml` | Index + SaaS + páginas legais |
| Robots | `/robots.txt` | Allow all + sitemap link |
| LLMs | `/llms.txt` | Resumo do ecossistema para AI crawlers |
| MCP Card | `/.well-known/mcp/server-card.json` | Descoberta de MCP server |
| Agent Skills | `/.well-known/agent-skills/index.json` | Capacidades para AI agents |
| WebMCP | `/saas` runtime | `request_consultation` tool |

**JSON-LD Index**: Organization (NXLV.AI) + WebSite + sameAs (lucioamorim, hackathons, linkedin).
**JSON-LD SaaS**: Service (B2B SaaS Growth Marketing) + BreadcrumbList.

---

## 12. DESIGN TOKENS

| Token | Valor | Uso |
|-------|-------|-----|
| Background | `#0A0B0C` | Page bg |
| Surface | `#111213` | Cards |
| Foreground | `#F0EDE8` | Body text |
| Muted | `#7A7A80` | Descriptions |
| **Primary (gold)** | `#E8B84B` | CTAs, ícones de bullet |
| **Accent (turquoise)** | `#00BFB3` | H2, badges, números, eyebrows |
| Border | `#1E2020` | Card borders |
| Display font | **Oxanium** | H1/H2/H3 |
| Body font | **Inter** | Texto |

---

## 13. INTERAÇÕES E REGRAS

- **i18n**: auto-detect EN/PT-BR. Switcher no header. Páginas legais ignoram o switch (sempre PT).
- **Auth**: Supabase + Google OAuth. `lovable.auth.signInWithOAuth("google")`.
- **Roles**: tabela `user_roles` com função `has_role()` (security definer). `[edit]` e `/admin` checam `role = 'admin'`.
- **Animações**: `useScrollReveal` (24px fade-up @ 15% threshold), count-up nas métricas, glow turquesa pulsante no Hero.
- **Hackathons**: sempre link externo, `target="_blank" rel="noopener noreferrer"`.
- **Lucio**: bio resumida na NXLV, CTA "Meet Lucio →" leva ao site editorial completo.
- **Voz NXLV**: enablement, hackathons, soluções completas. Nunca "operação da Lovable", nunca "linha direta com HQ", nunca "entregamos código".
