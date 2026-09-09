# Portfólio — Vicente Peyrot

Site estático (HTML + CSS puro, sem build) pronto para publicar no GitHub Pages.

## Estrutura

```
.
├── index.html        # conteúdo do site
├── styles.css        # estilos (dark mode, tema "console de dados")
├── assets/           # coloque aqui seu CV em PDF
│   └── CV_Vicente_Peyrot.pdf   (adicione este arquivo)
└── .nojekyll          # evita que o GitHub tente processar o site com Jekyll
```

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub. Duas opções de nome:
   - `seu-usuario.github.io` → o site fica em `https://seu-usuario.github.io/`
   - qualquer outro nome, ex. `portfolio` → o site fica em `https://seu-usuario.github.io/portfolio/`

2. Coloque estes arquivos na raiz do repositório (ou dentro de uma pasta `docs/`, se preferir — ajuste o passo 4 nesse caso).

3. Adicione seu currículo em PDF na pasta `assets/`, com o nome `CV_Vicente_Peyrot.pdf` (ou troque o link no `index.html`, na tag `<a class="nav-cta" href="assets/...">`).

4. No GitHub: **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**, escolha a branch `main` e a pasta `/ (root)` (ou `/docs`, se for o caso). Salve.

5. Em alguns minutos o site estará no ar no endereço indicado no passo 1.

### Via linha de comando (alternativa)

```bash
git init
git add .
git commit -m "Portfólio inicial"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPO.git
git push -u origin main
```

Depois, ative o GitHub Pages como no passo 4 acima.

## Editar conteúdo

- **Projetos**: seção `<section id="projetos">` no `index.html` — cada `<article class="project-card">` é um card.
- **Stack**: seção `<section id="stack">` — cada `.schema-table` é uma "tabela" de tecnologias.
- **Experiência**: seção `<section id="experiencia">` — cada `.timeline-item` é uma posição/curso.
- **Contato**: seção `<section id="contato">` — atualize e-mail, LinkedIn e GitHub se mudarem.
- **Cores**: no topo do `styles.css`, dentro de `:root`, estão as variáveis de cor (`--accent`, `--bg`, etc.) caso queira ajustar a paleta.

## Rodar localmente antes de publicar

Não precisa de instalação nenhuma — é HTML/CSS puro. Basta abrir o `index.html` direto no navegador, ou, para simular melhor o ambiente real:

```bash
python3 -m http.server 8000
```

E acessar `http://localhost:8000`.
