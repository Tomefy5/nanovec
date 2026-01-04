<p align="center">
  <img src="assets/logo.png" alt="NanoVec Logo" width="200">
</p>

<h1 align="center">NanoVec</h1>

<p align="center">
  <strong>Une base de données vectorielle légère et ultra-rapide pour l'Edge Computing et l'Offline-first.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Rust-2024-orange?logo=rust" alt="Version Rust">
  <img src="https://img.shields.io/badge/Licence-MIT-blue.svg" alt="Licence">
  <img src="https://img.shields.io/badge/PRs-bienvenues-brightgreen.svg" alt="PRs Bienvenues">
  <img src="https://img.shields.io/badge/Statut-Bêta-yellow" alt="Statut">
</p>

---

## 🚀 Pourquoi NanoVec ?

NanoVec est conçue pour les développeurs qui ont besoin d'une recherche de similitude performante sans la lourdeur des solutions cloud classiques. Développé en **Rust**, le projet offre :

- ⚡ **Faible Latence** : Algorithme HNSW pour une recherche en temps logarithmique.
- 📉 **Empreinte Réduite** : Optimisé pour les appareils à mémoire limitée (Edge/Mobile).
- 🛠️ **Zero-Copy Friendly** : Sérialisation efficace pour des E/S ultra-rapides.
- 🧪 **Puissance SIMD** : Utilise l'accélération matérielle pour les calculs vectoriels.

## 🏗️ Architecture

NanoVec suit un design modulaire strict pour garantir flexibilité et performance.

| Module | Responsabilité | Points Clés |
| :--- | :--- | :--- |
| **`core`** | Le Cœur | Algorithme HNSW, métriques SIMD. |
| **`storage`** | Persistance | Format `.nvec` custom, WAL, support mmap. |
| **`api`** | Intégration | Façade pour développeurs, FFI (Python/Node). |
| **`cli`** | Gestion | Outils en ligne de commande pour manipuler les bases. |

## 🛠️ Installation

```bash
# Cloner le dépôt
git clone https://github.com/Tomefy5/nanovec.git

# Accéder au dossier
cd nanovec

# Compiler en mode release
cargo build --release
```

## 📋 Démarrage Rapide

```rust
use nanovec::api::NanoDB;

fn main() {
    // Créer ou charger une base de données
    let db = NanoDB::new("mes_donnees.nvec");

    // Insérer un vecteur avec métadonnées
    db.insert(vec![0.12, 0.45, 0.78], "user_node_1");

    // Effectuer une recherche de similitude (Top-K)
    let resultats = db.query(vec![0.10, 0.40, 0.70], 5);

    println!("Meilleur match : {:?}", resultats[0]);
}
```

## 📖 Documentation

Explorez les détails de NanoVec :

- [Vue d'ensemble de l'architecture](docs/architecture.md)
- [Guide de démarrage complet](docs/getting_started.md)
- [Version Anglaise (README.md)](README.md)

## 🤝 Contribuer

Les contributions sont les bienvenues ! Consultez le fichier [CONTRIBUTING.fr.md](CONTRIBUTING.fr.md) pour commencer.

## ⚖️ Licence

Distribué sous la licence **MIT**. Voir `LICENSE` pour plus d'informations.

---
<p align="center">Propulsé par 🦀 et la communauté NanoVec.</p>
