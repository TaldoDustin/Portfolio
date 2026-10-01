# Portfólio Souza Tech

Landing page do portfólio, com a logo animada em HTML/CSS (os dois cursores piscam alternados, um para cada irmão).

## Estrutura

```
index.html        → página (HTML + CSS, sem dependências)
favicon.svg       → ícone da aba
assets/           → kit de logo em SVG (redes sociais, documentos etc.)
```

## Rodar localmente

Basta abrir o `index.html` no navegador. Ou, com um servidor simples:

```bash
npx serve .
# ou
python3 -m http.server 8000
```

## Publicar no GitHub

```bash
git init
git add .
git commit -m "Primeira versão do portfólio"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
git push -u origin main
```

Para colocar no ar de graça: no repositório, vá em **Settings → Pages**, escolha a branch `main` e a pasta `/ (root)`.

## Logo animada

O tamanho da logo é controlado só pelo `font-size` do elemento `.logo`:

```html
<a href="/" class="logo" style="font-size: 24px">
  <span>souza</span><span class="logo__tech">.tech</span>
  <span class="logo__cursors" aria-hidden="true">
    <span class="logo__cursor"></span><span class="logo__cursor"></span>
  </span>
</a>
```

Quem configurou o sistema para reduzir animações vê os cursores parados (`prefers-reduced-motion`).
