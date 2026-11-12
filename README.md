# Pizza-Em-Casa-MB

Página de VSL do **Pizza em Casa** (HTML estático, sem build).

- Domínio: `postdiario.com.br`, o site precisa ficar na **raiz** do domínio.
- `img/` guarda a imagem abaixo do vídeo.
- `/` é a página da VSL (Vturb), `/termos` e `/privacidade` são as páginas legais.
- Empresa: MB Business LTDA — CNPJ 49.203.753/0001-93.
- E-mail de contato usado nas páginas: `contato@postdiario.com.br` (troque se for outro; está em `index.html`, `termos/` e `privacidade/`).
- Rastreamento mantido em todas as páginas: Meta Pixel, Utmify e Utmify Google Ads.
- Hospedagem em S3 + CloudFront: se `/termos` e `/privacidade` derem erro, aplique a CloudFront Function que acrescenta `index.html` em URLs de pasta.
