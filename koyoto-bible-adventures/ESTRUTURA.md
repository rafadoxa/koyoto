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
| Plataformas | **Lançamento só no Google Play (Android)**; **estrutura já preparada para a Apple** depois (base única, ver seção 14) |

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
Abertura (KOYOTO grande no centro, "Oi, KOYOTO")
 └─ "Vamos começar" → KOYOTO encolhe, vai para o canto direito e,
    à esquerda, abre o MENU INICIAL:
     ├─ ADULTO → painel de pais e líderes (salas, equipes, relatório e Plus)
     │           (aqui o responsável escolhe idioma, trilha e vê o aviso de privacidade)
     └─ CRIANÇA → trilhas Exploradores / Desafiantes
                   └─ Personalizar o KOYOTO (apelido de lista, cor, acessórios)

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
5. ~~Plataforma inicial~~ → decidido: Google Play primeiro, Apple depois.
6. Quem fará a revisão doutrinária do conteúdo?

## 15. Personagens bíblicos (estilo e regras)

**Estilo único:** cartoon estilizado, sem realismo, com um **traço de identificação** fácil de reconhecer.
Todo desenho passa por **revisão doutrinária** antes de entrar no app **Revisor: o próprio autor, teólogo formado.**.

**Lista:** Adão, Eva, Noé, Abraão, Moisés, Davi, Jesus, os **doze apóstolos**, Paulo, anjos e sombras (demônios).

### Jesus
- **Alegre, feliz e sábio**, como um **Mestre** (nos Evangelhos Ele é chamado de "Mestre/Rabi"): sorriso aberto, olhar acolhedor, mãos abertas.
- Cenas de acolhida (ex.: com as crianças, Marcos 10:14), ensino e cura. Nada de piada ou caricatura que tire o respeito.
- Sempre o **mesmo desenho** em todo o app (folha de personagem fixa). Revisão doutrinária obrigatória.
- Referência de **tom**: a série *The Chosen* (no Brasil, *Os Escolhidos*), em que Jesus é caloroso, alegre e acolhedor.
  Usar só o clima. **Não copiar o rosto do ator nem imagens da série** (é obra protegida); o nosso Jesus é um desenho original.

### Os doze apóstolos (Mateus 10:2-4)
Para crianças, o traço de identificação **evita símbolos de martírio** (facas, serras, lanças).
Os traços abaixo são sugestões de desenho, sujeitas a revisão.

| # | Apóstolo | Gancho nas Escrituras | Ideia de traço visual |
|---|---|---|---|
| 1 | Pedro (Simão) | Pescador; andou sobre as águas | Rede de pesca e chaves |
| 2 | André | Pescador; trouxe o menino dos pães e peixes (João 6:8-9) | Peixe |
| 3 | Tiago (filho de Zebedeu) | "Filho do trovão" (Marcos 3:17) | Raio/trovão no manto |
| 4 | João | "Filho do trovão"; o discípulo amado | Pergaminho e pena |
| 5 | Filipe | Pergunta sobre os pães (João 6:5-7) | Cesta de pães |
| 6 | Bartolomeu | Tradicionalmente identificado com Natanael (debaixo da figueira, João 1:48) | Folha de figueira |
| 7 | Mateus | Era coletor de impostos | Moedas e livro de contas |
| 8 | Tomé | "Ver para crer" (João 20:24-29) | Lupa ou mão curiosa |
| 9 | Tiago (filho de Alfeu) | Pouco se sabe; só citado nas listas | A definir |
| 10 | Tadeu (Judas, não Iscariotes) | Pouco se sabe (João 14:22) | A definir |
| 11 | Simão, o Zelote | Também chamado Cananeu | A definir |
| 12 | Judas Iscariote | Tesoureiro; traiu Jesus | Bolsa de moedas, tratado com cuidado **[PENDENTE: decisão]** |

