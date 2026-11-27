# 🧬 Receita para recriar: Navegador SK

_Gerada sem IA, lendo 15 arquivo(s). Serve para remontar este app como HTML modular — com qualquer IA, um arquivo por vez._

## 1. O que é

- **Nome:** Navegador SK
- **Partes de código:** 9 (1 tela, 7 logica, 0 servidor, 0 dados, 1 estilo)
- **Tem servidor (rotas /api):** não — dá para ser só HTML
- **Peças de fora (bibliotecas):** nenhuma

## 2. Estrutura modular proposta

```
index.html            ← a página; chama os módulos NA ORDEM
css/app.css           ← o visual
js/00-core.js         ← a "locomotiva": cria window.APP (registrar, guardar, avisar)
js/10-base.js         ← Navegador SK — 00-base.js: peças comuns (era js/00-base.js)
js/15-busca.js        ← Navegador SK — 10-busca.js: busca o site. No APK: direto (o Android nã (era js/10-busca.js)
js/20-traducao.js     ← Navegador SK — 20-traducao.js: traduz para o português, de graça (trad (era js/20-traducao.js)
js/25-leitura.js      ← Navegador SK — 30-leitura.js: tira só o texto principal da página (mod (era js/30-leitura.js)
js/30-pagina.js       ← Navegador SK — 40-pagina.js: mostra o site aqui dentro (🌐 Página) ou  (era js/40-pagina.js)
js/35-guardar.js      ← Navegador SK — 50-guardar.js: favoritos, histórico, páginas guardadas  (era js/50-guardar.js)
js/40-inicio.js       ← Navegador SK — 90-inicio.js: liga os botões e reabre a última página ( (era js/90-inicio.js)
js/45-inicio.js       ← Navegador SK (era index.html)
js/99-app.js          ← o último: monta a tela com o que embarcou
```

## 3. As partes, uma por uma

