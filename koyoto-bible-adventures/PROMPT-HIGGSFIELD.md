# KOYOTO Bible Adventures — Pacote de prompts para o Higgsfield

Como usar: abra o Higgsfield online, **envie as imagens de referência** (seção 1), cole o **Briefing mestre** (seção 2)
e depois peça os lotes da seção 4 em ordem. Os prompts estão em **inglês** porque os modelos de imagem respondem melhor assim;
os títulos e instruções estão em português. **Todo texto do app é escrito no código**, por isso nenhuma imagem deve conter letras.

---

## 1. Imagens de referência para enviar (nesta ordem)

1. `ilustracoes/comparativo-piloto.png` e as 8 imagens do piloto (davi, noe, moises, jesus, abraao, adao-eva, anjo, fundo-tela): **referência de estilo e consistência**.
2. `personagens/koyoto-folha-de-personagem.png`: **o mascote KOYOTO** (não pode ser alterado).
3. As 5 referências de estilo do autor (pasta `referencias/`): cartões coloridos dos sapos, loja mobile, papel recortado, app de leitura infantil.
4. Para qualquer pedido de personagem: anexe o piloto correspondente como `image_references` para manter o rosto igual.

---

## 2. Briefing mestre (cole primeiro, vale para tudo)

```
PROJECT: "KOYOTO Bible Adventures" — a mobile game app (Android first, iOS later) for children and pre-teens aged 8–14
that teaches the Bible through short games, stories and collectible stickers. Mascot: KOYOTO, a rounded-square character with a
dark face, a pink-to-orange gradient border and two glowing white oval eyes (use the attached character sheet; never redesign it).

GLOBAL STYLE (apply to every image):
Charming flat 2D cartoon, thick dark-brown outlines (#4A2C1D), soft rounded shapes, warm cream (#FFF7EA), caramel (#B9794B)
and orange (#F18F0B) palette with teal (#456B5F) and mustard (#B79F0F) accents, subtle layered paper-cut depth with soft shadows,
big friendly eyes, gentle paper texture, polished children's video-game quality. Same style as the attached pilot images.

HARD RULES:
- NO text, letters, numbers, logos or watermarks inside any image (all text is added later in code).
- Biblical characters: joyful, warm, respectful, never realistic, never scary, modest ancient Middle-Eastern clothing.
- Jesus is always the same design as the attached pilot: cheerful, wise, welcoming teacher, never caricatured.
- Demons/dark forces: ONLY as soft abstract dark mist shapes with no face, no horns, no blood. Never in game assets.
- Keep each character visually identical across all images (same face, hair, outfit colors).
- Clean edges and flat backgrounds when asked for "isolated asset" so they can be cut out later.
OUTPUT: PNG, one asset per image unless a sheet is requested.
```

---

## 3. Lista completa de entregas (quantidades)

| Grupo | O que | Qtde |
|---|---|---|
| A | Mascote KOYOTO (pose, 8 expressões, 4 acessórios) | 13 |
| B | Jesus (variações) | 4 |
| C | 12 apóstolos (individuais) | 12 |
| D | Outras figuras (Adão, Eva, Noé, Abraão, Moisés, Davi, Paulo, anjos, sombras) | 10 |
| E | Cenas das 3 histórias do MVP (3 cenas cada) | 9 |
| F | Cartões do carrossel (um por história, cor chapada) | 12 |
| G | Fundos (abertura, escritório, mapa, menu, jogos) | 8 |
| H | Assets de jogos (MVP: 5 jogos) | ~30 |
| I | Figurinhas / carimbos do passaporte | 24 |
| J | Loja Google Play (ícone, gráfico, capturas) | 10 |
| K | Telas de interface (mockups) | 12 |
| L | Animações curtas (vídeo/GIF) | 12 |
| | **Total aproximado** | **~156** |

---

## 4. Prompts por lote

Em todos: **prefixe com o Briefing mestre** (já colado) e use a referência indicada.

### Lote A — Mascote KOYOTO (referência: folha de personagem)

A1 Pose base: `KOYOTO mascot, front view, centered on solid cream background, rounded-square dark face, pink-to-orange gradient border, two glowing white oval eyes, soft shadow below, exactly as the reference sheet.`
A2–A9 Expressões (mesmo mascote, só muda os olhos): normal; joyful (eyes as happy upward arcs); surprised (bigger eyes); thinking (one eye half-closed, one small brow line); sad (eyes drooping, brows tilted up inward); wink (one eye an arc); resting (closed downward arcs with a tiny 'z'); celebrating (eyes as golden stars).
A10–A13 Acessórios (mesmo mascote): explorer hat in brown; red scarf; round reading glasses; short caramel cape. Tudo sem texto.

