# agi-newprof â€” vÃ­deo do YouTube â†’ anÃ¡lise â†’ vÃ­deo completo + 3 reels

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo + os 5 vÃ­deos): **https://inematds.github.io/agi-newprof/guia/**

## O que Ã©

Pipeline local INEMA que transforma um vÃ­deo do YouTube em: anÃ¡lise do conteÃºdo, um vÃ­deo completo
narrado (16:9 e 9:16) e trÃªs reels 9:16, com imagens do **inemaimg** (flux2-klein), clipes-herÃ³i
image-to-video da **Agnes**, narraÃ§Ã£o **inemavox** (voz rachel) e render **HyperFrames**, entregues
no Telegram (@inemav3bot).

Primeiro caso: "GPT-6 Astra Doesn't Need Your Instructions Anymore" (Nate B. Jones, 2026-09-06).

## Estrutura

- `build.mjs` â€” gerador de composiÃ§Ã£o HyperFrames (`--video principal|reel1..3 [--vertical] [--out dir]`).
- `tools/` â€” `gen_img.py` (inemaimg), `agnes_clip.py` (Agnes), `narrar_vc.py` (inemavox), `escrever_txt.py`, `enviar.py` (Telegram).
- `scripts/roteiro.json` â€” fonte Ãºnica do texto (tela + fala) dos 4 vÃ­deos; `SCRIPT-*.md` gerados.
- `scripts/render.sh` â€” espera a narraÃ§Ã£o, faz lint e renderiza em alta.
- `guia/` â€” pÃ¡gina landing+guia (GitHub Pages) com os vÃ­deos em versÃ£o web.
- `capa/capa.png` â€” capa oficial do catÃ¡logo.
- `FALHAS.md` â€” registro de falhas (uma linha por falha).

Os assets pesados (imagens, WAVs, masters em alta) vivem em `~/projetos/output/agi-newprof/`.

---

Projeto adaptado da comunidade INEMA TDS - Marca Arckhe