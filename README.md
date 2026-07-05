# Tempos & Trocas — Guia de Matchups do Jax

Site estático (HTML/CSS/JS puro, sem build) com os 43 matchups da Planilha 2026,
com busca, ladder visual de cooldowns por rank e o plano de lane de cada campeão.

## Rodar localmente
Basta abrir `index.html` no navegador, ou:
```bash
npx serve .
```

## Publicar no Vercel

**Opção A — pelo site (mais fácil):**
1. Crie um repositório no GitHub e suba esta pasta (`index.html`, `vercel.json`).
2. Entre em https://vercel.com/new e importe o repositório.
3. Framework preset: **Other**. Não precisa de build command nem output directory.
4. Clique em Deploy.

**Opção B — pela CLI:**
```bash
npm i -g vercel
cd jax-site
vercel
```
Siga as perguntas (aceite os padrões) e o Vercel te dará a URL pública.

## Estrutura
- `index.html` — site inteiro (dados, estilos e lógica embutidos)
- `vercel.json` — configuração mínima de deploy
- `assets/nicklink-logo.png` — logo Nick Link (cabeçalho e rodapé)

## Ícones das habilidades
Cada card de cooldown busca automaticamente, no Data Dragon, o ícone real da
habilidade (passiva, Q, W, E, R) daquele campeão e o mostra dentro do círculo
colorido. A busca é feita sob demanda (ao abrir a página do campeão) e fica
em cache no navegador durante a sessão.

## Vídeos
Cada matchup tem um vídeo do YouTube incorporado (player oficial embutido via iframe,
o mesmo mecanismo usado por qualquer blog ou site de fãs) mostrando a lane Jax vs
aquele campeão, além de um link "Ver mais vídeos" que abre a busca do YouTube para
esse matchup específico.

## Imagens
Os ícones e as splash arts dos campeões (incluindo o Jax no cabeçalho) vêm do
**Data Dragon**, o CDN oficial que a Riot Games disponibiliza gratuitamente
para sites e ferramentas de fãs usarem os assets do jogo. O site busca a
versão de patch mais recente automaticamente ao carregar; nenhuma imagem é
armazenada no repositório.
