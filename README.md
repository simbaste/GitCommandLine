# GitCommandLine Guide

git --version (pour savoir quelle version vous utilisez)

Ajouter certaine variable de configuration:
- git config --global user.name "Stephane Mba"
- git config --global user.email "stephane.mba@email.com"
- git config --list (Liste les variables globales git sur votre ordinateur)

pour obtenir de l’aide, faire:
- git help <Verb> ==> (git help config) ou
- git <Verb> --help ==> (git config --help)

commandes récurrentes:
- git status (voire le l’état de votre dossier local git)
- git commit (git commit --help pour avoir les details)
- git add (Ajout des modification dans la « staging area »)
- git reset (suppression des modifications de la « staging area » )
- git log (liste l’ensemble des commit effectués)
- git remote -v (Liste les repertoires (remotes) git liés à notre repertoire local)
- git branch -a (Liste toutes les branches sur notre repertoire)
- git diff (liste les differences entre notre repertoire local et celui distant)
- git push [-u] <remote> <branche> (envoyer nos commits sur le repertoire distant)
    - L’option -u permet à git de se souvenir de notre remote et notre branche. Ce qui nous permettra dans le futur de faire juste (git push)
- git pull <remote> <branche> (récupérer les mise à jours du répertoire distant)
- git branch <name> (créer une branche de nom "name")
- git checkout <nom de la branche> (se déplacer sur une branche)
- git merge <branche a merge> (melange la branche indiquée à celle sur laquelle nous nous trouvons)
- git branch --merged (liste l’ensemble des merges effectués sur la branche courante)
- git branch -d <nom de la branche> (supprimer la branche indiquée)

Corriger les erreurs:
- git commit --amend -m «nouveau message de commit» (changer le message du dernier commit) {Ceci change l’historique}
- git commit --amend (ajouter les modifications se trouvant dans notre « staging area » à notre dernier commit)
- git log --stat (liste les commit avec plus de details sur les fichiers modifiers)
- git cherry-pick <commit hash> (copier le commit indiqué de sa branche d’origin vers la branche courante)
- git reset --soft <commit hash> | <branche> (reset notre repertoire à l’état du commit ou de la branche indiquée) {Cependant l’option «soft» nous permet de sauvegarder toutes les modification sensées êtres supprimer dans la «staging area»}
- git reset --mixed <commit> | <branche> (reset notre repertoire et laisse les changements sur notre repertoire local «non stage»)
- git reset --hard <commit hash> | <branche> (reset notre repertoire et supprime toutes les modifications)
- git clean -df (supprimer toutes les modifications sur notre repertoire courant)
    - (-d) pour tous les dossiers (directories)
    - (-f) pour tous les fichiers (files)
- git reflog (liste les commit avec plus de details sur les modifications apportées)
- git revert <commit hash> (créer un nouveau commit qui exclut les modifications apportées lors du commit indiqué)
