# Dolomitissime · Solovera

## 🚨 REGOLA FERREA: Mai perdere sottopagine

**Le sottopagine non devono MAI sparire.** Ogni nuova pagina creata va immediatamente aggiunta al repo e pushatata su `main`.

### Perché succede?
Il workflow GitHub Action deploya su Cloudflare Pages l'INTERO contenuto del repo. Se una pagina non è nel repo, non viene deployata e può essere persa.

### Regole
1. **Ogni nuova sottopagina** creata (es. `/reportannualecasevacanze/`, `/supergiulia/`) va messa in una cartella col suo `index.html`
2. **Commuttare SUBITO** dopo la creazione, prima di qualsiasi altro deploy
3. **Aggiungere il path** alla lista di verifica in `.github/workflows/deploy.yml`
4. **Mai deployare** con `wrangler pages deploy` singoli file — sempre l'intero repo

### Pagine attuali
- `/` → `index.html` (landing page)
- `/reportannualecasevacanze/` → `reportannualecasevacanze/index.html`

### Deploy
Automatico via GitHub Action su push a `main`. Il workflow verifica che tutte le pagine elencate siano presenti prima di deployare.
