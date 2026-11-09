# Design system — ecommercedozero

## Propósito e posicionamento

Landing page de consultoria para estruturação, integração e implantação de ecossistemas de ecommerce e marketplaces. A interface explica uma sequência de trabalho — diagnóstico, arquitetura, integrações, operação e continuidade — sem prometer resultados numéricos não comprovados. O tom é técnico, claro, consultivo e orientado a decisões práticas.

## Identidade visual

- **Marca:** `ecommercedozero`, escrita em minúsculas e sem espaços.
- **Personalidade:** competente, acessível, organizada, pragmática e tecnológica sem parecer uma ferramenta corporativa fria.
- **Princípio visual:** páginas predominantemente claras, com verde vivo para ação e verde-floresta para áreas de foco; diagramas substituem fotografia genérica de galpões ou produtos.
- **Composição:** grade editorial ampla, respiro generoso, mapas de sistemas, etapas de processo e listagens de entregáveis.

## Cores

| Token | Valor | Uso |
|---|---|---|
| `--color-ink` | `#172720` | Texto principal |
| `--color-forest` | `#16392f` | Faixas e cabeçalhos escuros |
| `--color-forest-strong` | `#17392f` | Nós centrais de integração e CTA de contraste |
| `--color-green` | `#c5fa63` | Ação primária e destaque |
| `--color-green-soft` | `#eff8e8` | Realce de fundo |
| `--color-page` | `#f4f6f2` | Fundo geral |
| `--color-surface` | `#ffffff` | Superfícies e cartões |
| `--color-muted` | `#66736c` | Texto secundário |
| `--color-border` | `#e2e9e2` | Divisores e contornos |

Use o verde-lima com parcimônia: CTA, estado ativo, pequenos marcadores e chamadas de atenção. Garanta contraste de texto suficiente sobre o verde.

## Tipografia

- **Manrope:** títulos e manchetes (peso 700–800), com tracking levemente negativo.
- **DM Sans:** texto corrido, navegação e botões.
- **DM Mono:** rótulos técnicos, etapas, códigos, metadados e diagramas.
- **Space Grotesk:** acentos de interface quando necessário.
- Carregamento atual por Google Fonts; as famílias genéricas de fallback permanecem nos estilos.

## Layout e espaçamento

- Contêiner de conteúdo máximo: `1440px`, centralizado.
- Hero: composição 2 colunas (texto + mapa), empilhada em telas menores.
- Seções desktop: espaçamento vertical típico de `74px`; mobile: `52px`.
- Bordas arredondadas: controles `6px`, cartões `8px`, painéis `14px`.
- Breakpoint principal de layout responsivo: `800px`. Navegação mobile mantém os links em faixa horizontal com rolagem.
- Elementos de interação devem ter área clicável confortável e estados de foco/hover perceptíveis.

## Componentes da página

1. **Faixa superior:** posicionamento e categoria do serviço.
2. **Navegação:** links internos para Ecossistema, Escopo, Método e Entregáveis; CTAs externos para contratação e WhatsApp.
3. **Hero:** promessa principal, resumo de escopo, CTA e mapa de sistemas.
4. **Mapa de ecossistema:** loja/canais, camada de integração e sistemas de gestão/operação. É ilustrativo; adaptar ao cenário real.
5. **Barra de ferramentas:** exemplos de plataformas e categorias, não endosso nem garantia de integração.
6. **Problemas:** quatro sintomas operacionais apresentados em lista numerada.
7. **Fluxo de dados:** origem de produto → orquestração → canais → operação → gestão.
8. **Escopo da consultoria:** cinco frentes, com descrições diretas.
9. **Método:** diagnóstico → arquitetura → plano de integração → implantação → operação assistida.
10. **Entregáveis:** artefatos concretos, com diagrama ilustrativo.
11. **Formatos de apoio:** diagnóstico, blueprint e implantação assistida, sujeitos à definição comercial.
12. **FAQ e CTA final:** reduzir dúvidas e guiar para o próximo passo.
13. **WhatsApp flutuante:** atalho persistente para contato.

## Iconografia

A interface atual usa micro-rótulos tipográficos (`WEB`, `ERP`, `SKU`, `OPS`), caracteres de fluxo e símbolos simples em vez de uma dependência de pacote de ícones. A pasta `assets/icons/` inclui uma família complementar de SVGs de traço fino: ecommerce, marketplace, catálogo, integração, ERP, operação, serviços, WhatsApp e seta. `icons-preview.html` permite inspecioná-los. Ícones devem permanecer monocromáticos, com `currentColor`, traço `1.7` e proporção `24×24`.

## Conteúdo e conversão

- CTAs de contratação levam ao endereço externo definido pelo proprietário da página; não exibir o nome do processador de pagamento no texto público.
- WhatsApp: `(51) 98122-0279`; link usa formato internacional com código do Brasil.
- Não criar números, depoimentos, cases, parcerias ou compatibilidades sem validação.
- Ferramentas citadas são exemplos. Confirmar conectores e escopo de integração caso a caso.
- Usar rótulos objetivos: “Contratar consultoria”, “Falar pelo WhatsApp”, “O que estruturamos”.

## Arquivos incluídos

- `index.html`: página final funcional e responsiva.
- `styles.css`: estilos completos extraídos da implementação.
- `design-tokens.css`: tokens de referência para manutenção e evolução.
- `assets/icons/*.svg`: biblioteca vetorial.
- `icons-preview.html`: galeria visual local dos ícones.
- `preview.png`: captura da página no desktop.

## Manutenção

Editar conteúdo e links em `index.html`; alterar layout em `styles.css`; atualizar as decisões de marca em `design-tokens.css` e neste documento. Testar navegação, CTAs, WhatsApp e os breakpoints desktop/mobile antes da publicação.

## Símbolo da marca e favicon

O símbolo traduz o conceito de ecommerce do zero conectado a um ecossistema: um nó central (plataforma/orquestração) ligado a três pontos (loja, canais e operação). A composição mantém o verde-floresta `#17392F` e o verde-lima `#C5FA63`, sem lettering, para funcionar em tamanhos pequenos. A versão de favicon usa um tile verde-floresta arredondado e o núcleo em verde-lima para contraste na aba do navegador.

- `assets/brand/brand-mark.svg`: vetor transparente para aplicação em fundos claros e peças de marca.
- `assets/brand/brand-mark-1024.png`: exportação PNG transparente de alta resolução.
- `assets/brand/favicon.svg`: versão vetorial com fundo tile para navegadores.
- `assets/brand/favicon.ico`: favicon multirresolução para compatibilidade.
- `assets/brand/favicon-16.png`, `favicon-32.png`, `favicon-48.png`: tamanhos de navegador.
- `assets/brand/apple-touch-icon.png` (180×180) e `favicon-192.png` / `favicon-512.png`: ícones para atalhos e dispositivos.

Use `brand-mark.svg` quando o fundo permitir transparência. Use `favicon.svg`/`.ico` para abas, atalhos e contextos pequenos. Não estique o símbolo; preserve o espaço interno e o contraste. O favicon já está vinculado no `index.html`.
