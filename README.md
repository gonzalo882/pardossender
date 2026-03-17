# Pardos WA Sender

App de envio de mensagens WhatsApp via Z-API.

## Deploy no Railway

### 1. Cria conta
Vai a https://railway.app e cria conta (gratuito até 5$/mês de uso).

### 2. Instala o Railway CLI (opcional, mais rápido)
```bash
npm install -g @railway/cli
railway login
```

### 3. Deploy via GitHub (recomendado)

1. Cria repositório no GitHub e faz push desta pasta:
```bash
git init
git add .
git commit -m "init"
git remote add origin https://github.com/SEU_USER/pardos-sender.git
git push -u origin main
```

2. No Railway: **New Project → Deploy from GitHub repo** → seleciona o repositório

3. Railway deteta automaticamente Node.js e faz deploy.

4. Vai a **Settings → Networking → Generate Domain** para obteres o URL público.

### 4. Deploy direto via CLI (alternativa)
```bash
railway init
railway up
railway domain
```

## Acesso
- URL: o Railway gera automaticamente (ex: `pardos-sender.up.railway.app`)
- Password: `pardos2025`

## Alterar a password
Edita a linha no ficheiro `public/index.html`:
```javascript
const PASS = 'pardos2025';
```

## Estrutura
```
pardos-sender/
├── server.js          # Express server
├── package.json
├── railway.toml       # Config Railway
└── public/
    └── index.html     # App completa
```
