# Bestioles Timides

Moniteur de bruit pour la classe, en français, dans le navigateur. Le micro mesure le volume de la salle : tant que la classe reste calme, des créatures originales sortent une à une. Si le bruit dure, la scène se couvre de brouillard et les créatures s'enfuient (ou restent en pause, au choix).

- 3 scènes (clairière, récif, espace), collection conservée dans le navigateur ; les créatures non encore rencontrées sont grisées
- Objectifs : silencieux, individuel, binôme, ou curseur personnalisé ; calibrage facultatif
- **Tes propres créatures** : dépose des images (png, jpg, gif, webp, svg) dans le dossier `creatures/`. Chacune devient une créature collectable, nommée d'après son fichier sans l'extension. La liste est lue automatiquement, sans autre réglage (voir plus bas).
- Aucun enregistrement : le son n'est mesuré que localement
- Mode sans micro pour tester : maintenir la barre d'espace

Un seul fichier, `index.html`. Pour le publier : Settings → Pages → Deploy from a branch → `main` / root.

## Ajouter des créatures

Dépose les images dans `creatures/` (sur GitHub : `creatures` → Add file → Upload files). Elles apparaissent au prochain chargement de la page. Seules les images de ce dossier apparaissent dans le jeu et dans la collection (grisées tant qu'elles n'ont pas été rencontrées).

La page lit le dossier via l'API publique de GitHub. Hors ligne ou en ouvrant le fichier sans le dépôt, ajoute un fichier `creatures/liste.json` contenant la liste des noms de fichiers, par exemple `["Gloubi.png","Tidou.png"]`.
