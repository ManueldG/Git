[![Open Source Love](https://firstcontributions.github.io/open-source-badges/badges/open-source-v1/open-source.png)](https://github.com/firstcontributions/open-source-badges) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Open Source Helpers](https://www.codetriage.com/manueldg/git/badges/users.svg)](https://www.codetriage.com/manueldg/git)
 

# Repository per esercitazione su GIT

In varie occasioni mi è capitato di dover eseguire delle operazioni su alcune repository per risolvere conflitti o cancellare dei commit errati, 
ho dovuto fare pratica con delle repository test come questa per studiarmi gli effetti dei vari comandi di Git.

Pubblico questa Repo per chi come me voglia esercitarsi con Git e magari contribuire aggiungendo i comandi usati alla tabella [Comandi Git](GIT.md).

per fare pratica si può aggiungere e modificare i file nella cartella [area di prova](area_prova)

---

## Fai il fork di questa repository

Clicca sul pulsante in alto ***fork*** creerà una repo nel tuo account.

## Scarica la repository

https://github.com/ManueldG/Git.git
Per inviare le modifiche puoi andare sul tuo account e poi sulla repo appena creata e copiare l'url cliccando su ***Code*** di solito in formato `https://github.com/\<tuo-nome-utente\>/Git.git`
apri il terminale e quindi digitare il comando `git clone` e poi l'URL copiato 

```bash
git clone https://github.com/tuo-nome-utente/Git.git
```

## Crea un ramo (*Branch*)

Non è possibile inviare le modifiche direttamente è meglio tenere il master sincronizzato con la repository originale e creare dei rami (branch) per ogni file da modificare.

Entra nella directory della repository:

```bash
cd git
```

Ora crea un ramo (*branch*) usando il comando `git branch`  oppure `git checkout -b`:

Il primo comando crea il branch poi bisogna selezionarlo con `git checkout`

```bash
git branch <nome-del-ramo>
git checkout <nome-del-ramo>
```

oppure usando il secondo comando

```bash
git checkout -b <nome-del-ramo>
```

Ad esempio:

```bash
git branch bugFix
git checkout bugFix
```
oppure

```bash
git checkout -b bugFix
```

## Fai le modifiche necessarie e crea un commit

Effettua le tue modifiche poi per aggiungere le modifiche alla coda dello ***staging area*** tramite `git add`:

con questo comando aggiunge tutte le modifiche alla coda
 
```bash
git add .
```

oppure è possibile aggiungere solo i file selezionati

es.:
```bash
git add git.md
```

Ora usare `git commit` per caricarlo nella repository locale:

```bash
git commit -m "Modificato il file git.md"
```

## Invia le modifiche su GitHub

Inviare (*push*) le tue modifiche con il comando `git push`:

```bash
git push 
```
che caricherà le modifiche nel branch selezionato in precedenza.

## Invia i tuoi cambiamenti per una revisione

Se vai nella tua repository su GitHub, vedrai il pusante  `Compare & pull request`.  Mostrerà le modifiche effettuate e poi
 invia la PR (pull request).

 In seguito posso commentare le modifiche, fare il merge oppure chiudere la PR nel caso nel modifiche non siano necessarie o corrette.


---


Plug-in usati:
[Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
[Gitignore](https://marketplace.visualstudio.com/items?itemName=codezombiech.gitignore)

Editor:
[Visual Studio Code](https://code.visualstudio.com/)
