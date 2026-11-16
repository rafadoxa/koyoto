# KOYOTO Bible Adventures — Especificação completa do app (v1.0 para o Codex)

Fonte da verdade do produto e da parte técnica. O contexto e o histórico estão em `ESTRUTURA.md`.
Itens **[DECISÃO]** foram decididos pelo autor; **[RECOMENDAÇÃO]** é minha sugestão técnica, que o Codex pode ajustar
justificando em `DECISIONS.md`; **[OWNER]** depende do autor (teologia, licenças, contas).

---

## 1. Produto

**Nome:** KOYOTO Bible Adventures (sempre "KOYOTO", com K e Y). **[DECISÃO]**
**Resumo:** app infantil e juvenil (8 a 14 anos) para aprender a Bíblia jogando, com o mascote KOYOTO, histórias, jogos curtos,
figurinhas colecionáveis e partidas entre amigos. Gratuito, com assinatura opcional **Plus**, sem anúncios.
**Idiomas:** português (Brasil) e inglês desde o início.
**Plataforma:** **Google Play primeiro**, com a estrutura já pronta para a Apple App Store depois. **[DECISÃO]**
**Usuários:** criança/pré-adolescente (jogador), responsável e líder de igreja (administram contas, salas e equipes).

### Objetivos
1. A criança aprende e lê a Bíblia com prazer; cada jogo termina com o versículo e a referência.
2. Sessões curtas (2 a 4 minutos) que dão vontade de "só mais uma".
3. Igrejas usam o app em gincanas, células e pequenos grupos (equipes de até 10).

### Fora de escopo da v1
Voz do KOYOTO e reconhecimento de voz, chat livre, ranking global, conteúdo gerado por IA em tempo real, versão iOS publicada.

---

## 2. Trilhas por idade **[DECISÃO]**

Um app só, duas trilhas escolhidas pelo responsável (e alteráveis no painel dos pais).

| | **Exploradores (8-10)** | **Desafiantes (11-14)** |
|---|---|---|
| Tom do KOYOTO | Amigo brincalhão | Parceiro de equipe, mais "cool" |
| Visual | Cartoon colorido, bem arredondado | Mesmo mundo, mais ação e efeitos |
| Textos | Curtos, versículo curto | Versículo completo, referência e contexto |
| Motivação | Coletar, desbloquear, colorir | Ranking, desafios, tempo, equipes |
| Dificuldade | Mais dicas, sem tempo apertado | Tempo, combos, perguntas de interpretação |

O **conteúdo (histórias e perguntas) é o mesmo**; cada item tem campos por trilha quando necessário (`short`, `full`, `hint`).
Partidas entre trilhas diferentes ajustam a pontuação (seção 9).

---

## 3. Fluxo e telas **[DECISÃO]**

```
S1 Abertura
   KOYOTO grande e centralizado, olhos que piscam e brilham. Botão "Oi, KOYOTO!".
   (Sem voz na v1: só toque.)
   └─ ao tocar: KOYOTO encolhe e desliza para o canto DIREITO; à ESQUERDA abre o menu:
S2 Menu inicial
   ├─ ADULTO  → S12 Painel de pais e líderes (protegido por parental gate)
   └─ CRIANÇA → S3 Escolha da trilha (se ainda não escolhida) → S4 Personalizar o KOYOTO → S5 Escritório

S5 Escritório (home da criança)
   KOYOTO pequeno à direita, reagindo. Carrossel de ARQUIVOS (histórias) em cartões coloridos.
   Atalhos: Missão do dia, Passaporte, Salas, Streak.
S6 Arquivo da história (ex.: Davi)
   ├─ Diário (Modo Estudo) → S7
   ├─ Atividades (jogos individuais) → S8 lista de jogos → S9 jogo
   └─ Competição (duelo, equipe, gincana) → S11 Salas
S7 Diário: cenas com texto curto, alternador Áudio/Texto, letra capitular, perguntas leves.
S8 Lista de jogos da história
S9 Tela de jogo (um dos 20 jogos)
S10 Fim de jogo: pontos, versículo (paráfrase) + referência ("Leia em Josué 6"), figurinha ganha, botão "Só mais uma".
S11 Salas: criar sala (código de 4 letras + QR), entrar, lobby, partida, placar.
S12 Painel de pais/líderes: perfis, trilha, relatório, equipes/salas, Plus, privacidade, apagar dados.
S13 Passaporte: coleção de figurinhas (carimbos) e itens do KOYOTO.
S14 Missão do dia: 3 mini-desafios de jogos diferentes.
```

