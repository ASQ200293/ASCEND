# Questionário Web — Instituto ASCEND

## O que contém

- `index.html`: página completa do questionário.
- `assets/logo-ascend.svg`: logo provisória/editável.
- `_headers`: cabeçalhos simples para Cloudflare Pages.
- `vercel.json`: configuração mínima para Vercel.

## Como usar localmente

Abra o arquivo `index.html` no navegador.

As respostas:
- ficam salvas no navegador da pessoa;
- podem ser baixadas em JSON;
- podem ser baixadas em CSV;
- podem ser impressas/salvas em PDF.

## Como trocar a logo

Opção 1:
- Substitua o arquivo `assets/logo-ascend.svg` pela logo real mantendo o mesmo nome.

Opção 2:
- Coloque a logo em `assets/logo-ascend.png`.
- No `index.html`, procure por:

```html
<img src="./assets/logo-ascend.svg" alt="Logo Instituto ASCEND">
```

- Troque para:

```html
<img src="./assets/logo-ascend.png" alt="Logo Instituto ASCEND">
```

Recomendação:
- Use PNG com fundo transparente ou SVG.
- Tamanho sugerido: 800x800px ou SVG vetorial.

## Como alterar a paleta

No topo do `index.html`, procure por:

```css
:root {
  --ascend-blue-dark: #173E59;
  --ascend-blue: #2E6F88;
  --ascend-green: #8FBF9F;
  --ascend-sand: #F4EFE7;
  --ascend-gold: #C99A4A;
}
```

Altere os códigos das cores.

## Como publicar na Vercel

### Caminho simples pelo GitHub

1. Crie um repositório no GitHub.
2. Envie estes arquivos para o repositório.
3. Acesse a Vercel.
4. Clique em Add New Project.
5. Importe o repositório.
6. Framework Preset: Other.
7. Build Command: deixe vazio.
8. Output Directory: deixe vazio ou coloque `.`.
9. Deploy.

## Como publicar na Cloudflare Pages

1. Crie um repositório no GitHub.
2. Envie estes arquivos para o repositório.
3. Acesse Cloudflare.
4. Vá em Workers & Pages.
5. Create application.
6. Pages.
7. Connect to Git.
8. Escolha o repositório.
9. Framework preset: None.
10. Build command: deixe vazio.
11. Build output directory: deixe vazio ou coloque `/`.
12. Deploy.

## Observação importante

Esta versão não envia as respostas automaticamente para um banco de dados.

Fluxo recomendado nesta fase:
1. Renata responde.
2. Clica em "Baixar JSON".
3. Envia o arquivo JSON para você.
4. Você joga o JSON no ChatGPT para consolidar, extrair decisões, riscos, plano de ação e próximos passos.

Quando o projeto avançar, a evolução ideal é:
- Next.js + Supabase, se quiser login, banco de dados, dashboard e histórico;
- Tally/Typeform, se quiser validar rápido sem programar;
- Google Forms, se quiser algo simples e menos premium.
