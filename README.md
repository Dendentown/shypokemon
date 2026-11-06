# Bestioles Timides

Moniteur de bruit pour la classe, en français, dans le navigateur. Le micro mesure le volume de la salle : tant que la classe reste calme, des créatures originales sortent une à une. Si le bruit dure, la scène se couvre de brouillard et les créatures s'enfuient (ou restent en pause, au choix).

- 3 scènes (clairière, récif, espace), collection conservée dans le navigateur ; 3 niveaux de rareté ; les créatures non encore rencontrées sont grisées
- Objectifs : silencieux, individuel, binôme, ou curseur personnalisé ; calibrage facultatif
- **Tes propres créatures** : dépose des images (png, jpg, gif, webp, svg) dans le dossier `creatures/`. Chacune devient une créature collectable, nommée d'après son fichier sans l'extension. La liste est lue automatiquement, sans autre réglage (voir plus bas).
- Aucun enregistrement : le son n'est mesuré que localement
- Mode sans micro pour tester : maintenir la barre d'espace

Un seul fichier, `index.html`. Pour le publier : Settings → Pages → Deploy from a branch → `main` / root.

## Raretés et dossiers

Les créatures sont rangées par rareté, chaque rareté ayant son sous-dossier dans `creatures/` :

- `creatures/commun/` : 70 % des apparitions
- `creatures/rare/` : 25 % des apparitions, halo bleu et bandeau « Créature rare »
- `creatures/legendaire/` : 5 % des apparitions, halo doré, plus grande, bandeau « Créature légendaire »

Dépose une image (png, jpg, gif, webp ou svg) dans le bon sous-dossier : elle apparaît au prochain chargement de la page. Son nom dans le jeu est le nom du fichier sans l'extension. La collection est classée par rareté, et chaque créature reste grisée tant qu'elle n'est pas apparue.

La page lit le dossier via l'API publique de GitHub, et lit aussi `creatures/liste.js`. En ouvrant `index.html` depuis ton ordinateur, seule `liste.js` est lue : ajoute-y le nom de tes images dans la rareté correspondante.