### Lote B — Jesus (referência: jesus.png do piloto)

B1 `Jesus as a cheerful wise teacher, full body, laughing kindly, open welcoming hands, cream robe with caramel sash, brown hair and short beard, standing on isolated clean cream background.`
B2 `Jesus sitting among laughing children on a grassy hill, warm sunset, same character.`
B3 `Jesus teaching a small crowd by the lake, gentle smile, boats in the background.`
B4 `Jesus breaking bread with a boy offering a basket of bread and fish, joyful mood.`

### Lote C — Os 12 apóstolos (um por imagem, fundo creme isolado, corpo inteiro, 3:4)

Use este molde: `[NOME], one of the twelve apostles, friendly cartoon character, [TRAÇO], isolated on clean cream background, same style as the pilot.`

| # | Nome | TRAÇO (sem símbolos de martírio) |
|---|---|---|
| 1 | Peter | fisherman look, rope net over shoulder, a ring with two keys |
| 2 | Andrew | fisherman look, holding a small fish |
| 3 | James (son of Zebedee) | energetic pose, lightning-bolt pattern on his cloak ("son of thunder") |
| 4 | John | youngest, gentle, holding a scroll and a feather quill |
| 5 | Philip | holding a basket of round bread |
| 6 | Bartholomew | holding a fig leaf, a small fig tree behind |
| 7 | Matthew | holding coins and a ledger scroll (former tax collector) |
| 8 | Thomas | curious face, one hand reaching out to touch (honest "seeing is believing") |
| 9 | James (son of Alphaeus) | neutral: simple walking staff, calm face |
| 10 | Thaddaeus | neutral: carrying a small lantern |
| 11 | Simon the Zealot | neutral: a small flame emblem on his sash |
| 12 | Judas Iscariot | serious and thoughtful, small coin bag at the belt; muted palette; story card only, not a collectible |

Opcional (1 imagem): `All twelve apostles together in a friendly group portrait, consistent with the individual designs.`

### Lote D — Outras figuras (isolado, creme)

D1 Adam (calm, leaf-and-cloth garment). D2 Eve (only Eve, no serpent, no apple). D3 Noah (referência piloto). D4 Abraham (referência piloto).
D5 Moses (referência piloto). D6 David (referência piloto). D7 Paul, as a thoughtful traveler with scrolls (letters) in a bag.
D8 Angel made of soft warm light, friendly (referência piloto). D9 Group of three smaller angels, joyful.
D10 Abstract dark mist shape fading into golden light, no face, gentle (story use only).

### Lote E — Cenas das histórias do MVP (3:4 e 16:9 quando indicado)

Davi: E1 shepherd David with sheep at sunrise; E2 David with the sling facing a giant shadow-silhouette (non-scary, comic scale); E3 David celebrating with soldiers cheering.
Noé: E4 Noah building the ark with animals arriving in pairs; E5 rainstorm and the ark floating safely, rainbow forming; E6 the dove with an olive branch.
Moisés: E7 Moses and the burning bush (soft glowing flames, no scary face); E8 sea parting with people crossing; E9 Moses receiving the stone tablets on a mountain (tablets with no writing).

### Lote F — Cartões do carrossel (estilo "cartão de sapo", 3:5, cor chapada por história)

`Tall rounded card illustration, flat saturated background [COR], [PERSONAGEM] large and centered with thick outline, simple shapes, no text, no heart icon, no frame.`
Cores: Davi laranja #F18F0B; Noé verde-petróleo #456B5F; Moisés vermelho-alaranjado #EF491D; Abraão mostarda #B79F0F; Jesus creme com detalhe caramelo; Adão e Eva verde #7BA05B; Josué terracota; Daniel azul-petróleo; José roxo-vinho; Jonas azul-mar; Ester rosa-antigo; Paulo marrom.

### Lote G — Fundos

G1 Splash (9:16): `cream sky, layered paper-cut hills in caramel and dark brown, small sparkling stars, big empty center for the mascot` (referência: fundo-tela.png).
G2 Escritório: `a warm detective-explorer desk seen from above, cream paper, brown wood, magnifier, rolled map, empty center area, no text.`
G3 Mapa-múndi: `layered paper-cut map of the Holy Land with hills, a sea and path dots, no labels.`
G4 Menu Criança/Adulto: soft cream gradient with decorative corner clouds.
G5 Noite no deserto (para histórias): deep blue sky, golden stars, caramel dunes.
G6 Jardim: lush garden with fruit trees (sem serpente).
G7 Lago: calm lake with boats at sunset.
G8 Montanha: mountain with a glowing sky.

