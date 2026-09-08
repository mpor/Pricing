# IFIUR — Prezzario (v0.1 beta)

Web app installabile sul telefono per calcolare il prezzo di vendita a partire dal costo fornitore.

## Pubblicazione su GitHub Pages (prezzario.ifiur.it)

### 1. Crea il repository
Su github.com → **New repository** → nome a scelta (es. `prezzario`) → **Public** → crea.

### 2. Carica questi file
Trascina tutti i file di questa cartella (index.html, manifest.json, service-worker.js, CNAME, le icone) nella pagina del repository su GitHub, poi **Commit changes**.

Oppure da terminale, nella cartella estratta:
```bash
git init
git add .
git commit -m "Prima pubblicazione IFIUR Prezzario"
git branch -M main
git remote add origin https://github.com/TUO-USERNAME/NOME-REPO.git
git push -u origin main
```

### 3. Attiva GitHub Pages
Nel repository: **Settings → Pages**
- Source: `Deploy from a branch`
- Branch: `main`, cartella `/ (root)`
- Salva

### 4. Configura il dominio personalizzato
Sempre in **Settings → Pages**, nel campo **Custom domain** scrivi:
```
prezzario.ifiur.it
```
GitHub userà automaticamente il file `CNAME` già incluso in questa cartella.

### 5. Configura il DNS
Nel pannello DNS dove gestisci `ifiur.it`, aggiungi un record:

| Tipo  | Nome       | Valore                  |
|-------|------------|--------------------------|
| CNAME | prezzario  | TUO-USERNAME.github.io  |

(sostituisci TUO-USERNAME con il tuo nome utente GitHub)

### 6. Attendi e verifica
La propagazione DNS può richiedere da pochi minuti a qualche ora. Quando `prezzario.ifiur.it` è raggiungibile, torna su **Settings → Pages** e spunta **Enforce HTTPS** (necessario perché l'app sia installabile).

### 7. Condividi con lo staff
Manda il link `https://prezzario.ifiur.it` via WhatsApp. Su iPhone: Safari → Condividi → "Aggiungi a Home". Su Android: Chrome → menu ⋮ → "Installa app".

## Aggiornamenti futuri
Per aggiornare l'app (nuove categorie, prezzi, ecc.) basta modificare i file e rifare il push — GitHub Pages ripubblica automaticamente in 1-2 minuti, senza che lo staff debba reinstallare nulla.