| # | Era | Vira | Tipo | O que faz | Usa |
|---|---|---|---|---|---|
| 1 | `js/00-base.js` | `js/10-base.js` | logica | Navegador SK — 00-base.js: peças comuns | — |
| 2 | `js/10-busca.js` | `js/15-busca.js` | logica | Navegador SK — 10-busca.js: busca o site. No APK: direto (o Android não tem o bloqueio do  | — |
| 3 | `js/20-traducao.js` | `js/20-traducao.js` | logica | Navegador SK — 20-traducao.js: traduz para o português, de graça (tradutor do Google), man | — |
| 4 | `js/30-leitura.js` | `js/25-leitura.js` | logica | Navegador SK — 30-leitura.js: tira só o texto principal da página (modo leitura) | — |
| 5 | `js/40-pagina.js` | `js/30-pagina.js` | logica | Navegador SK — 40-pagina.js: mostra o site aqui dentro (🌐 Página) ou só o texto (📖 Leitu | — |
| 6 | `js/50-guardar.js` | `js/35-guardar.js` | logica | Navegador SK — 50-guardar.js: favoritos, histórico, páginas guardadas e o menu ⋮ | — |
| 7 | `js/90-inicio.js` | `js/40-inicio.js` | logica | Navegador SK — 90-inicio.js: liga os botões e reabre a última página (sem sumir nada) | — |
| 8 | `css/estilo.css` | css/app.css | estilo | — | — |
| 9 | `index.html` | `js/45-inicio.js` | tela | Navegador SK | manifest.json, icone.svg, estilo.css, 00-base.js |

## 4. Montar passo a passo (cada bloco é um pedido pronto: 📋 Copiar → colar na IA)

### Passo 0 — combinar as regras com a IA

```text
Vamos recriar o app "Navegador SK" como HTML MODULAR, que abre pelo index.html, sem servidor e sem nada da Replit.
Regras: (1) index.html chama os arquivos js/ na ordem, antes do </body>; (2) js/00-core.js cria window.APP com APP.registrar(modulo), APP.guardar(chave, valor) em IndexedDB/localStorage e APP.avisar(texto); (3) cada arquivo js/NN-nome.js cuida de UM assunto, começa com (function (APP) { e termina com })(window.APP); (4) js/99-app.js vem por último e monta a tela com os módulos registrados; (5) textos em português do Brasil.
Vou pedir UM arquivo por vez. Responda só com o arquivo completo, sem cortar nada. Primeiro: crie index.html, css/app.css e js/00-core.js.
```

### Passo 1 — `js/10-base.js` (era `js/00-base.js`, 39 linhas)

```text
Crie js/10-base.js. Ele faz: Navegador SK — 00-base.js: peças comuns.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 2 — `js/15-busca.js` (era `js/10-busca.js`, 69 linhas)

```text
Crie js/15-busca.js. Ele faz: Navegador SK — 10-busca.js: busca o site. No APK: direto (o Android não tem o bloqueio do navegador). No navegador: tenta direto e depois a CASCATA de proxies grátis (a mesma do extrator do Gemini, que funciona): AllOrigins → corsproxy.io → CodeTabs → AllOrigins (cru). Último recurso: leitor r.jina.ai (só o texto).
No app original ele tinha estas funções/partes: comTempo, pareceHtml, lerTexto.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 3 — `js/20-traducao.js` (era `js/20-traducao.js`, 47 linhas)

```text
Crie js/20-traducao.js. Ele faz: Navegador SK — 20-traducao.js: traduz para o português, de graça (tradutor do Google), mantendo a página.
No app original ele tinha estas funções/partes: tradTexto.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 4 — `js/25-leitura.js` (era `js/30-leitura.js`, 35 linhas)

```text
Crie js/25-leitura.js. Ele faz: Navegador SK — 30-leitura.js: tira só o texto principal da página (modo leitura).
No app original ele tinha estas funções/partes: limpa.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 5 — `js/30-pagina.js` (era `js/40-pagina.js`, 120 linhas)

```text
Crie js/30-pagina.js. Ele faz: Navegador SK — 40-pagina.js: mostra o site aqui dentro (🌐 Página) ou só o texto (📖 Leitura), com tradução.
No app original ele tinha estas funções/partes: modo, traduzir, linkReal, montarPagina, montarLeitura, mostrar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 6 — `js/35-guardar.js` (era `js/50-guardar.js`, 78 linhas)

```text
Crie js/35-guardar.js. Ele faz: Navegador SK — 50-guardar.js: favoritos, histórico, páginas guardadas e o menu ⋮.
No app original ele tinha estas funções/partes: favs, pintarFavs, textoAtual, titulo, precisa.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 7 — `js/40-inicio.js` (era `js/90-inicio.js`, 22 linhas)

```text
Crie js/40-inicio.js. Ele faz: Navegador SK — 90-inicio.js: liga os botões e reabre a última página (sem sumir nada).
No app original ele tinha estas funções/partes: pintarModo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 8 — `js/45-inicio.js` (era `index.html`, 70 linhas)

```text
Crie js/45-inicio.js. Ele faz: Navegador SK.
Ele usa o que já foi criado em: js/10-base.js, js/15-busca.js, js/20-traducao.js, js/25-leitura.js, js/30-pagina.js, js/35-guardar.js, js/40-inicio.js (pelo APP).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 9 — `js/99-app.js` e conferir

```text
Crie js/99-app.js: ele olha APP.modulos e monta o menu/abas com um botão para cada módulo. Depois, me mande o index.html atualizado com todos os <script src="js/…"> na ordem certa: js/00-core.js, js/10-base.js, js/15-busca.js, js/20-traducao.js, js/25-leitura.js, js/30-pagina.js, js/35-guardar.js, js/40-inicio.js, js/45-inicio.js, js/99-app.js.
```

## 5. Conferir no final

- [ ] Abrir o index.html na prévia: aparece a tela sem erro (▤ console vazio)?
- [ ] Cada botão abre a sua parte?
- [ ] Fechar e abrir de novo: os dados continuam?
- [ ] Nada com "replit", "REPL_", "@workspace" no código (🏗️ Preparar confere).
- [ ] 📱 PWA → deixar instalável; 📦 APK ou 🖥️ .exe.
