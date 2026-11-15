# Passagem de contexto — KOYOTO Bible Adventures

Resumo para quem for assumir o projeto (responsáveis por site e aplicativo). Escrito em 2026-11-15.
Os detalhes completos estão em `ESTRUTURA.md`; este arquivo é o ponto de partida.

## O que é
App infantil e juvenil (8 a 14 anos) para aprender a Bíblia jogando, com o mascote **KOYOTO** (sempre escrito assim).
Gratuito, com modo **Plus** discreto, sem anúncios. Idiomas: português e inglês. Nome na loja: **KOYOTO Bible Adventures**.

## Decisões já tomadas pelo autor
- Um app só, com duas trilhas: **Exploradores (8-10)** e **Desafiantes (11-14)**.
- Primeira tela: KOYOTO grande no centro → ele diminui para a direita → menu à esquerda **Adulto / Criança**.
  Adulto = painel de pais e líderes (salas, equipes, relatório, Plus). Criança = trilhas e personalização do KOYOTO.
- **Plataforma: só Google Play primeiro**, mas a estrutura deve ficar pronta para a Apple (base única, camada de plataforma isolada).
- **Demônios nunca nos jogos**; só nas histórias de libertação, como sombras abstratas, sem a criança lutar.
- **Judas Iscariote** só na história da traição, não colecionável. Doze apóstolos no total.
- Jesus: alegre e sábio, desenho original (tom inspirado em *The Chosen*, sem copiar rosto nem imagens).
- Revisão doutrinária: feita pelo próprio autor (teólogo formado).
- Visual: direção **branco/creme + marrom + desenho** (a cor de terra do esboço D incomodou); referência favorita: app de leitura infantil (Kidory).
- Logo atual é só um esboço; o autor não gostou e ela só será usada nas lojas, fica para depois.

## O que já existe no repositório (pasta `koyoto-bible-adventures/`)
- `ESTRUTURA.md`: visão, trilhas, retenção, fluxo, 20 jogos, visual, Plus, privacidade, MVP, personagens, plataformas.
- `esbocos/`: 5 fundos da primeira tela (A a D, mais E em branco e marrom).
- `personagens/koyoto-folha-de-personagem.png`: folha do mascote (expressões, acessórios, cores).
- `logo/`: esboço da logo em SVG e PNG.
- `referencias/`: pasta para imagens de referência de estilo.

## Pendências
1. Tradução bíblica: direitos não confirmados; recomendação atual é paráfrase infantil com a referência ao lado.
2. Privacidade e regras de loja (Google Play Families Policy, LGPD, COPPA): validar com profissional.
3. Confirmar o que incomodou na logo ("lobo do Coyoto" foi lido como "logo").
4. Título brasileiro da série citada: o autor disse "Os Enviados"; conferir.
5. Folha de personagem de Jesus e das demais figuras bíblicas.
6. Desenho da tela do menu Adulto/Criança e da personalização do KOYOTO.
7. Escolher a tecnologia (Flutter ou React Native) no protótipo e iniciar o MVP da seção 12.

## Cuidados
- Texto de tela sempre no código, nunca dentro das imagens geradas por IA.
- Imagens bíblicas geradas por IA passam por revisão do autor antes de entrar.
- Referências visuais são de terceiros: usar só como inspiração de estilo.
