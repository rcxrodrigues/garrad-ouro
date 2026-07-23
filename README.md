# Método Garra de Ouro — Landing page do curso

Landing page estática (HTML/CSS/JS puros, sem build, sem dependências) para vender
o curso "Método Garra de Ouro" — como identificar a mecânica das máquinas de
ursinho pelo som e pegar 6, 10 ou mais numa jogada só.

## Estrutura

```
index.html   página inteira (estilos e scripts embutidos no próprio arquivo)
```

## Antes de publicar

- [ ] Trocar os botões "Quero o plano Básico" e "Quero o plano Premium" (seção
      `#oferta`, hoje apontam para `#`) pelos links reais de cada checkout
      (Hotmart, Kiwify, Eduzz, Stripe Payment Link, etc.) — um link por plano.
- [ ] Trocar o `.brand-mark` (emoji 🧸 no header e no rodapé) pela sua logo
      real assim que estiver pronta, ex: `<img src="logo.png" alt="Garra
      D'Ouro">` no lugar do `<span class="brand-mark">`.
- [ ] Substituir o vídeo principal do hero (`.phone-frame`, logo abaixo da
      headline) e os 3 vídeos da seção "Veja o método na prática"
      (`.video-card`) pelos vídeos reais do expert — troque o `div
      .placeholder-txt` por um `<video controls src="...">` ou um `<iframe>`
      de YouTube/Instagram/TikTok, mantendo a proporção 9:16.
- [ ] Substituir os prints de WhatsApp (`.wa-mock`, mockups em CSS) e os
      vídeos de depoimento (`.proof-video`) do carrossel de prova social por
      capturas e vídeos reais de alunos — todos já estão nas dimensões
      verticais 9:16.
- [ ] Conferir preço, nome do produto e link/e-mail de suporte.
- [ ] Revisar o texto do FAQ sobre legalidade/ética conforme a linha de
      comunicação que você quer usar.

## Rodar localmente

Não precisa de servidor nem instalação — é só abrir o `index.html` no navegador.
Se preferir servir localmente:

```bash
python -m http.server 8080
# depois abra http://localhost:8080
```

## Publicar no GitHub

```bash
# dentro desta pasta (lp_ursinhos)
git init
git add .
git commit -m "Landing page do curso Metodo Garra de Ouro"

# crie um repositório vazio em https://github.com/new (sem README/gitignore)
# depois conecte e envie:
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPO.git
git branch -M main
git push -u origin main
```

## Publicar na Vercel

**Opção 1 — pelo site (recomendado, sem instalar nada):**
1. Acesse https://vercel.com/new
2. Clique em "Import" no repositório do GitHub que você acabou de criar
3. Framework Preset: "Other" (a Vercel detecta HTML estático automaticamente)
4. Clique em "Deploy" — pronto, sem configuração adicional necessária

**Opção 2 — pela CLI:**
```bash
npm install -g vercel
vercel        # segue o assistente, gera uma URL de preview
vercel --prod # publica em produção
```

## Domínio próprio

Depois do deploy, em **Vercel → seu projeto → Settings → Domains**, adicione seu
domínio e siga as instruções de DNS mostradas na tela.
