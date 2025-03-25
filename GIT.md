# Comandi Git 

|                |comando                        |descrizione                  |
|----------------|-------------------------------|-----------------------------|
|git clone       |`git clone https://github.com/ManueldG/Git.git`|clona la repository dell'URL passato           |
|git add         |`git add .` |aggiunge tutti i file modificati            |
| | | |
|git checkout \<branch\>   |`git checkout bugFix`| seleziona il branch bugFix |
|git checkout -b \<branch\>   |`git checkout -b bugFix`| crea e seleziona il branch bugFix |
| | | |
|git branch -f \<branch\> \<posizione\>  |`git branch bugFix f1418d`| sposta il branch in una posizione arbitraria che può essere indicata con l'hash tag o branch della posizione|
| | | |
|git rebase -i \<posizione\> | `git rebase -i bugFix` |effettua un rebase interattivo accodando alla posizione passata i commit tra la posizione corrente e la posizione indicata -i indica **interactive** permette di scegliere i commit da copiare|
| | | |
|git commit -m"message"         |`git commit -m"fixed bug"`|esegue il commit con il messaggio indicato con l'opzione -m|
| git commit -a --amend --no-edit |`git commit -a --amend --no-edit`| usa il commit precedente e aggiunge le modifiche effettuate -a : aggiunge tutte le modifiche, --amend : usa il precedente commit, --no-edit : esegue il comando senza richiedere conferma della modifica del messaggio del commit |
| | | |
|git cherry-pick \<commit\> .. \<commit\> |`git cherry-pick abc1a677 abc1a677`| accoda i commit selezionati al branch corrente|
| git merge \<branch\> |`git merge bugFix `| git merge collega il branch passato al branch corrente |
| git reset <--soft/--hard/--mixed/--merge> <commit>|`git reset --hard abc1a677`| soft -> praticamente invariato sposta solo l'indice (HEAD)<br> mixed -> pulisce la staging area ovvero i file modificati aggiunti alla coda con git add per esempio<br>hard -> rimuove tutte le modifiche e torna allineato con HEAD<br>merge -> annulla un merge precedentemente effettuato
| | | | |
