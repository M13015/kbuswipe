# Ma chaîne vidéo

Un site de vidéos et de photos verticales façon TikTok. Toi seul publies, les visiteurs regardent.

Personne d'autre ne peut ajouter de vidéo : seul le propriétaire du dépôt GitHub peut modifier les fichiers.

## Mettre le site en ligne (une seule fois)

1. Va sur github.com, connecte-toi, puis clique sur **New repository**.
2. Donne un nom au dépôt (par exemple `ma-chaine`), laisse-le **Public**, puis clique sur **Create repository**.
3. Clique sur **uploading an existing file**, glisse tous les fichiers de ce dossier (`index.html`, `videos.json`, `README.md` et le dossier `videos`), puis clique sur **Commit changes**.
4. Va dans **Settings** puis **Pages**. Sous **Branch**, choisis `main` et le dossier `/ (root)`, puis clique sur **Save**.
5. Attends une minute. L'adresse de ton site s'affiche en haut de la page Pages : `https://TON-PSEUDO.github.io/ma-chaine/`.

## Publier une nouvelle vidéo ou photo

1. Ouvre ton dépôt sur GitHub, entre dans le dossier `videos`, puis clique sur **Add file** puis **Upload files**. Dépose ta vidéo (par exemple `voyage.mp4`) et clique sur **Commit changes**.
2. Reviens à la racine du dépôt, ouvre `videos.json`, clique sur l'icône crayon et ajoute ta vidéo **en premier** dans la liste :

```json
{
  "channel": "Ma chaîne",
  "videos": [
    { "file": "voyage.mp4", "caption": "Mon premier voyage", "date": "2026-11-10" },
    { "file": "ancienne-video.mp4", "caption": "Avant", "date": "2026-11-01" }
  ]
}
```

3. Clique sur **Commit changes**. La vidéo apparaît sur le site après environ une minute.

La vidéo la plus récente doit être en haut de la liste. Les noms de fichiers ne doivent pas contenir d'espaces (utilise `mon-voyage.mp4`).

## Photos

Les photos se publient exactement comme les vidéos : dépose le fichier dans le dossier `videos` et ajoute une ligne dans `videos.json`, par exemple `{ "file": "plage.jpg", "caption": "La plage", "date": "2026-11-10" }`. Les formats `.jpg`, `.jpeg`, `.png`, `.webp`, `.gif` et `.avif` sont reconnus. Une photo s'affiche en plein écran, sans bouton de lecture. Garde chaque photo sous 5 Mo.

## Conseils pour les vidéos

- Format MP4 (codec H.264), en vertical (1080 x 1920) si possible.
- GitHub refuse les fichiers de plus de 100 Mo. Reste sous 25 Mo par vidéo pour un chargement rapide.
- Change le nom de la chaîne en modifiant `"channel"` dans `videos.json`.