### Lote H — Assets dos jogos do MVP (fundo transparente quando possível)

Memória relâmpago (jogo 1): H1 card back with a decorative star-and-leaf pattern; H2–H9 eight card faces (sling, ark, dove, staff, lamp, fish, bread, star) in one consistent style.
Arca 2048 (jogo 3): H10–H14 animal tiles that evolve in size (lamb, goat, ox, camel, elephant) as isolated round tiles.
Funda de Davi (jogo 7): H15 round wooden target; H16 sling with stone; H17 small sparkle effect sheet.
Linha do tempo (jogo 12): H18 blank parchment event card frame (no text); H19 time-line rope with pegs; H20 gold medal.
Duelo 1x1 (jogo 17): H21 versus lightning badge (no letters); H22 trophy; H23 timer ring; H24 correct-answer burst; H25 wrong-answer soft cloud.
Genéricos: H26 coin; H27 star; H28 heart-less "life" lantern; H29 confetti burst; H30 scroll for verse (empty).

### Lote I — Figurinhas / passaporte (24 selos redondos, 1:1, sem texto)

`Round passport-style stamp sticker, thick outline, distressed ink look, [SÍMBOLO] in the center, cream and brown with one accent color.`
Símbolos: sling; ark; dove; staff; burning bush; tablets; lamb; star; fish; bread; key; lantern; scroll; harp; crown of olive leaves; wall of Jericho; rainbow; fig leaf; coins; anchor; sandal; tent; camel; angel wing.

### Lote J — Loja Google Play

J1 Ícone 512x512: the KOYOTO face (dark rounded square, gradient border, glowing eyes) centered on a cream circle with tiny stars; no text.
J2 Gráfico de recursos 1024x500: mascot on the left, layered hills and biblical characters (David, Noah, Moses, Jesus) on the right, empty band for the title to be added later.
J3–J10 Fundos de capturas de tela (9:16), um por tela: splash, menu, carrossel, história, jogo de memória, jogo da funda, duelo, passaporte.

### Lote K — Telas de interface (mockups 9:16, só referência visual)

`Mobile app screen mockup, cream and brown palette, cartoon style, rounded cards, [TELA]. Replace all text with plain grey bars.`
Telas: K1 abertura com KOYOTO grande; K2 KOYOTO pequeno à direita e menu à esquerda (Adulto / Criança); K3 trilhas Exploradores e Desafiantes; K4 personalizar o KOYOTO; K5 escritório com carrossel de cartões; K6 arquivo da história (Diário, Atividades, Competição); K7 modo Estudo com alternador áudio/texto e letra capitular; K8 jogo de memória; K9 fim de jogo com versículo e figurinha; K10 passaporte de carimbos; K11 sala por QR Code; K12 painel de pais e líderes.

### Lote L — Animações (vídeo/GIF curto, câmera parada, 2D plano, loop, fundo sólido creme)

Gere a partir das imagens estáticas aprovadas (imagem para vídeo), 2 a 4 segundos cada:
L1 KOYOTO pisca e respira (loop). L2 KOYOTO pula de alegria. L3 KOYOTO encolhe e desliza para o canto direito (transição da abertura). L4 olhos acendem ao dizer "Oi" (brilho pulsa). L5 comemoração com estrelas e confete. L6 KOYOTO dorme com "z". L7 carrossel desliza um cartão (efeito de arrastar). L8 carimbo pressionado no passaporte. L9–L11 movimento sutil de câmera (parallax) nas cenas de Davi, Noé e Moisés. L12 chuva e arco-íris leve na cena da arca.

---

## 5. Ordem sugerida (se o crédito for limitado)

1. **Essenciais (~40):** A (13), B1, C (12), D1–D8, G1, G2, F (3 cartões do MVP), J1.
2. **MVP jogável (~45):** E (9), H (30), I (12 primeiros).
3. **Acabamento (~70):** resto de I, J2–J10, K, L, F restantes.

## 6. Observações finais

- A Higgsfield entrega imagens e vídeos, **não o aplicativo**. Telas e animações de uso final serão programadas no app (ex.: Rive ou Lottie), usando estas imagens e vídeos como base.
- Se uma imagem sair com texto ou rosto diferente do piloto, **refaça com a referência anexada** (não mude o prompt).
- Todo desenho bíblico passa pela **revisão doutrinária do autor** antes de entrar no app.
- A logo atual é só um esboço; o briefing da seção J1 não depende dela.