**Pontos a decidir:**
- **Judas Iscariote (decidido):** aparece só na história da traição, tratado com seriedade, e **não** é personagem colecionável.
- Os apóstolos 9 a 11 têm pouca informação bíblica; o traço visual deles será **inventado de forma neutra** (decidido).
- Matias (Atos 1:26), que ocupa o lugar de Judas, pode entrar numa fase posterior.

### Demônios (decisão do autor)
- **Nunca nos jogos.** A criança **não luta contra demônios**.
- Aparecem **só na parte das histórias** que tratam de libertação ou do tema, como **sombras abstratas**, sem rosto agressivo, sem chifres, sem sangue.
- Quem age é Jesus (ou o texto bíblico); a criança apenas acompanha a história.

### Anjos
- Formas de luz, amigáveis e serenas; mesmo estilo do mundo cartoon.

### Produção das imagens
- Uma **folha de personagem por figura** (frente, lado, expressões), fixa e reutilizada.
- Começar por: Davi, Noé, Moisés, Jesus (as 3 histórias do MVP e o personagem central).

## 14. Plataformas: Google Play primeiro, Apple depois

**Decisão:** publicar só no **Google Play** na primeira versão, mas construir o app já **pronto para a Apple App Store**,
para não refazer nada quando chegar a hora do iOS.

**Como deixar pronto para a Apple:**
- Usar uma **base de código única** (multiplataforma), por exemplo Flutter ou React Native, com Rive ou Lottie para animar o KOYOTO. A escolha final fica para o protótipo.
- Evitar recursos exclusivos do Android (ex.: serviços só do Google) sem uma alternativa; isolar o que for específico de plataforma em uma camada própria.
- Assinatura Plus por um serviço que atenda as duas lojas (ex.: RevenueCat), para trocar de loja sem reescrever.
- Conteúdo (histórias, perguntas, imagens) guardado em **arquivos de dados**, independente da loja.
- Interface com **tamanhos e áreas seguras** que funcionem também em iPhone e iPad.
- Política de privacidade e regras de dados já escritas pensando na Apple (categoria Kids, rótulos de privacidade).
- Evitar nomes e arquivos que dependam do Android (ícones e telas de abertura gerados por plataforma).

**Para o lançamento no Google Play** (conferir nas páginas oficiais, valores e regras mudam):
- Conta de desenvolvedor do Google Play.
- **Families Policy** e declaração de público-alvo, por ser app infantil.
- Assinatura Plus pelo Google Play.
- Testar em celular e **tablet** (crianças usam muito tablet).
- Jogos em tempo real (duelo, equipes) funcionando bem em redes comuns.

**Depois, para a Apple (fase 2):** conta de desenvolvedor Apple, categoria Kids, revisão mais rígida em apps infantis,
testes em iPhone e iPad. O escopo do MVP da seção 12 continua o mesmo.

## 16. Atualizações recentes

- **Direção de cor da primeira tela:** o fundo D (deserto) agradou, mas a **cor de terra incomodou**.
  Nova direção: **branco/creme + marrom + desenho** (como a referência favorita, o app de leitura infantil).
  Esboço: `esbocos/E-branco-e-marrom.png`. As cores creme, marrom e caramelo são sugestões minhas.
- **Folha de personagem do KOYOTO (v0.1):** `personagens/koyoto-folha-de-personagem.png`
  (pose base, 8 expressões só pelos olhos, 4 acessórios, cores, proporções e tamanhos). O mascote atual **não foi alterado**.
- **Logo:** a versão atual é um **esboço**; o autor **não gostou** e ela só será usada para as lojas, então **fica para depois**.
  Obs.: a mensagem dizia "lobo do Coyoto"; entendi como "logo". **[PENDENTE: confirmar o que incomodou]**
- **Título do app na loja:** a Play Store e a App Store pedem ícone e imagens próprios; ver seção 14.
- **Título da série:** o autor chamou de "Os Enviados"; o título no Brasil que conheço é *Os Escolhidos* **[PENDENTE: conferir]**.
