Réponses du TP1 : Maîtrise de Git



Partie 3 : Concepts de base



Q3. Annuler les modifications locales d'un fichier avant de les ajouter à l'index ?



Il suffit de restaurer le fichier depuis le dernier commit avec `git checkout -- eda.py` (ou `git restore eda.py`). Les modifications non commitées sont alors perdues



Q4. Visualiser les fichiers prêts à être commités (staging) ?



Avec `git status`, les fichiers apparaissent dans la section « Changes to be committed ». Pour voir le détail des modifications indexées, on utilise `git diff --staged`



Partie 4 : Collaborer sur Git



Q4. Suivre un dépôt distant et récupérer toutes les branches ?



On utilise `git fetch --all`, qui télécharge toutes les branches distantes, puis `git branch -r` pour les lister



Q5. Supprimer une branche locale après l'avoir fusionnée dans master ?



On utilise `git branch -d experiment-eda`. Git refuse la suppression si la branche n'est pas fusionnée (`-D` force la suppression)



Partie 5 : Rebase



Q8. Interrompre un rebase en cours en cas d'erreur ?



On utilise `git rebase --abort`, qui ramène la branche à l'état d'avant le rebase.



Q9. Lister les commits qui vont être rebasés avant de lancer un rebase ?



On utilise `git log --oneline main..experiment-eda` : cela affiche les commits de `experiment-eda` absents de `main`

