# CoproAudit — Site vitrine

Site vitrine de **CoproAudit**, le système d'exploitation des copropriétés modernes : gouvernance, conformité et risques surveillés en continu par l'IA.

Le site est 100 % statique et autonome : une seule page `index.html` (HTML + CSS + JS inclus), sans build, sans dépendance ni framework. La navigation entre les cinq vues (Accueil, Plateforme, Le moteur IA, Confiance, Vision) se fait par ancres (`#accueil`, `#plateforme`, `#coproaudit`, `#confiance`, `#vision`).

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | Le site complet (contenu, styles, animations) |
| `favicon.svg` / `favicon.png` / `apple-touch-icon.png` | Icônes du site |
| `404.html` | Page d'erreur avec retour à l'accueil |
| `robots.txt` | Autorise l'indexation |
| `.nojekyll` | Désactive le traitement Jekyll sur GitHub Pages |

## Aperçu en local

Ouvrez simplement `index.html` dans un navigateur, ou servez le dossier :

```bash
python3 -m http.server 8000
# puis http://localhost:8000
```

## Mise en ligne

### GitHub Pages (recommandé, gratuit)

1. Sur GitHub : **Settings → Pages**.
2. Source : **Deploy from a branch**, branche `main`, dossier `/ (root)`.
3. Le site est publié en quelques minutes sur `https://<votre-compte>.github.io/CoproAudit-landing-page/`.

### Netlify / Vercel / Cloudflare Pages

Importez le dépôt (ou glissez-déposez le dossier). Aucune commande de build : publiez le dossier racine tel quel.

### Hébergeur classique (OVH, etc.)

Copiez tous les fichiers du dépôt à la racine du serveur web.

## Avant le lancement — points à personnaliser

- **Domaine** : une fois votre domaine choisi, ajoutez dans `<head>` une balise `<link rel="canonical" href="https://votredomaine.fr/">` et les balises `og:url` / `og:image` correspondantes.
- **Témoignages et indicateurs** : les témoignages et chiffres d'impact sont illustratifs (mentions « à remplacer par vos clients réels » dans la page). Remplacez-les par vos données réelles.
- **Boutons « Demander une démonstration »** : ils pointent vers la vue Vision. Reliez-les à votre outil de prise de rendez-vous (Calendly, formulaire…) le moment venu.
- **Images** : les photos sont chargées depuis Unsplash (avec un dégradé de repli si l'image ne charge pas). Pour une indépendance totale, remplacez les `src` par des images hébergées avec le site.
