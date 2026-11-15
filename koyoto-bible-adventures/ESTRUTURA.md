# KOYOTO Bible Adventures — Documento de Estrutura (v0.1)

> Rascunho de planejamento. Nada aqui é código nem decisão jurídica final.
> Itens marcados **[PENDENTE]** precisam de confirmação antes de virar regra.

## 1. Visão

App infantil e juvenil, **gratuito com modo Plus**, para aprender a Bíblia jogando.
O mascote **KOYOTO** acompanha a criança. Idiomas desde o início: **português e inglês**.
Nome do app: **KOYOTO Bible Adventures**.

Público principal: crianças e pré-adolescentes de 8 a 14 anos.
Público de apoio: pais (baixam e configuram) e líderes de igreja (gincanas e equipes).

## 2. Decisões já tomadas

| Tema | Decisão |
|---|---|
| Nome | KOYOTO Bible Adventures (sempre KOYOTO, com K e Y) |
| Faixa etária | Um app só, **duas trilhas**: Exploradores (8-10) e Desafiantes (11-14) |
| Escolha da trilha | Na primeira abertura, **pelo responsável** |
| Modelo de negócio | Grátis + modo Plus discreto, sem anúncios |
| Ilustrações | Geradas por IA, estilo cartoon estilizado, sem realismo |
| Texto bíblico | Ver seção 9 (tradução × paráfrase) **[PENDENTE]** |
| Tema visual | "Diário do Explorador": arquivos de caso, carimbos, papel (ver seção 7) |

## 3. As duas trilhas

| | **Exploradores (8-10)** | **Desafiantes (11-14)** |
|---|---|---|
| Tom do KOYOTO | Amigo brincalhão | Parceiro de equipe, mais "cool" |
| Visual | Cartoon colorido, bem arredondado | Mesmo mundo, mais ação e efeitos |
| Textos | Curtos, versículo curto | Versículo completo, referência e contexto |
| Motivação | Coletar, desbloquear, colorir | Ranking, desafios, tempo, equipes |
| Dificuldade | Mais dicas, sem tempo apertado | Tempo, combos, perguntas de interpretação |

**Regras:**
- O **conteúdo e as histórias são os mesmos**; muda ritmo, texto e dificuldade.
- Irmãos e amigos de trilhas diferentes jogam juntos; a pontuação é **ajustada por faixa**.
- O responsável pode **trocar a trilha** depois, no painel dos pais.

## 4. Retenção e hábito (sem manipulação)

- **Sequência diária (streak)** sem punição agressiva, com **"descanso do KOYOTO"** gratuito aos domingos.
- **Liga semanal só dentro da equipe ou da igreja**, nunca contra estranhos.
- **Todo jogo termina com algo concreto da Bíblia:** o versículo, a referência ("Leia em Josué 6") e uma figurinha. O tempo vira aprendizado, não só pontuação.
- **Sessões curtas (2 a 4 minutos)**, com "só mais uma".
- Evitar compra dentro do jogo feita pela criança e paywall no meio de uma partida.

## 5. Estrutura de telas e fluxo

```
Primeira abertura
 ├─ Tela do responsável: idioma, trilha (Exploradores/Desafiantes), aviso de privacidade
 └─ Criança escolhe apelido (lista) e cor do KOYOTO

Abertura (KOYOTO grande, "Oi, KOYOTO")
 └─ "Vamos começar" → KOYOTO encolhe e vai para o canto direito

ESCRITÓRIO (home) — fundo escuro de mesa
 ├─ Carrossel de ARQUIVOS (uma história = um cartão colorido)
 │    └─ ARQUIVO da história (ex.: Davi)
 │         ├─ Diário (Modo Estudo): cenas, áudio/texto, versículo
 │         ├─ Atividades (jogos individuais)
 │         └─ Competição (duelo, equipe, gincana)
 ├─ Missão do dia (3 mini-desafios)
 ├─ Passaporte (coleção de figurinhas = carimbos, itens do KOYOTO)
 ├─ Salas (criar/entrar por QR Code ou código de 4 letras)
 └─ Painel dos pais/líderes (Plus: relatório, equipes, gincana)
```

