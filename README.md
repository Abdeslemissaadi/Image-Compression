#  Image Compression — SVD, PCA & Autoencoder

> Trois approches de compression d'image : des méthodes algébriques classiques jusqu'au deep learning avec PyTorch.

---

## Description

Ce projet explore et compare trois techniques de compression d'image de complexité croissante.
Il illustre comment la **réduction de dimensionnalité** — qu'elle soit mathématique ou apprise par un réseau de neurones — permet de reconstruire une image à partir d'une représentation compacte.

---

##  Méthodes Implémentées

###  SVD — Décomposition en Valeurs Singulières
- Décompose la matrice image en U, Σ, Vt
- Conserve uniquement les k plus grandes valeurs singulières
- Testé en niveaux de gris et en couleur (R, G, B séparément)
- Valeurs de k testées : `[5, 20, 50, 100]`

###  PCA — Analyse en Composantes Principales
- Appliquée canal par canal sur l'image couleur
- Reconstruction via `inverse_transform`
- Comparaison visuelle pour k = `[10, 50, 100]`

### Autoencoder (Deep Learning — PyTorch)
- Réseau encodeur/décodeur entraîné sur MNIST
- Espace latent de dimension 32
- Encodeur : `784 → 256 → 32`
- Décodeur : `32 → 256 → 784`
- Entraîné sur 10 epochs avec Adam + MSELoss
- Visualisation côte à côte : images originales vs reconstruites