Regras de interface:
- O KOYOTO está sempre visível ao lado e **reage** (acerto, erro, dica, comemoração).
- Parental gate (conta matemática ou segurar o botão) antes de compra, link externo ou configurações.
- Alvos de toque ≥ 48dp, texto escalável, contraste adequado, sem depender só de cor.

---

## 4. Design system

### Direção visual **[DECISÃO]**
Branco/creme + marrom + desenho cartoon (cantos bem arredondados, formas grandes, cores chapadas), no espírito do app de leitura infantil
da referência. Tema "Diário do Explorador": arquivos de caso, carimbos, papel recortado em camadas. Primeira tela com fundo creme
e colinas em camadas (esboço `esbocos/E-branco-e-marrom.png`).

### Tokens
| Token | Valor |
|---|---|
| cream | `#FFF7EA` |
| paper | `#F3E6C8` |
| brown | `#4A2C1D` |
| caramel | `#B9794B` |
| orange | `#F18F0B` |
| red-orange | `#EF491D` |
| teal | `#456B5F` |
| mustard | `#B79F0F` |
| lime (destaques/Plus) | `#D9F23F` |
| mascot-border-gradient | `#FF3D8B` → `#FF8A3D` → `#FFB43D` (135°) |
| mascot-face | `#1B1B1D` → `#09090A` (vertical) |
| radii | cartões 28; botões pílula 999; cartão grande 36 |
| sombras | suaves, cor marrom a 25–35% |

Tipografia (fontes embutidas no app, não baixadas em tempo de execução; licenças OFL/Apache a conferir):
títulos **Lilita One**; rótulos em caixa-alta **Barlow Condensed**; leitura **Nunito**; títulos de "caso" opcional **Special Elite**.

### Mascote KOYOTO (desenhar nativamente, sem redesenhar) **[DECISÃO]**
Geometria (lado = L): quadrado de cantos ≈ 27% de L; borda em degradê ≈ 6,5% de L com contorno marrom; rosto escuro interno
(cantos ≈ 21% de L); **dois olhos brancos ovais** ≈ 18% × 29% de L, com brilho (glow); o olho direito ligeiramente mais alto que o esquerdo.
Sem boca. A emoção vem dos olhos e do movimento.

| Expressão | Olhos |
|---|---|
| normal | ovais |
| alegre | dois arcos "^ ^" |
| surpreso | ovais maiores |
| pensando | um olho oval, outro meio fechado + traço de sobrancelha |
| triste | ovais menores, caídos, sobrancelhas inclinadas para cima no centro |
| piscando | um oval e um arco |
| descansando | arcos para baixo + "z" |
| comemorando | estrelas douradas |

Acessórios (camadas por cima): chapéu de explorador, lenço vermelho, óculos redondos, capa curta.
Animações: respirar (escala sutil em loop), piscar, pular, balançar, brilho pulsando, encolher e deslizar (transição S1→S2).
Regras: nunca esticar; girar no máximo 10°; sempre manter a borda em degradê. Arquivo de referência: `personagens/koyoto-folha-de-personagem.png`.

---

## 5. Conteúdo e dados

### Histórias do MVP (3) e seguintes
MVP: **Davi** (1 Samuel 17), **Noé** (Gênesis 6–9), **Moisés** (Êxodo 14). Depois: Abraão, Adão e Eva, Josué, Daniel, José, Jonas, Ester, Jesus e Paulo.
**Doze apóstolos**: todos presentes; **Judas Iscariote** só na história da traição, não colecionável. **[DECISÃO]**
**Demônios**: nunca nos jogos; só em textos de histórias de libertação, como sombra abstrata; a criança não luta contra eles. **[DECISÃO]**

### Texto bíblico **[OWNER]**
Nesta fase use **paráfrases curtas** + a **referência** (ex.: "Josué 6"). Nenhuma tradução literal até o autor confirmar a licença.
O autor é teólogo e revisa todo conteúdo. Campo `reviewed` (booleano): **builds de release escondem itens com `reviewed=false`**.

### Estrutura de dados (JSON em `assets/content/`)

