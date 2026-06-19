# 🧠 Neurofeedback — Vidéos & Podcasts

Bibliothèque web qui regroupe et classe **par thématique** les vidéos, conférences,
podcasts et témoignages partagés autour du neurofeedback.

👉 **Site en ligne :** https://sacha9214.github.io/neurofeedback-videos/

## Thématiques

- ✨ **Découvrir le neurofeedback** — pour comprendre la pratique
- 🎤 **Conférences & Webinaires** — interventions et replays
- 🎧 **Podcasts** — sommeil, bonheur, fonctionnement du cerveau
- 💬 **Témoignages** — retours de patients
- 📚 **Playlists** — collections complètes

## Comment ça marche

- Site **100 % statique** : un seul fichier [`index.html`](index.html), aucune dépendance, aucun build.
- Les vidéos restent **hébergées sur YouTube** — le site ne fait que les organiser.
- Les **titres réels** des vidéos sont récupérés automatiquement (via [noembed](https://noembed.com)),
  avec un repli si la requête échoue.
- Les vignettes proviennent de l'API d'images YouTube.

## Ajouter / modifier une vidéo

Tout se passe dans le tableau `DATA` au bas de [`index.html`](index.html) :

```js
{ type:"video", id:"IDENTIFIANT_YOUTUBE", theme:"podcasts", note:"Courte description." }
```

- `type` : `"video"` ou `"playlist"`
- `id` : l'identifiant YouTube (la partie après `watch?v=` ou `playlist?list=`)
- `theme` : `decouverte` · `conferences` · `podcasts` · `temoignages` · `playlists`
- `note` : la phrase de contexte affichée sous le titre

## Lancer en local

```bash
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

---

Construit à partir des partages du groupe *Neurofeedback Family*.
