# TP 3 : Ingenierie Deep Learning — TensorFlow vs PyTorch

Comparaison des deux ecosystemes de Deep Learning (PyTorch et TensorFlow) sur
un ensemble d'exercices : algebre tensorielle, differenciation automatique,
pipeline de classification d'images CNN et gestion multi-device.

## Organisation du projet

```
TP_3/
├── tp3_deep_learning.ipynb    Notebook complet : les 4 parties / 6 exercices
├── requirements.txt           Dependances epinglees
└── README.md
```

Le notebook est organise en sections suivant le sujet du TP :

- **Introduction** — verification des versions et du GPU, fixation de la graine.
- **Partie 1 — Fondations** : Ex. 1 initialisation comparee, Ex. 2 typage /
  interop NumPy / reshaping.
- **Partie 2 — Autograd** : Ex. 3 descente de gradient sur Rosenbrock
  (`backward()` vs `tf.GradientTape()`).
- **Partie 3 — CNN** : Ex. 4 architecture du modele, Ex. 5 boucle
  d'entrainement personnalisee (Adam).
- **Partie 4 — Materiel** : Ex. 6 placement CPU/GPU et question de reflexion.

## Installation

```bash
python -m venv .venv
source .venv/bin/activate        # Windows : .venv\Scripts\activate
pip install -r requirements.txt
```

## Reproductibilite

La graine aleatoire est fixee a `42` (fonction `fixer_graine`) pour NumPy,
PyTorch et TensorFlow. Le notebook relance donc les memes tirages et produit les
memes resultats d'une execution a l'autre.

## Execution

Ouvrir `tp3_deep_learning.ipynb` dans Jupyter / VS Code et executer les cellules
dans l'ordre, ou en ligne de commande :

```bash
jupyter nbconvert --to notebook --execute --inplace tp3_deep_learning.ipynb
```

La Partie 3 telecharge automatiquement FashionMNIST via `tf.keras.datasets` lors
de la premiere execution.
