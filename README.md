# T10-Google-MB-Business-v2

Site estático (HTML, CSS e JavaScript puros) de **postdiarios.com.br**. Não precisa de build nem de instalação: basta publicar os arquivos como estão.

## Estrutura

| Endereço | Pasta | O que é |
|---|---|---|
| `/` | `index.html` | Página principal = página de vendas com VSL (preço e botões liberados no pitch). É uma cópia de `front/` |
| `/front/` | `front/` | Mesma página de vendas, mantida no endereço antigo |
| `/297/` | `297/` | Upsell Pacote Completo (VSL + widget Hotmart no pitch) |
| `/197/` | `197/` | Oferta 197 (se recusar a 297) |
| `/97/` | `97/` | Oferta 97 (se recusar a 197) |
| `/obrigado/` | `obrigado/` | Página de obrigado (grupo de WhatsApp) |
| `/termos/` | `termos/` | Termos de uso |
| `/privacidade/` | `privacidade/` | Política de privacidade |
| — | `img/`, `video/` | Imagens e vídeo usados nas páginas (caminhos a partir da raiz, ex.: `/img/logo.webp`) |

## Rastreamento
- Pixel da Meta (ID 207279252446547)
- Utmify (UTMs) e pixel do Google da Utmify (ID da versão 2, otimizado para Google Ads)

## Publicação
Cada pasta tem um `index.html`, então o site precisa ser servido a partir da **raiz do repositório** (sem pasta por fora).
- **Cloudflare Pages / Netlify / Vercel:** conecte o repositório, deixe o comando de build vazio e o diretório de saída como `/` (raiz).
- **AWS (S3 + CloudFront):** envie o conteúdo para a raiz do bucket e, para as subpastas abrirem, associe uma CloudFront Function que complete endereços terminados em `/` com `index.html`.

Observação: as páginas apontam para as imagens a partir da raiz do domínio, então o site deve ficar na raiz (ex.: `https://postdiarios.com.br/`), não numa subpasta.
