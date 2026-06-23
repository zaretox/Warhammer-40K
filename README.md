# Codex Chromatica

Application web (un seul fichier `index.html`, sans build) répertoriant les schémas de
peinture des armées de **Warhammer 40 000** : pour chaque schéma, la séquence étape par
étape, la peinture **Citadel** et son équivalent **Army Painter**, et **où l'appliquer**
sur la figurine. Inclut une liste de courses imprimable. Optimisée mobile (iOS / Android).

## Mettre en ligne avec Netlify

### Option A — Glisser-déposer (le plus rapide)
1. Va sur https://app.netlify.com/drop
2. Glisse le **dossier** (ou le zip) contenant `index.html`.
3. C'est en ligne. Netlify te donne une URL `https://….netlify.app`.

### Option B — Via GitHub (déploiement continu)
1. Crée un dépôt GitHub et pousse ces fichiers à la racine :
   ```
   git init
   git add .
   git commit -m "Codex Chromatica"
   git branch -M main
   git remote add origin https://github.com/<toi>/<depot>.git
   git push -u origin main
   ```
2. Sur Netlify : **Add new site → Import an existing project → GitHub**, choisis le dépôt.
3. Laisse **Build command** vide et **Publish directory** = `.` (déjà défini dans `netlify.toml`).
4. **Deploy**. Chaque `git push` redéploiera automatiquement.


## Atelier — tes propres schémas
L'onglet **Atelier** permet de créer tes schémas : nom, faction, et pour chaque étape la
peinture, sa couleur, la **zone** sur la figurine et le **dosage** (ex. `1:1 eau`, `2 couches fines`,
`glacis 1:4`). Tes schémas sont **sauvegardés dans le navigateur** de l'appareil (localStorage)
une fois l'app servie depuis une vraie URL (Netlify/GitHub Pages). Ils s'ajoutent aussi à la liste de courses.

## Notes
- Aucune donnée n'est envoyée : tout tourne dans le navigateur, hors-ligne possible.
- La liste de courses se réinitialise au rechargement (pas de stockage persistant).
- Marques et noms © Games Workshop / The Army Painter. Projet non officiel.