```jsonc
// story.json
{
  "id": "david",
  "order": 1,
  "color": "#F18F0B",
  "reference": "1 Samuel 17",
  "title": { "pt": "Davi e o gigante", "en": "David and the giant" },
  "cardImage": "assets/cards/david.png",
  "reviewed": false,
  "scenes": [
    { "id": "d1", "image": "assets/scenes/david_1.png",
      "text": { "pt": { "short": "Davi cuidava das ovelhas do pai.", "full": "Davi, o mais novo, cuidava das ovelhas do pai e confiava em Deus." },
                "en": { "short": "David took care of his father's sheep.", "full": "David, the youngest, looked after his father's sheep and trusted God." } },
      "audio": null }
  ],
  "verse": { "reference": "1 Samuel 17:47",
             "pt": "A vitória vem de Deus.", "en": "The victory comes from God.", "reviewed": false },
  "sticker": "sling"
}

// question.json
{ "id": "david_q1", "story": "david", "type": "multiple_choice", "level": 1,
  "track": ["exploradores", "desafiantes"],
  "prompt": { "pt": "O que Davi usou contra Golias?", "en": "What did David use against Goliath?" },
  "options": [ { "pt": "Uma funda", "en": "A sling", "correct": true },
              { "pt": "Uma espada", "en": "A sword" }, { "pt": "Um cajado", "en": "A staff" } ],
  "hint": { "pt": "Era feita de couro.", "en": "It was made of leather." },
  "interpretation": false,           // true: pergunta de interpretação (só Desafiantes)
  "reference": "1 Samuel 17:40", "reviewed": false }

// sticker.json
{ "id": "sling", "image": "assets/stickers/sling.png", "story": "david",
  "name": { "pt": "Funda", "en": "Sling" }, "rarity": "common", "collectible": true }
```

Tipos de pergunta: `multiple_choice`, `true_false`, `order` (arrastar na ordem), `match` (pares), `fill_verse` (completar a palavra).
Mínimo por história no MVP: 12 perguntas (4 por nível de dificuldade).

### Figurinhas (24 selos do passaporte)
funda, arca, pomba, cajado, sarça ardente, tábuas, cordeiro, estrela, peixe, pão, chave, lanterna, pergaminho, harpa, coroa de oliveira,
muralha de Jericó, arco-íris, folha de figueira, moedas, âncora, sandália, tenda, camelo, asa de anjo.

---

## 6. Regras de hábito (retenção) **[DECISÃO]**

- **Streak diário:** conta se a criança completa pelo menos 1 jogo no dia. Domingo é **"descanso do KOYOTO"** gratuito (não quebra a sequência).
  1 **proteção (freeze)** gratuita por semana. Sem mensagens de culpa; notificações só se o responsável ativar.
- **Liga semanal:** apenas **dentro de uma sala, equipe ou grupo da igreja**; zera na segunda-feira. Nunca contra desconhecidos.
- **Fim de jogo sempre entrega:** paráfrase do versículo + referência + figurinha.
- **Sessões de 2 a 4 minutos**, botão "Só mais uma".
- Moedas e itens do KOYOTO são **conquistados jogando**; nada de compra feita pela criança.

---

## 7. Os 20 jogos **[DECISÃO]**

Modos: S = solo, E = equipe, G = gincana presencial. Todos terminam com versículo + referência + figurinha.
Trilha **Exploradores**: dicas disponíveis, sem tempo apertado. **Desafiantes**: tempo, combos e perguntas de interpretação.