**Regras de interface:**
- KOYOTO fica sempre visível ao lado e **reage** (acerto, erro, dica).
- Voz completa fica para uma versão futura; no início, **balões de texto + sons curtos**.
- Falas do KOYOTO são **escritas por nós** (conjunto fechado), **sem IA conversando livremente** com a criança.
- Todo **texto da tela é renderizado no app**, nunca dentro da imagem gerada por IA.

## 6. Mapa dos jogos (20)

Legenda de modo: **S** = solo, **E** = equipe, **G** = gincana presencial.
"Variação" mostra como muda por trilha.

| # | Jogo | Mecânica | Ligação com a Bíblia | Modo | Variação por trilha |
|---|---|---|---|---|---|
| 1 | Memória relâmpago | Cartas aparecem, viram, achar os pares | Personagem × objeto, versículo × livro | S/E | Mais pares e menos tempo nos Desafiantes |
| 2 | Onde estava? | Cena some, apontar onde cada personagem estava | Memória visual da história | S | Mais personagens |
| 3 | Arca 2048 (merge) | Juntar animais iguais para evoluir | Noé | S | Pergunta a cada N jogadas, com tempo nos Desafiantes |
| 4 | Muralha de Jericó | Empilhar blocos no ritmo certo | Josué | S/E | Ritmo mais rápido |
| 5 | Torre alta | Empilhar com timing, cada andar um versículo | Babel | S | Versículo completo nos Desafiantes |
| 6 | Combina 3 bíblico | Match-3 com ícones bíblicos | Qualquer história | S | Combos e metas |
| 7 | Funda de Davi | Puxar e soltar; só atira após acertar a pergunta | Davi e Golias | S/E | Alvos móveis |
| 8 | Corrida do KOYOTO | Corredor infinito, pegar respostas certas | Êxodo | S | Velocidade crescente |
| 9 | Cruze o Mar | Escolher portas certas antes que fechem | Moisés | S/E | Mais portas e tempo |
| 10 | Quebra-cabeça de vitral | Montar a cena em peças | Ilustração da história | S | Mais peças |
| 11 | Detetive bíblico | Pistas surgem, acertar cedo vale mais | Personagens | S/E | Pistas mais abstratas |
| 12 | Linha do tempo | Arrastar eventos na ordem | Visão geral da Bíblia | S/E | Mais eventos |
| 13 | Versículo escondido | Palavras caem como Tetris, encaixar na ordem | Memorização | S | Versículo maior |
| 14 | Caça aos itens | Achar objetos na cena | Parábolas | S | Menos pistas visuais |
| 15 | Bolhas da verdade | Estourar só as bolhas da resposta certa | Qualquer tema | S | Pergunta de interpretação |
| 16 | Missão do dia | 3 mini-desafios de jogos diferentes | Variado | S | Dificuldade da trilha |
| 17 | Duelo relâmpago 1x1 | Mesma pergunta, vence quem acerta mais rápido | Variado | Online/QR | Pontos ajustados por faixa |
| 18 | Gincana de times (até 10) | Times A e B, rodadas de jogos, placar ao vivo | Variado | E (Plus) | Equipes mistas permitidas |
| 19 | Mímica e desenho | Um desenha/faz mímica, o time adivinha | Personagens e cenas | G | Cartas diferentes por faixa |
| 20 | Caça ao tesouro da igreja | Líder esconde QR Codes, cada um libera uma pergunta | Variado | G (Plus) | Perguntas por faixa |

**Prioridade de protótipo (MVP):** 1, 3, 7, 12, 17. Servem para testar o ciclo "jogo → versículo → figurinha".

## 7. Direção visual (a partir das 5 referências)

Tema: **"Diário do Explorador"**.

- **Arquivo de caso (cartão da história):** pasta de papel pardo, carimbo, clipe.
- **Carrossel:** cartões altos e arredondados, cada história de uma cor chapada, botão de favorito.
- **Navegação:** grade de 2 colunas, filtros em pílula, barra inferior, detalhe com personagem grande.
- **Abertura e mapa:** cenário em camadas de papel recortado (usar com moderação, é caro de gerar).
- **Modo Estudo:** leitura limpa com alternador Áudio/Texto, letra capitular e tamanho de letra ajustável.

