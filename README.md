# ecommercedozero — landing page

Página de vendas da consultoria **ecommercedozero**. É um site estático (HTML + CSS), sem build e sem banco de dados, publicado na Vercel.

## Estrutura

```
index.html          Conteúdo da página, links de CTA e WhatsApp, metatags de SEO
styles.css          Estilos (tokens de design no :root, breakpoints 1100px / 800px)
assets/brand/       Símbolo da marca e favicons
assets/icons/       Biblioteca de ícones SVG (traço 1.7, currentColor)
assets/og-image.png Imagem de compartilhamento (1200×630)
site.webmanifest    Ícones para dispositivos
robots.txt, sitemap.xml
vercel.json         Cache e headers de segurança
docs/               Design system original (DESIGN-SYSTEM.md, preview, zip do pacote)
```

## Rodar localmente

```bash
npx serve .
# abra http://localhost:3000
```

## Editar

- **Textos e seções:** `index.html`. Cada seção está comentada (`<!-- 01 PROBLEMAS -->` etc.).
- **Link de contratação:** procure `data-link="checkout"` (3 ocorrências) e troque o `href`.
- **WhatsApp:** procure `data-link="whatsapp"` (4 ocorrências).
- **Cores, fontes e espaçamentos:** variáveis no topo de `styles.css`.
- Regras de marca e de conteúdo: [docs/DESIGN-SYSTEM.md](docs/DESIGN-SYSTEM.md). Por exemplo, não citar o processador de pagamento no texto e não publicar números, cases ou parcerias sem validação.

## Deploy na Vercel

**Opção A: pelo GitHub (recomendado)**
1. Suba este repositório para o GitHub.
2. Na Vercel: *Add New → Project → Import* o repositório.
3. Framework Preset: **Other**. Deixe Build Command vazio e Output Directory como `.` (raiz).
4. Clique em Deploy. Cada `git push` na `main` publica automaticamente, e outras branches geram URLs de preview.

**Opção B: pela CLI**
```bash
npx vercel        # primeiro deploy / preview
npx vercel --prod # produção
```

## Domínio próprio

Depois de configurar o domínio em *Project → Settings → Domains*, troque `https://ecommercedozero.vercel.app` pelo domínio final em:
- `index.html` (canonical, `og:url`, `og:image`)
- `robots.txt`
- `sitemap.xml`

## Checklist antes de publicar

- [ ] Desktop (1440px) e mobile (375px) sem quebra de layout
- [ ] Links do menu rolam até as seções
- [ ] Os 3 CTAs abrem o checkout em nova aba
- [ ] Os 4 links de WhatsApp abrem com a mensagem pré-preenchida
- [ ] FAQ abre e fecha
- [ ] Favicon aparece e a prévia de compartilhamento (WhatsApp/LinkedIn) mostra a imagem
