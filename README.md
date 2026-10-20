# Odonto Zoe — Site Institucional

Site one-page para a clínica odontológica **Odonto Zoe**, localizada em Mauá, SP.  
Desenvolvido por **TeoCode** · [teocode.com.br](https://teocode.com.br/)

---

## Estrutura de arquivos

```
OdontoZoe/
├── index.html                        # Site completo (single-page)
├── img/
│   ├── espaco-consultorio.png        # Foto do consultório
│   ├── espaco-corredor.png           # Foto do corredor com 4 salas
│   ├── espaco-fachada.png            # Foto da fachada
│   ├── espaco-recepcao.png           # Foto da sala de espera
│   ├── resultado-3-antes-depois.webp # Antes/depois — clareamento (Instagram)
│   └── resultado-4-antes-depois.png  # Antes/depois — tratamento estético
└── README.md
```

---

## Stack

| Tecnologia | Uso |
|---|---|
| HTML5 semântico | Estrutura única em `index.html` |
| Tailwind CSS (CDN) | Utilitários de layout e espaçamento |
| CSS customizado + variáveis | Design system, animações, curvas de easing |
| Vanilla JavaScript | Menu mobile, scroll-reveal, carrossel infinito |
| Google Fonts — Outfit | Tipografia (weights 300–800) |
| GoatCounter | Analytics sem cookie, sem LGPD |

Sem build step. Sem dependências de Node. Abre direto no navegador.

---

## Seções do site

| Seção | ID | Descrição |
|---|---|---|
| Hero | — | Headline, CTA principal, card de avaliação do Google |
| Serviços | `#servicos` | 6 especialidades com cards interativos |
| Avaliações | `#avaliacoes` | 5 avaliações reais do Google com link de verificação |
| Resultados | `#resultados` | 2 fotos antes/depois reais dos pacientes |
| Sobre | `#sobre` | Estatísticas da clínica + diferenciais |
| Conheça o Espaço | `#espaco` | Carrossel automático com 4 fotos da clínica |
| Localização | `#localizacao` | Endereço, horários, mapa, WhatsApp e redes sociais |

---

## WhatsApp

Todas as CTAs apontam para o mesmo número com mensagem contextual por seção:

```
Base: https://wa.me/5511970770718
```

Cada seção usa um `?text=` diferente para facilitar o atendimento na clínica.

---

## Analytics

Implementado com **GoatCounter** (sem cookie, sem aviso de LGPD):

```html
<script data-goatcounter="https://teocode.goatcounter.com/count"
        async src="//gc.zgo.at/count.js"></script>
```

Painel: [teocode.goatcounter.com](https://teocode.goatcounter.com)

---

## Deploy

### GitHub Pages (recomendado)

1. Crie um repositório público em `github.com/seu-usuario/odontozoe`
2. Suba os arquivos (`index.html` + pasta `img/`)
3. Vá em **Settings → Pages → Deploy from branch → main / root**
4. O site ficará em `https://seu-usuario.github.io/odontozoe`

Para domínio próprio (ex.: `odontozoe.com.br`), adicione um arquivo `CNAME` com o domínio e configure os registros DNS no painel do registrador.

### Netlify / Vercel

Arraste a pasta do projeto para [netlify.com/drop](https://app.netlify.com/drop) — deploy em segundos sem conta.

### Hospedagem tradicional (cPanel)

Faça upload dos arquivos para a pasta `public_html` via FTP. O `index.html` é a raiz do site.

---

## Personalização rápida

| O que mudar | Onde |
|---|---|
| Número do WhatsApp | Buscar `5511970770718` e substituir em todo o arquivo |
| Avaliações do Google | Seção `AVALIAÇÕES` no HTML (nome, texto, link) |
| Fotos do espaço | Substituir os arquivos em `img/espaco-*.png` |
| Fotos de resultados | Substituir `img/resultado-3-antes-depois.webp` e `img/resultado-4-antes-depois.png` |
| Endereço / horários | Seção `LOCALIZAÇÃO` no HTML |
| Link do Google Maps (iframe) | Buscar `maps.google.com/maps?q=` no HTML |

---

## SEO

O site já inclui:

- `<title>` e `<meta name="description">` otimizados para "dentista em Mauá SP"
- `<meta property="og:*">` para compartilhamento social
- `lang="pt-BR"` no `<html>`
- `rel="noopener noreferrer"` em todos os links externos
- `loading="lazy"` em todas as imagens abaixo da dobra
- Estrutura semântica com `<nav>`, `<section>`, `<footer>`, `<h1>`→`<h3>`

**Recomendado após o deploy:**

- Adicionar `<meta property="og:image">` com a URL de uma imagem da clínica
- Adicionar um `favicon.ico` (ou `<link rel="icon">` com SVG/PNG)
- Submeter a URL no [Google Search Console](https://search.google.com/search-console)

---

## Acessibilidade

- `aria-label` em todos os elementos interativos sem texto visível
- `aria-expanded` + `aria-controls` no botão de menu mobile
- `alt` descritivo em todas as imagens
- `:focus-visible` estilizado com a cor gold da marca
- `prefers-reduced-motion` respeitado nas animações de scroll-reveal
- `@media (hover: hover) and (pointer: fine)` nos efeitos de hover (sem disparo em touch)

---

## Créditos

Desenvolvido por **TeoCode** — [teocode.com.br](https://teocode.com.br/)  
© 2026 Odonto Zoe · Todos os direitos reservados