| # | Jogo | Mecânica | Bíblia | Modo | MVP |
|---|---|---|---|---|---|
| 1 | Memória relâmpago | Cartas viram e somem, achar os pares | Personagem×objeto, versículo×livro | S/E | **Sim** |
| 2 | Onde estava? | Cena some, apontar onde cada personagem estava | História | S | |
| 3 | Arca 2048 (merge) | Juntar animais iguais para evoluir; pergunta a cada N jogadas | Noé | S | **Sim** |
| 4 | Muralha de Jericó | Empilhar blocos no ritmo certo | Josué | S/E | |
| 5 | Torre alta | Empilhar com timing, cada andar um versículo | Babel | S | |
| 6 | Combina 3 bíblico | Match-3 com ícones bíblicos | Variado | S | |
| 7 | Funda de Davi | Puxar e soltar; só atira após acertar a pergunta | Davi | S/E | **Sim** |
| 8 | Corrida do KOYOTO | Corredor infinito; pegar respostas certas | Êxodo | S | |
| 9 | Cruze o Mar | Escolher portas certas antes que fechem | Moisés | S/E | |
| 10 | Quebra-cabeça de vitral | Montar a cena em peças | História | S | |
| 11 | Detetive bíblico | Pistas surgem; acertar cedo vale mais | Personagens | S/E | |
| 12 | Linha do tempo | Arrastar eventos na ordem | Visão geral | S/E | **Sim** |
| 13 | Versículo escondido | Palavras caem como Tetris, encaixar na ordem | Memorização | S | |
| 14 | Caça aos itens | Achar objetos na cena | Parábolas | S | |
| 15 | Bolhas da verdade | Estourar só as bolhas da resposta certa | Variado | S | |
| 16 | Missão do dia | 3 mini-desafios de jogos diferentes | Variado | S | |
| 17 | Duelo relâmpago 1x1 | Mesma pergunta, vence quem acerta mais rápido | Variado | Online/QR | **Sim** |
| 18 | Gincana de times (até 10) | Times A e B, rodadas, placar ao vivo | Variado | E (Plus) | |
| 19 | Mímica e desenho | Um representa, o time adivinha | Personagens | G | |
| 20 | Caça ao tesouro da igreja | Líder esconde QR Codes; cada um libera uma pergunta | Variado | G (Plus) | |

### Regras detalhadas dos 5 jogos do MVP

**Pontuação base (todos):** +10 por acerto; +5 de bônus de velocidade só nos **Desafiantes** (decai de 5 a 0 ao longo de 8 s);
combo ×1,2 a partir de 3 acertos seguidos (máx. ×2); erro não tira pontos, apenas zera o combo.
**Partidas mistas:** pontos dos Exploradores ×1,0; dos Desafiantes ×0,8 (ajuste a calibrar em teste).

**1. Memória relâmpago.** Grade 3×4 (Exploradores) ou 4×4 (Desafiantes). Mostra todas as cartas por 3 s (Exploradores) ou 2 s (Desafiantes),
vira e embaralha. Achar os pares (personagem×objeto ou versículo×livro). Dica: revela 1 par (Exploradores, 1 vez). Fim: todos os pares. Meta de 2 a 3 min.
**3. Arca 2048.** Tabuleiro 4×4; deslizar para juntar animais iguais (cordeiro → bode → boi → camelo → elefante). A cada 8 jogadas (Desafiantes: 6),
surge uma pergunta; resposta certa dá uma jogada extra, errada não penaliza. Fim: chegar ao elefante ou tabuleiro cheio. Meta de 3 a 4 min.
**7. Funda de Davi.** Aparece uma pergunta; ao acertar, libera um disparo: puxar e soltar para acertar o alvo (Exploradores: alvo grande e parado;
Desafiantes: alvo móvel). 5 rodadas. Fim: 5 rodadas. Meta de 2 a 3 min.
**12. Linha do tempo.** 5 cartões de eventos (Exploradores) ou 7 (Desafiantes) para arrastar na ordem certa; imagem em cada cartão.
Tempo: livre (Exploradores) ou 60 s (Desafiantes). Fim: ordem completa ou tempo.
**17. Duelo 1x1.** Sala por QR ou código de 4 letras; 7 perguntas iguais para os dois, 10 s cada; pontua quem acerta mais rápido. Empate: pergunta extra.
Sem chat; reações prontas (emojis do KOYOTO). Desconexão: o outro jogador vence após 15 s.

Os demais jogos seguem a tabela; Codex implementa depois do MVP (milestone M8), reaproveitando o motor de perguntas.

---

## 8. Multijogador, salas e equipes **[RECOMENDAÇÃO]**

- Supabase: **Auth** (apenas para o responsável) e **Realtime** para salas. A criança joga com perfil local, vinculado à conta do responsável.
- **Sala:** código de 4 letras + QR com *deep link* (`koyoto://room/ABCD`); quem não tem o app é levado à Google Play.
- Papéis: host (cria e inicia), jogadores. **Grátis:** duelo 1x1. **Plus:** equipes de até 10, gincana A×B, ranking da liga.
- Sem chat. Apelidos escolhidos de lista (sem nome real). Expulsar jogador (host). Tempo de vida da sala: 2 h.
- Sincronização: o servidor define a ordem das perguntas e o tempo; o cliente envia só a resposta. Evitar confiar no relógio do cliente.
- Segurança: regras de acesso (RLS) por sala; nenhum dado pessoal da criança no banco; limites de criação de salas por conta.

