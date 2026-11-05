# Centro Cosat Car – maquette 3D

Maquette 3D interactive (Three.js r128) du lavage Cosat Car agrandi :

- **Taller mecánico + neumáticos** – 16 × 5 m, 3 portes de 3 × 6 m (bureau direction + pneus, puis 2 ponts élévateurs en diagonale)
- **Lavado existente** – conservé au centre, façades alignées
- **Lavandería autoservicio** – 6 × 5 m, entièrement vitrée, s'arrête avant la grille de plomberie

## Lancer

Un seul fichier, aucune installation : ouvrir `index.html` dans un navigateur.
Three.js est chargé depuis cdnjs / jsDelivr (connexion internet nécessaire).

## Publier avec GitHub Pages

Settings → Pages → Source : branche `main`, dossier `/ (root)`.
Le site sera disponible sur `https://<utilisateur>.github.io/<repo>/`.

## Structure du code (`index.html`, bloc `<script>`)

| Section | Rôle |
|---|---|
| Rendu réaliste | ciel, environnement (reflets), textures procédurales |
| `car()` | modèle de voiture (silhouette extrudée) |
| Site | sol, murs de soutènement, poteau électrique, parking |
| Lavado existente | module central x 0 → 14 |
| Lavandería | x 14 → 20, machines, personnages animés |
| Taller | x −16 → 0 : dirección + neumáticos, 2 elevadores |
| Cotas / Vistas | cotes, étiquettes, vues caméra |
| Visita a pie | mode première personne + collisions (`blocked()`) |

Unités : mètres. Axe x le long du mur, z vers le parking (façades à z = 5).
