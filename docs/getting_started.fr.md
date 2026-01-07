# Démarrer avec NanoVec

Bienvenue sur NanoVec ! Ce guide vous aidera à configurer votre environnement de développement et à commencer à construire avec NanoVec.

## Prérequis

Assurez-vous d'avoir installé les éléments suivants :
- **Compilateur Rust** : Version 1.80+ ou l'édition 2024.
- **Cargo** : Le gestionnaire de paquets de Rust.

## Compiler le Projet

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/votreutilisateur/nanovec.git
   cd nanovec
   ```

2. Compilez le projet :
   ```bash
   cargo build --release
   ```

## Utiliser la CLI

Lancez l'aide de la CLI pour voir les commandes disponibles :
```bash
./target/release/nanovec-cli --help
```

## Exemple de Code de Base

Voici comment vous pouvez utiliser NanoVec dans votre projet Rust :

```rust
use nanovec::api::NanoDB;

fn main() {
    let db = NanoDB::new("ma_base_de_donnees.nvec");
    
    let vecteur = vec![0.1, 0.2, 0.3];
    db.insert(vecteur, "Quelques métadonnées".to_string());
    
    let vecteur_requete = vec![0.1, 0.2, 0.29];
    let resultats = db.query(vecteur_requete, 5);
    
    for resultat in resultats {
        println!("Match trouvé : {:?}", resultat);
    }
}
```

## Exécuter les Tests

Pour s'assurer que tout fonctionne correctement :
```bash
cargo test
```

## Documentation

Pour plus de détails, consultez :
- [Architecture](architecture.fr.md)
- [README (Anglais)](../README.md)
- [README (Français)](../README.fr.md)
