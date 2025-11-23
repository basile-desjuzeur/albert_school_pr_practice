# Instructions -- Workflow Git & GitHub

Cet exercice est basé sur [ce projet](https://github.com/mathurinm/github-assignment) maintenu par Mathurin Massias.

## 0. Créer un personnal access token 

- Allez sur [ce lien](https://github.com/settings/tokens)

- Cliquez sur **Generate new token** (classic)

- Donnez un nom à ce token (par ex : _cours-git__)

- Cochez l'option **repo**

- Cliquez sur **Generate token**

- Copiez le token dans un endroit sûr (_e.g. Bitwarden, Proton_)

## 1. Forker le dépôt

-   Cliquez sur **Fork** en haut à droite de la page GitHub du projet.

## 2. Cloner votre fork

    git clone VOTRE_URL_DE_FORK

## 3. Vérifier les dépôts distants (remotes)

    git remote -v

Vous devez voir l'URL de votre fork (`origin`).

## 4. Ajouter le dépôt original comme remote upstream

    git remote add upstream https://github.com/basile-desjuzeur/albert_school_pr_practice

## 5. Vérifier à nouveau les remotes

    git remote -v

Vous devez maintenant voir **origin** et **upstream**.

## 6. Créer une branche à votre nom

    git branch -c YOURNAME
    git checkout YOURNAME

Vérifier : git status

## 7. Modifier le fichier students.txt

-   Ouvrez le fichier localement.
-   Ajoutez un **X** à la fin de la ligne où apparaît votre nom.

## 8. Ajouter et commit

    git add students.txt
    git commit -m "Ajout du X à côté de mon nom"

Vérifier : git status

## 9. Pousser votre branche vers votre fork

    git push --set-upstream origin YOURNAME

## 10. Créer une Pull Request

-   Rendez-vous sur :
    https://github.com/basile-desjuzeur/albert_school_pr_practice/pulls
    
    Créez une PR depuis votre branche vers `main` du repo original.

## 11. En cas de conflits

Mettre à jour : git pull upstream main

Résoudre les conflits puis : git add . git commit git push

## 12. Me prévenir


## 13. Après le merge

Supprimez votre branche

    git switch main
    git branch -D YOURNAME

## 14. Synchroniser votre main

    git pull upstream main
