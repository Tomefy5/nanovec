# Architecture de NanoVec

NanoVec est conçu avec une architecture modulaire pour garantir performance, évolutivité et facilité d'utilisation.

## Module Core (`core/`)

Le module `core` est le cœur algorithmique de NanoVec. Il est responsable de :

- **Implémentation HNSW** : Gère la structure de graphe multicouche pour une récupération rapide des vecteurs.
- **Métriques de Distance** : Implémente les distances Euclidienne, Cosinus et Produit Scalaire avec des optimisations SIMD.
- **Opérations Vectorielles** : Opérations de base sur les données vectorielles.

### Composants Clés

- `HNSWIndex` : La structure d'index principale.
- `VectorNode` : Représente un nœud dans le graphe, contenant le vecteur et ses voisins.
- Trait `Metric` : Définit l'interface pour les calculs de distance.

## Module Storage (`storage/`)

Le module `storage` gère la persistance des données. Il garantit que les vecteurs et l'index peuvent être sauvegardés et chargés du disque efficacement.

- **Format Binaire** : Utilise un format `.nvec` personnalisé pour un stockage compact.
- **Write-Ahead Log (WAL)** : Garantit l'intégrité des données en cas de crash.
- **Page Manager** : (Prévu) Gestion efficace du mappage mémoire pour les grands ensembles de données.

## Module API (`api/`)

Le module `api` fournit une façade propre pour les développeurs. Il abstrait la complexité de `core` et `storage`.

- **NanoDB** : Le point d'entrée principal pour les utilisateurs.
- **Bindings FFI** : Expose NanoVec à d'autres langages comme Python et Node.js en utilisant `pyo3` ou des outils similaires.

## Module CLI (`cli/`)

Le module `cli` fournit une interface en ligne de commande pour interagir avec les bases de données NanoVec sans écrire de code.

- Création et gestion de bases de données.
- Insertion de vecteurs à partir de fichiers CSV/JSON.
- Exécution de recherches de similitude.
