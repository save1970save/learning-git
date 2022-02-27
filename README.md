# learning-git

repository per imparare git e github

GIT COMMANDS
----------------
git config --global user.name "s.iormetti"<br>
git config --global user.email "s.iormetti@be-tse.it"
git config --global color.ui auto
git config -l -> lista parametri di configurazione
cd desktop/learning-git 
git init .    -> inizializza la directory
dir /ah       -> per vedere i files nascosti
type nul >> index.html -> crea un file vuoto  
git status             -> da informazioni sullo stato del progetto / branch
git add index.html     -> aggiunge il file alla staging area
git rm --cached index.html  -> rimuove il file dalla staging area
git add .              -> aggiunge tutti i files della directory nella staging area
git rm -r --cached .   -> rimuove tutti i files dalla staging area
git add -A             -> aggiunge tutti i file della directory e delle sottodirectory nella staging area
git commit -m "bootstrap project"  -> esegue la commit dei files della staging nel reposotory locale
git log                -> mostra lo stato di tutti commit con codice hash e utente
git show <codice hash>      -> mostra lo stato del commit.
git restore index.js   -> annulla le modifiche fatte a un file, riporta il file locale a quello committato nel repository locale.
git commit --amend -m "added body {}"    -> permette di modificare il messaggio dell'ultimo commit
git remote -v  ->  mostra il repository remoto
git remote add origin https://github.com/save1970save/learning-git.git    -> setto il repository remoto, gli associo l'etichetta "origin"
git push origin --delete https://github.com/save1970save/learning-git.git  -> rimuovo il repository remoto, e lo disassocio dall'etichetta "origin"
git remote set-url --add --push origin https://github.com/save1970save/learning-git.git -> risetto il repository remoto, e lo disassocio dall'etichetta "origin"
git branch               -> mostra le branch locali, la branch corrente ha un asterisco
git branch -M main       -> modifica la branch locale da "master" in "main"  
git push -u origin main  -> aggiorna il repository remoto (origin) con i files del repository locale
git push                 -> aggiorna il repository remoto (origin) con i files del repository locale, per le push successive alla prima non serve specificare le branch
git push -f              -> aggiorna il repository remoto (origin) con i files del repository locale, con l'opzione force
git pull                 -> aggiorna il repository local (origin) con i files del repository remoto.
git branch -r            -> mostra le branch remote, la branch corrente ha un asterisco
git branch -a            -> mostra le branch locali e remote
git branch feature-a     -> crea una nuova branch locale come copia della corrente, prima di staccare una branch è best practise fare una pull della main remota.
NB prima di fare un push è meglio fare una pull e una rebase.
git checkout feature-a   -> switcha dalla branch main alla feature-a
git checkout -           -> switcha alla branch precedente
git push -u origin feature-a  -> porta la branch locale nel repository remoto (solo se non esiste ancora nel repositori remoto)
git checkout -b feature-b -> crea la nuova branch feature-b e switcha su quella.
git branch -d feature-b   -> cancella la branch feature-b.
NB La merge di una branch locale non viene fatta mai direttamente con la main remota, ma con la branch remota. 
Inoltre per best practise prima che la branch remota venga mergiata nella main remota, viene fatta una pull request e opzionalmente una merge request.
Dopo la merge viene cancellata la branch remota. e anche la branch locale. Succesivamente da locale si fa una git pull per sincronizzare i repository
git merge feature-a       -> porta le modifiche della branch locale nella main locale. 
git log --online          -> mostra le commit del repository remoto
git pull -r origin main   -> effettua la rebase, ovvero porta le modifiche della main remota sulla branch corrente locale
git rebase --continue     -> dopo avere risolto il conflitto modificando i file manualmente, si effettua la rebase
