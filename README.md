# ⚡ La boîte à outils — portefeuille de 10 micro-apps

10 outils web mono-fichier (HTML/CSS/JS, zéro dépendance), réunis sur un seul site et **reliés
entre eux** (chaque page renvoie vers les 9 autres → le visiteur circule, le trafic monte).
Monétisation : **pub display** (AdSense/Ezoic).

## Les 10 outils
| Dossier | Outil | Cible / recherche |
|---|---|---|
| `pseudos/` | Générateur de pseudos stylés | gaming, ados |
| `robux/` | Robux ⇄ € | joueurs Roblox |
| `roue/` | Roue de tirage au sort | "roue aléatoire" (gros volume) |
| `minuteur/` | Minuteur / compte à rebours | evergreen énorme |
| `mot-de-passe/` | Générateur de mot de passe | evergreen |
| `pourcentage/` | Calcul de pourcentage | scolaire, evergreen |
| `compteur-mots/` | Compteur de mots | étudiants, rédacteurs |
| `bio/` | Bio stylée Insta/TikTok | ados, réseaux sociaux |
| `noms/` | Générateur de noms | gaming |
| `pile-ou-face/` | Pile ou face & dé | jeux |

## 1) Tester en local
Ouvre `index.html` (la page d'accueil) dans ton navigateur. Tout marche hors-ligne.

## 2) Mettre en ligne (gratuit, GitHub Pages)
```bash
cd micro-apps
git init && git add . && git commit -m "10 outils"
git branch -M main
git remote add origin https://github.com/<toi>/outils.git
git push -u origin main
```
Puis GitHub → **Settings → Pages → Source = main / root → Save**.
Site en ligne sur `https://<toi>.github.io/outils/` en quelques minutes.

> Encore plus simple : glisse le dossier `micro-apps` sur https://app.netlify.com/drop

**Après mise en ligne :** remplace `TON-DOMAINE` dans `robots.txt` et `sitemap.xml` par ton URL,
puis soumets le sitemap dans **Google Search Console** (indispensable pour être référencé).

## 3) Activer la pub (AdSense)
1. Crée un compte https://adsense.google.com (le site doit être en ligne).
2. Récupère ton ID `ca-pub-XXXX`.
3. Dans **chaque** `index.html` : décommente la balise `<script>` AdSense dans le `<head>`
   et remplace `ca-pub-XXXX`. (Astuce : un simple chercher-remplacer global suffit.)
4. Remplace les blocs `<div class="ad">…</div>` par tes blocs d'annonces.

> En attendant la validation AdSense (parfois lente), **Ezoic** ou **Adsterra** acceptent plus vite.

## 4) Comment ça gagne 25–50€/mois (par outil)
La pub paie au trafic. Visée : **5 000–15 000 visites/mois** par outil populaire.
Pour amener le trafic :
- **SEO** : titres/descriptions déjà optimisés + sitemap → soumettre à Search Console.
- **Partage** : Discord gaming, TikTok, communautés Roblox/Fortnite (pour pseudos, robux, bio, noms).
- **Liens internes** : déjà en place, ils boostent le référencement de tout le site.
- Réalité du portefeuille : 6-7 outils feront peu, 2-3 porteront le revenu. C'est normal — on garde et on pousse les gagnants.

## Idées d'évolution
- Pages dédiées par jeu (`/pseudos/roblox`, `/pseudos/fortnite`) pour ranker sur chaque mot-clé.
- Mémoire des favoris (localStorage).
- PWA (installable sur téléphone) pour le minuteur.
