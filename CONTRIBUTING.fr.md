# Contribuer à NanoVec

Merci de votre intérêt pour NanoVec ! Nous acceptons toutes les contributions, des rapports de bugs aux nouvelles fonctionnalités.

## Comment Contribuer

### Signaler des Bugs
- Utilisez le [modèle de rapport de bug](.github/ISSUE_TEMPLATE/bug_report.md).
- Fournissez une description claire du problème et les étapes pour le reproduire.

### Suggérer des Fonctionnalités
- Utilisez le [modèle de demande de fonctionnalité](.github/ISSUE_TEMPLATE/feature_request.md).
- Décrivez le cas d'utilisation et pourquoi la fonctionnalité serait bénéfique.

### Pull Requests
1. Forkez le dépôt.
2. Créeez une nouvelle branche (`git checkout -b feature/ma-nouvelle-fonctionnalite`).
3. Apportez vos modifications.
4. Assurez-vous que le code respecte les standards du projet (lancez `cargo fmt` et `cargo clippy`).
5. Lancez les tests (`cargo test`).
6. Commitez vos changements (`git commit -m 'feat: ajout d'une fonctionnalité'`).
7. Pushez vers la branche (`git push origin feature/ma-nouvelle-fonctionnalite`).
8. Ouvrez une Pull Request.

## Configuration du Développement

1. Installez Rust : `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`
2. Clonez le dépôt : `git clone https://github.com/Tomefy5/nanovec.git`
3. Compilez le projet : `cargo build`

## Standards de Codage

- **Formatage** : Toujours lancer `cargo fmt` avant de commiter.
- **Lints** : Aucun nouvel avertissement clippy ne doit être introduit.
- **Tests** : Ajoutez des tests pour toute nouvelle fonctionnalité.

## Code de Conduite

Veuillez noter que ce projet est publié avec un [Code de Conduite du Contributeur](CODE_OF_CONDUCT.md). En participant à ce projet, vous acceptez d'en respecter les termes.
