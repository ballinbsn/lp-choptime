# lp-choptime — site de páginas do FutChopp (teste A/B)

Site estático (HTML/JS/CSS/imagens) servido pela Vercel. Não tem servidor próprio: o checkout chama a API (`api-choptime`) no endereço
configurado em `config.js`.

## Vercel (o que fazer)
1. Projeto novo → importar o repositório `lp-choptime`. Framework: **Other**; sem comando de build; pasta de saída: raiz (`.`).
2. Domínio: `futchop.shop` (e `www.futchop.shop`).
3. Edite **`config.js`** (na raiz do repositório) com os valores deste teste:
   - `apiBase`: endereço da API no Railway, **sem barra no final** (ex.: `https://api-choptime-production.up.railway.app`);
   - `utmifyPixelId`: ID do pixel da UTMify deste teste (texto entre aspas);
   - `metaPixelId`: deixe `""` (Meta desligada);
   - `cardEnabled`: `false`.

Páginas: `/produto/futchopp` (a raiz `/` leva para ela, mantendo UTMs), `/checkout`, `/pagamento-pix`, `/politicas`, `/rastreio`.

Este repositório é gerado pelo projeto-mãe (`npm run build:public && npm run build:static && node tools/export-repos.mjs`). Não edite os JS à mão.
