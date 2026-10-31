# Site da Dra. Aline Lima

Site estático, sem build: `index.html` (com CSS e JS no próprio arquivo), `privacidade.html`, `favicon.svg` e a pasta `assets/`.
Para ver localmente, abra o `index.html` no navegador.

**Estado: prévia.** A página tem `noindex` e marcadores tracejados "a confirmar" visíveis. Não publique como versão final
antes de a doutora revisar textos, dados e imagens.

## A confirmar com a doutora

- [ ] **CRO-MG 57211**: número lido na logo circular das capas do Instagram. Confirmar antes de publicar (Sobre e rodapé).
- [ ] Graduação: instituição e ano.
- [ ] Pós-graduação em Implantodontia: instituição e situação. O site diz "em andamento" e não a chama de especialista.
- [ ] Tratamentos oferecidos hoje: facetas em resina, reabilitação oral, próteses, implantes, gengivoplastia e cirurgias. Os implantes aparecem nos posts, mas não estão nos destaques.
- [ ] Revisão dos textos clínicos de cada tratamento pela Dra. Aline.
- [ ] As etapas do atendimento (primeiro contato, avaliação, planejamento, acompanhamento) batem com o que ela faz na prática?
- [ ] Endereço (Rua Belo Horizonte, 988, Centro) e CEP. O mapa no story mostra 37940-000.
- [ ] Horários, formas de pagamento, convênios, acessibilidade e estacionamento.
- [ ] Duração e valor da avaliação (FAQ).
- [ ] WhatsApp: o link da bio (`wa.me/message/YPS3UDOS6PXJN1`) é um link de mensagem e não aceita texto pronto. Se ela preferir, troque pelo número no formato `wa.me/55DDDNUMERO?text=...`.
- [ ] Uso da frase do Instagram citada na seção Sobre.
- [ ] Autorização para usar os dois retratos e arquivos originais em alta resolução. Hoje eles vêm da grade do Instagram:
  - `aline-retrato-*.webp`: retrato de blazer preto em fundo cinza (1080 px).
  - `aline-sobre-*.webp`: retrato na poltrona (1216×2160).
- [ ] Fotos reais do consultório. A seção `#consultorio` está pronta para recebê-las e hoje mostra só texto.
- [ ] Logo oficial em SVG (ou PNG transparente). A assinatura "Dra. Aline *Lima*" é **provisória**. O monograma circular com o dente e o "A" não foi recriado.
- [ ] Cores e fontes oficiais. As cores atuais foram estimadas a partir dos posts.
- [ ] Domínio definitivo (as metatags apontam para `paparidisbrancher.github.io/dra-aline-lima/`).

Ficaram fora de propósito: fotos de pacientes, antes e depois e depoimentos. Só entram com autorização por escrito e dentro das regras do CFO.

## Como trocar

| O quê | Onde |
|---|---|
| WhatsApp | Buscar e substituir `https://wa.me/message/YPS3UDOS6PXJN1` em `index.html` e `privacidade.html`. |
| Marcador "a confirmar" | Elementos `<span class="pendente">`. Ao confirmar o dado, escreva o valor no lugar e apague o span. |
| CRO, formação | `index.html`, bloco `<dl class="dados">` da seção `#sobre`, e o rodapé. |
| Tratamentos | `index.html`, `<ul class="lista">`. Cada item é um `<li>` com `<h3>` e `<p>`. |
| Endereço, horários, pagamento | Seção `#consultorio` (`<dl class="info">`), perguntas do FAQ e rodapé. Com o endereço confirmado, acrescente `streetAddress` e `postalCode` ao JSON-LD do `<head>`. |
| Retratos | `assets/aline-retrato-640/1080.webp` (quadrados) e `assets/aline-sobre-600/900.webp` (9:16). Mantendo nome e proporção, nada mais muda. Mudando a proporção, ajuste `width`/`height` da `<img>`. |
| Imagem de compartilhamento | `assets/og-aline.jpg` (1200×630). |
| Cores e fontes | Variáveis do `:root`, no início do `<style>`. Fontes: Instrument Serif (títulos) e Hanken Grotesk (texto), ambas do Google Fonts, licença OFL. |
| Logo | Trocar o `<a class="marca">` do cabeçalho, do menu e do rodapé por uma `<img>`. |

## Ao publicar a versão final

1. Remover `<meta name="robots" content="noindex, nofollow">` do `index.html` e do `privacidade.html`.
2. Atualizar `og:url`, `og:image` e o JSON-LD com o domínio definitivo.
3. Testar os links de WhatsApp no celular.
