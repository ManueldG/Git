# Comandi Git 

|                |comando                        |descrizione                  |
|----------------|-------------------------------|-----------------------------|
|git clone       |`git clone https://github.com/ManueldG/Git.git`|clona la repository dell'URL passato           |
||||
|git add         |`git add .` |aggiunge tutti i file modificati            |
| | | |
|git checkout \<branch\>   |`git checkout bugFix`| seleziona il branch bugFix |
||||
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
||||
| git merge \<branch\> |`git merge bugFix `| git merge collega il branch passato al branch corrente |
||||
| git reset <--soft/--hard/--mixed/--merge> <commit>|`git reset --hard abc1a677`| soft -> praticamente invariato sposta solo l'indice (HEAD)<br> mixed -> pulisce la staging area ovvero i file modificati aggiunti alla coda con git add per esempio<br>hard -> rimuove tutte le modifiche e torna allineato con HEAD<br>merge -> annulla un merge precedentemente effettuato
||||
|git reflog |`git reflog`| registro delle operazioni effettuate |
||||
|git format-patch \<branch1\>..\<branch2\> |`git format-patch origin/master..bugfix`| crea dei patch tra branch1 e branch2 |
||||
|git log \<options\>|git log --oneline --decorate --graph --all | mostra il log delle modifiche in una struttura ad albero<br> --decorate: Mostra i nomi dei ref di tutti i commit visualizzati. in formato short<br> --all: Mostra i ref in refs/,insieme a HEAD,  elencati sulla riga di comando come \<commit\>.<br> --oneline: Questa è una forma abbreviata per --pretty=oneline --abbrev-commit usati insieme.<br> --graph: Disegna una rappresentazione grafica testuale della cronologia dei commit sul lato sinistro dell'output. Questo potrebbe causare la stampa di righe aggiuntive tra i commit, per consentire la corretta visualizzazione della cronologia del grafico.|
||||