---

## 9. Plus (monetização discreta) **[DECISÃO]**

| Grátis | Plus |
|---|---|
| KOYOTO, histórias do MVP, jogos individuais básicos, duelo 1x1, missão do dia, convidar amigo por QR | Todas as histórias e jogos |
| | Equipes até 10, gincanas, ranking da liga |
| | Itens extras do KOYOTO, relatório para os pais, modo offline completo |
| | Plano igreja (líder de ministério infantil) |

Assinatura mensal e anual via **Google Play Billing**, gerenciada por **RevenueCat** (para a Apple depois sem refazer). Compra só atrás de parental gate.
Sem anúncios. Sem compra feita pela criança.

---

## 10. Privacidade, segurança e lojas **[OWNER: validar com profissional]**

- **Sem anúncios e sem SDKs de terceiros de anúncio/analytics.** Métricas mínimas e anônimas (ex.: erros) com consentimento do responsável.
- Conta apenas do **responsável** (e-mail). Criança: apelido da lista e avatar; sem nome real, foto, localização ou chat.
- Dados mínimos; botão **"Apagar todos os dados"** no painel dos pais.
- Parental gate em compras, links externos e configurações.
- Para o Google Play: seguir a **Families Policy**, declarar o público-alvo, política de privacidade publicada, formulário de segurança de dados.
  Considerar COPPA (EUA) e LGPD (Brasil; consentimento dos pais para dados de criança). **Não presumir idades legais: o autor confirma com profissional.**
- Preparado para a Apple: categoria Kids, rótulos de privacidade, sem rastreamento.
- Conteúdo: sem imagens assustadoras; demônios só como sombra abstrata nas histórias; nada que a criança "enfrente".

---

## 11. Arquitetura técnica **[RECOMENDAÇÃO]**

- **Flutter** (stable), **Riverpod**, **go_router**, **freezed/json_serializable** para modelos.
- **Local-first:** conteúdo e imagens no pacote; progresso em **Drift/SQLite** (ou Isar); sincronização opcional com Supabase para pais.
- **Mascote:** `CustomPainter` com 8 expressões e animações (AnimationController); sem dependência de Rive na v1.
- **Jogos:** widgets Flutter para cartas/arrastar (1, 12, 3); **Flame** para funda (7) e corredor (8).
- **Efeitos:** Lottie para confete, brilho e carimbo (arquivos criados depois).
- **Áudio:** `just_audio`; sons curtos; narração opcional futura.
- **i18n:** `flutter_localizations` + arquivos ARB (`pt`, `en`). Nenhum texto fixo em widgets.
- **Plataforma isolada:** interfaces `BillingService`, `PushService`, `ShareService` com implementações Android; stubs prontos para iOS.
- **Testes:** unitários para pontuação, streak, liga e regras dos jogos; widget tests das telas S1, S5, S10; teste de integração do fluxo S1→S10.

### Estrutura de pastas
```
lib/
  core/ (theme, tokens, l10n, router, utils, services)
  data/ (models, repositories, content_loader, db)
  features/
    onboarding/ (splash, menu, track_select, mascot_customize)
    home/ (office, story_carousel, streak_bar)
    story/ (story_detail, study_diary)
    games/ (engine/, memory/, ark2048/, sling/, timeline/, duel/ ...)
    rewards/ (results, passport, stickers)
    rooms/ (lobby, realtime, qr)
    parents/ (dashboard, gate, plus, privacy)
  shared/ (mascot/, widgets/)
assets/ (content/, cards/, scenes/, stickers/, backgrounds/, games/, animations/, fonts/)
test/
```

---

## 12. Milestones (ordem de trabalho)

