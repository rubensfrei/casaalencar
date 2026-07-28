# ✨ Casa Alencar — Site

Site institucional da **Casa Alencar** — espaço que reúne Salão, Barbearia, Maquiagem e Estética em Vitória da Conquista - BA.

*"Mais que um espaço de beleza: um lugar para pertencer."*

Pronto para hospedar de graça no **GitHub Pages**.
Feito em HTML + CSS + JS puro (sem build, sem npm, sem complicação).

---

## 📁 O que tem nesta pasta

```
casa-alencar-site/
├── index.html       ← a página inteira (texto, links, imagens)
├── styles.css       ← cores, fontes, layout, responsividade
├── script.js        ← menu mobile, animações
├── images/          ← (vazio — coloque aqui fotos suas, se quiser)
└── README.md        ← este arquivo
```

---

## 🚀 Como colocar no ar (passo a passo, sem conhecimento técnico)

### 1. Crie uma conta no GitHub
Acesse [github.com](https://github.com) e crie sua conta (é grátis).

### 2. Crie um repositório novo
1. Depois de logado, clique no **"+"** no canto superior direito → **"New repository"**.
2. **Nome do repositório**: `casa-alencar-site` (ou outro nome, sem espaços e sem acentos).
3. Marque como **Public** (público).
4. **NÃO marque** "Add a README file" — vamos subir os arquivos manualmente.
5. Clique em **"Create repository"**.

### 3. Suba os arquivos do site
Na página do repositório vazio, você verá a opção **"uploading an existing file"** (ou "add file" → "upload files").

1. **Arraste TODOS os arquivos** desta pasta (menos esta pasta em si) para a área de upload:
   - `index.html`
   - `styles.css`
   - `script.js`
   - (a pasta `images/` se tiver fotos)
2. Role pra baixo, escreva uma mensagem curta tipo "primeira versão do site".
3. Clique em **"Commit changes"**.

### 4. Ativar o GitHub Pages
1. No repositório, clique em **"Settings"** (engrenagem, no topo).
2. No menu lateral esquerdo, clique em **"Pages"**.
3. Em **"Branch"**, selecione `main` e deixe a pasta como `/ (root)`.
4. Clique em **"Save"**.
5. Espere 1-2 minutos. Seu site vai estar no ar em:

   ```
   https://SEU-USUARIO.github.io/casa-alencar-site/
   ```

   (troque `SEU-USUARIO` pelo seu nome de usuário do GitHub)

---

## ✏️ Como editar o conteúdo (sem mexer em código)

Tudo o que você precisa mudar está no arquivo **`index.html`**. Ele é texto puro — você edita igual a um documento do Word.

### 📌 Trocar o texto "Sobre"
Procure no `index.html` por:
```html
<!-- TROCAR ESTE TEXTO PELA SUA HISTÓRIA REAL -->
```
Apague o parágrafo de exemplo e escreva a história do seu negócio.

### 📌 Trocar horário de funcionamento
Procure por `<!-- TROCAR PELOS SEUS HORÁRIOS REAIS -->` e ajuste os dias/horas.

### 📌 Trocar WhatsApp
O número `557788064127` aparece em vários lugares. Se mudar, use Ctrl+H (Find & Replace) no editor e troque todos.

Formato do link: `https://wa.me/55` + DDD + número (sem espaços, sem traço).
Exemplo: `(77) 8806-4127` → `557788064127`

### 📌 Trocar Instagram
Procure por `suacasaalencar` e troque pelo seu @ (sem o @).

### 📌 Trocar endereço / mapa
Procure por `Caminho H, 29 - Urbis 1` e troque pelo seu endereço.
No link do Google Maps embed, troque também:
```
https://maps.google.com/maps?q=SEU+ENDERECO+AQUI&t=&z=15&ie=UTF8&iwloc=&output=embed
```
(Use `+` no lugar de espaços.)

### 📌 Trocar fotos da galeria
Tem **duas formas**:

**Forma 1 — Manual (mais simples):**
1. Coloque suas fotos na pasta `images/gallery/` (jpg ou png).
2. No `index.html`, troque o `src="https://images.unsplash.com/..."` por:
   ```html
   src="images/gallery/sua-foto.jpg"
   ```

**Forma 2 — Automática (feed do Instagram real):**
1. Crie uma conta grátis em [elfsight.com](https://elfsight.com/instagram-feed-instashow/) ou [snapwidget.com](https://snapwidget.com).
2. Configure com seu @ do Instagram.
3. Copie o código de embed (iframe).
4. No `index.html`, **substitua** toda a `<div class="gallery-grid">...</div>` pelo iframe do widget.

### 📌 Trocar cores
No `styles.css`, no começo do arquivo, tem:
```css
--c-primary: #a0413d;       /* terracotta */
--c-accent: #f1e3c5;        /* creme */
--c-dark: #2a1d1b;
```
Troque pelos códigos das cores que você quiser. Use [htmlcolorcodes.com](https://htmlcolorcodes.com) pra escolher.

---

## 🌐 Usar um domínio próprio (opcional, mais tarde)

Este site já vem com um arquivo `CNAME` configurado para `casaalencar.com.br`.
Se um dia quiser trocar de domínio (ou se estiver usando outro):

1. **Edite o arquivo `CNAME`** na raiz do projeto — coloque o domínio (apenas o domínio, sem `http://`, sem barra).
2. No painel onde comprou o domínio (HostGator, Registro.br, Namecheap…), configure o **DNS** com estes registros:

   | Tipo  | Nome | Valor                     |
   |-------|------|---------------------------|
   | A     | @    | 185.199.108.153           |
   | A     | @    | 185.199.109.153           |
   | A     | @    | 185.199.110.153           |
   | A     | @    | 185.199.111.153           |
   | CNAME | www  | SEU-USUARIO.github.io.    |

   (Troque `SEU-USUARIO` pelo seu nome de usuário do GitHub. **Não esqueça o ponto final** depois de `github.io`.)

3. Em **Settings → Pages → Custom domain** do seu repo no GitHub, confirme o domínio.
4. Ative **"Enforce HTTPS"** (GitHub gera o certificado grátis).
5. **Aguarde a propagação DNS** — pode levar de 30 minutos até 24h (principalmente em `.com.br`).

---

## 🆘 Problemas comuns

**O site não atualiza depois que eu mudei algo?**
- Espere 1-2 minutos e dê um Ctrl+Shift+R (recarregar ignorando cache).

**A imagem não aparece?**
- Confira se o nome do arquivo está EXATAMENTE igual (maiúsculas/minúsculas importam).
- Se a imagem está em `images/gallery/foto.jpg`, o caminho no HTML é `images/gallery/foto.jpg`.

**O mapa aparece em branco?**
- Verifique o endereço no link do Google Maps embed.
- Abra o link no navegador — se o mapa abrir lá, vai abrir no site.

---

Feito com 🏠 para a Casa Alencar.
Qualquer dúvida na hora de subir, é só chamar.
