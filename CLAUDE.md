# arsha1

Sito Jekyll (tema Arsha, clone di MLH-Fellowship/jekyll-theme-arsha) su GitHub Pages: https://cialdecompatibili-netizen.github.io/arsha1/

## Cose che funzionano
- Clone del tema in una repo propria: `gh repo create OWNER/NOME --public`, `git clone` del tema, `git remote rename origin upstream`, `git remote add origin` sulla nuova repo, `git push -u origin main`. Poi in `_config.yml` impostare `url` (https://OWNER.github.io) e `baseurl` (/NOME).
- Attivare Pages da PowerShell con gh gia' loggato: scrivere il JSON `{\"source\":{\"branch\":\"main\",\"path\":\"/\"}}` in un file temporaneo e lanciare `gh api -X POST repos/OWNER/NOME/pages --input FILE`. Passare il JSON da stdin con `--input -` fallisce in PowerShell.
- Verifica dopo il deploy: controllare lo stato con `gh api repos/OWNER/NOME/pages/builds/latest` e scaricare home e asset cercando href/src che non iniziano col baseurl.
