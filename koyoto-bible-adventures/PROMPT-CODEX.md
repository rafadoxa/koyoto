# Prompt para o Codex (cole isto primeiro)

> Anexe ao Codex a pasta do projeto: `ESPECIFICACAO-APP.md`, `ESTRUTURA.md`, `PROMPT-HIGGSFIELD.md`, `personagens/`, `esbocos/`
> e as imagens finais geradas no Higgsfield, colocadas em `assets/` conforme o manifesto da seção 15 da especificação.

```
You are the lead mobile engineer finishing "KOYOTO Bible Adventures", a children's Bible game app. The product owner is a
trained theologian and is NOT a developer. Everything you need is in this repository. Read, in this order:
1. koyoto-bible-adventures/ESPECIFICACAO-APP.md  (the full product + technical spec — your source of truth)
2. koyoto-bible-adventures/ESTRUTURA.md          (earlier planning notes and decisions)
3. koyoto-bible-adventures/personagens/koyoto-folha-de-personagem.png (mascot sheet — do NOT redesign the mascot)
4. koyoto-bible-adventures/esbocos/ and the design images in assets/ (visual direction)

GOAL
Build a production-ready Android app (Google Play first) with a codebase that is already structured so an iOS release is only
a build + store step later. Audience: children and pre-teens aged 8–14, two tracks ("Exploradores" 8–10 and "Desafiantes" 11–14),
parents/leaders as secondary users. Languages: Portuguese (Brazil) and English from day one.

STACK (decided; deviate only if you find a blocking reason and explain it in DECISIONS.md)
Flutter (stable) + Riverpod + go_router; local content as JSON bundled in assets; Supabase for parent accounts and realtime rooms;
RevenueCat for the "Plus" subscription; Flame only for the arcade-style games; the mascot is drawn natively (CustomPainter) — geometry
is in the spec. Platform-specific code must be isolated behind interfaces.

NON-NEGOTIABLE RULES
- No ads, no third-party analytics/ad SDKs, no free-text chat between children, no real names. Children use a nickname chosen from a list.
- Parent gate before any purchase, external link, or account/settings change.
- No demons or scary content in games. Dark forces appear only as abstract mist inside story text scenes, never as something the child fights.
- All UI text comes from localization files (pt-BR and en). Never put text inside image assets.
- Bible text: use only short paraphrases + the reference (e.g. "Josué 6") from content JSON until the owner confirms a translation license.
  Every content item has `reviewed` (bool); release builds must hide items with reviewed=false.
- Every game ends with: the verse paraphrase + reference ("Leia em Josué 6") + a sticker reward. Sessions are 2–4 minutes.
- Streaks must never punish harshly: free Sunday rest, one free freeze per week, no guilt-trip notifications.
- Leagues are only inside a room/team/church group, never against strangers.

WHAT TO DELIVER (milestones M0–M7 in the spec, in order)
Work milestone by milestone. After each one: run `flutter analyze` and `flutter test`, make the app build, and update CHANGELOG.md.
Keep commits small and descriptive. Do not skip ahead. If something in the spec is ambiguous or missing, make the smallest reasonable
decision, record it in DECISIONS.md, and continue — do not stall. List anything that needs the owner (theology review, licenses,
store accounts, secrets) in OWNER-TODO.md.

DEFINITION OF DONE (per milestone)
App builds for Android; no analyzer errors; tests for scoring/streak/room logic pass; works offline for bundled free content;
screens match the visual direction (cream/brown palette, rounded cards, mascot reactions); accessibility basics (touch targets ≥ 48dp,
contrast, text scaling) respected.

START NOW with M0 (project scaffold, design system, localization, theme tokens, mascot widget with its 8 expressions) and show me what you
built and what you decided before moving to M1.
```

## Notas para o autor
- O Codex trabalha melhor em inglês, por isso o prompt está em inglês; a especificação está em português.
- Coloque as imagens do Higgsfield em `assets/` com os nomes do manifesto (seção 15 da especificação) antes de começar.
- Chaves e senhas (Supabase, RevenueCat, conta do Google Play) **nunca** entram no repositório; o Codex vai listá-las em `OWNER-TODO.md`.