**Paleta** (as quatro primeiras estão escritas numa das referências; as demais são estimadas):

| Cor | Código |
|---|---|
| Laranja | `#F18F0B` |
| Vermelho-alaranjado | `#EF491D` |
| Verde-petróleo | `#456B5F` |
| Mostarda | `#B79F0F` |
| Papel creme (estimado) | ~`#F3E6C8` |
| Marrom escuro de fundo (estimado) | ~`#2B1B12` |

**Tipografia (a testar):** máquina de escrever para títulos de "caso" (ex.: Special Elite),
condensada em caixa-alta para rótulos (ex.: Barlow Condensed), arredondada para leitura (ex.: Nunito).

**Cuidados:**
- As referências são trabalhos de terceiros: usar só como **inspiração de estilo**, sem copiar personagens ou layouts.
- O KOYOTO precisa de desenho **simples o bastante** para manter consistência em centenas de imagens.

## 8. Imagens por IA

- Criar uma **folha de personagem** fixa do KOYOTO e dos personagens recorrentes; usar como referência em todo pedido.
- Fazer um **piloto de 10 imagens** antes de gerar o catálogo inteiro.
- Custo de referência (a reconfirmar): Imagen 4 Fast ~US$ 0,02 por imagem, Standard ~US$ 0,04; modo em lote costuma custar metade.
- **Revisão humana** de todas as cenas bíblicas (roupas, época, representação respeitosa).
- Nenhum texto dentro das imagens.

## 9. Texto bíblico **[PENDENTE]**

Não foi possível confirmar a situação de direitos das traduções:
- Almeida Revista e Corrigida: a busca indicou edição de 1948, não 1898; domínio público confirmado só para a Almeida de 1641 (linguagem antiga demais para crianças).
- KJV e World English Bible: não confirmados nesta pesquisa.

**Caminho recomendado:** paráfrases curtas em linguagem infantil, com a **referência bíblica ao lado**,
revisadas por alguém de confiança doutrinária. Antes de citar qualquer tradução literal, **confirmar a licença** da edição.

## 10. Plus (monetização discreta)

| Grátis | Plus |
|---|---|
| KOYOTO, algumas histórias completas, jogos individuais básicos, duelo 1x1, missão do dia | Todas as histórias e jogos |
| Convidar amigo por QR Code | Equipes de até 10 e gincanas |
| | Itens extras do KOYOTO, relatório para os pais, modo offline completo |
| | Plano igreja (líder de ministério infantil) |

Planos mensal e anual. Sem anúncios.

## 11. Privacidade e regras de loja **[PENDENTE — validar com profissional]**

- Cadastro feito pelo **responsável**; a criança usa apelido de lista, sem nome real.
- **Sem chat livre**; interação entre crianças só por figurinhas e reações prontas.
- Coletar o mínimo de dados; sem anúncios de terceiros.
- Conferir Google Play (Families Policy), Apple (categoria Kids), COPPA e LGPD (idade e consentimento) antes do lançamento.

## 12. Escopo sugerido da primeira versão (MVP)

1. Fluxo de primeira abertura + escolha da trilha.
2. KOYOTO animado na abertura e reações básicas.
3. Escritório com carrossel e 3 histórias (Davi, Noé, Moisés).
4. 5 jogos do mapa (1, 3, 7, 12, 17).
5. Passaporte com figurinhas.
6. Duelo 1x1 por QR Code.

Fora do MVP: equipes de 10, gincana presencial, itens do KOYOTO, voz, plano igreja.

## 13. Perguntas em aberto

1. Como é o KOYOTO hoje (imagem do mascote atual)?
2. O tema "detetive/explorador" e "Arquivos" está aprovado?
3. Fundo marrom escuro de "mesa" está bom?
4. Texto bíblico: paráfrase, tradução licenciada ou domínio público?
5. Plataforma inicial: Android, iOS ou os dois?
6. Quem fará a revisão doutrinária do conteúdo?