| M | Entrega | Critério de aceite |
|---|---|---|
| **M0** | Scaffold, tokens, tema, l10n (pt/en), mascote com 8 expressões, CI (analyze + test) | App abre; mascote anima; sem erros do analyzer |
| **M1** | S1 abertura → S2 menu → S3 trilha → S4 personalizar | Transição do mascote fluida; escolha de trilha persistida |
| **M2** | S5 escritório + carrossel; S6 arquivo; S7 diário (3 histórias do MVP com conteúdo `reviewed=false` visível só em debug) | Navegação completa; texto por trilha; áudio/texto alterna |
| **M3** | Motor de perguntas + jogos 1, 3, 7, 12 | Regras da seção 7 testadas; 2–4 min por partida |
| **M4** | S10 fim de jogo, figurinhas, passaporte, streak (com domingo e freeze), missão do dia | Testes de streak passam; ciclo jogo→versículo→figurinha |
| **M5** | Salas por QR/código e duelo 1x1 (Supabase Realtime) | 2 aparelhos jogam; desconexão tratada |
| **M6** | Painel de pais, parental gate, Plus (RevenueCat), privacidade, apagar dados | Compra de teste funciona; gate bloqueia a criança |
| **M7** | Acabamento para a Google Play: ícone, capturas, política, formulários, testes em tablet, desempenho | Build assinado (AAB); checklist da Play concluído |
| **M8** | Demais jogos (2, 4–6, 8–11, 13–15), equipes (18), gincana presencial (19, 20), mais histórias | Um jogo por vez, com testes |

Cada milestone: `flutter analyze`, `flutter test`, build Android, atualização de `CHANGELOG.md`, decisões em `DECISIONS.md`, pendências do autor em `OWNER-TODO.md`.

---

## 13. Qualidade, desempenho e acessibilidade

- 60 fps em aparelhos de entrada; partida inicial em < 3 s; APK/AAB enxuto (imagens em WebP/PNG otimizados).
- Funciona **offline** com o conteúdo gratuito; salas exigem rede.
- Acessibilidade: rótulos semânticos, alvos ≥ 48dp, contraste, escala de texto, não depender só de cor, opção de reduzir animações.
- Logs sem dados pessoais.

---

## 14. Pendências do autor **[OWNER]**

1. Revisão doutrinária (teólogo): histórias, perguntas, versículos e imagens, **principalmente Jesus**.
2. Licença da tradução bíblica (ou manter paráfrases curtas).
3. Contas: Google Play Console, Supabase, RevenueCat (chaves nunca no repositório).
4. Política de privacidade e termos, validados com profissional (LGPD/COPPA/Play Families).
5. Logo final (a atual é esboço; o autor não gostou) e ícone do app.
6. Decidir Judas Iscariote (só na história da traição), traços visuais dos apóstolos 9–11.
7. Eva sem serpente/maçã no material de Adão e Eva (se a intenção for só o Jardim).
8. Confirmar o título brasileiro da série usada como referência de tom para Jesus (*The Chosen*).

---

## 15. Manifesto de assets (nomes que o Codex espera em `assets/`)

| Pasta | Arquivos |
|---|---|
| `assets/mascot/` | `koyoto_sheet.png` (referência, não usar no app); acessórios se forem imagens |
| `assets/characters/` | `david.png`, `noah.png`, `moses.png`, `abraham.png`, `adam.png`, `eve.png`, `paul.png`, `angel.png`, `jesus_1..4.png`, `apostle_peter.png`, `apostle_andrew.png`, `apostle_james_zebedee.png`, `apostle_john.png`, `apostle_philip.png`, `apostle_bartholomew.png`, `apostle_matthew.png`, `apostle_thomas.png`, `apostle_james_alphaeus.png`, `apostle_thaddaeus.png`, `apostle_simon_zealot.png`, `apostle_judas.png` |
| `assets/scenes/` | `david_1..3.png`, `noah_1..3.png`, `moses_1..3.png` |
| `assets/cards/` | `david.png`, `noah.png`, `moses.png`, … (um por história, 3:5) |
| `assets/backgrounds/` | `splash.png`, `office.png`, `map.png`, `menu.png`, `night_desert.png`, `garden.png`, `lake.png`, `mountain.png` |
| `assets/stickers/` | 24 arquivos (`sling.png`, `ark.png`, …) |
| `assets/games/` | cartas da memória, peças da Arca 2048, alvo/funda, cartões e corda da linha do tempo, selos do duelo, moeda, estrela, confete |
| `assets/animations/` | `.mp4`/`.gif` curtos e, depois, Lottie (`confetti.json`, `stamp.json`) |
| `assets/fonts/` | Lilita One, Barlow Condensed, Nunito, Special Elite |
| `assets/content/` | `stories.json`, `questions.json`, `stickers.json`, `l10n` |

Se alguma imagem faltar, o Codex usa um **placeholder** claro e registra em `OWNER-TODO.md`; nunca inventa imagem bíblica.
