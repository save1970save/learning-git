# learning-git

repository per imparare git e github

GIT COMMANDS
----------------
git config --global user.name "s.iormetti" <br>
git config --global user.email "s.iormetti@be-tse.it" <br>
git config --global color.ui auto <br>
git config -l -> lista parametri di configurazione <br>
cd desktop/learning-git <br>
git init .    -> inizializza la directory <br>
dir /ah       -> per vedere i files nascosti <br>
type nul >> index.html -> crea un file vuoto   <br>
git status             -> da informazioni sullo stato del progetto / branch <br>
git add index.html     -> aggiunge il file alla staging area <br <br>>
git rm --cached index.html  -> rimuove il file dalla staging are <br>a <br>
git add .              <br> -> aggiunge tutti i files della directory nella staging area <br>
git rm -r --ca <br>ched .   -> rimuove tutti i files dalla staging area <br>
git add -A             -> aggiunge tutti i file della directory e delle sottodirectory nella staging area <br>
git commit -m "bootstrap project"  -> esegue la commit dei files della staging nel reposotory locale <br>
git log                -> mostra lo stato di tutti commit con codice hash e utente <br>
git show <codice hash>      -> mostra lo stato del commit. <br>
git restore index.js   -> annulla le modifiche fatte a un file, riporta il file locale a quello committato nel repository locale. <br>
git commit --amend -m "added body {}"    -> permette di modificare il messaggio dell'ultimo commit <br>
git remote -v  ->  mostra il repository remoto <br>
git remote add origin https://github.com/save1970save/learning-git.git    -> setto il repository remoto, gli associo l'etichetta "origin" <br>
git push origin --delete https://github.com/save1970save/learning-git.git  -> rimuovo il repository remoto, e lo disassocio dall'etichetta "origin" <br>
git remote set-url --add --push origin https://github.com/save1970save/learning-git.git -> risetto il repository remoto, e lo disassocio dall'etichetta "origin" <br>
git branch               -> mostra le branch locali, la branch corrente ha un asterisco <br>
git branch -M main       -> modifica la branch locale da "master" in "main"   <br>
git push -u origin main  -> aggiorna il repository remoto (origin) con i files del repository locale <br>
git push                 -> aggiorna il repository remoto (origin) con i files del repository locale, per le push successive alla prima non serve specificare le branch <br>
git push -f              -> aggiorna il repository remoto (origin) con i files del repository locale, con l'opzione force <br>
git pull                 -> aggiorna il repository local (origin) con i files del repository remoto. <br>
git branch -r            -> mostra le branch remote, la branch corrente ha un asterisco <br>
git branch -a            -> mostra le branch locali e remote <br>
git branch feature-a     -> crea una nuova branch locale come copia della corrente, prima di staccare una branch è best practise fare una pull della main remota. <br>
NB prima di fare un push è meglio fare una pull e una rebase. <br>
git checkout feature-a   -> switcha dalla branch main alla feature-a <br>
git checkout -           -> switcha alla branch precedente <br>
git push -u origin feature-a  -> porta la branch locale nel repository remoto (solo se non esiste ancora nel repositori remoto) <br>
git checkout -b feature-b -> crea la nuova branch feature-b e switcha su quella. <br>
git branch -d feature-b   -> cancella la branch feature-b. <br>
NB La merge di una branch locale non viene fatta mai direttamente con la main remota, ma con la branch remota.  <br>
Inoltre per best practise prima che la branch remota venga mergiata nella main remota, viene fatta una pull request e opzionalmente una merge request. <br>
Dopo la merge viene cancellata la branch remota. e anche la branch locale. Succesivamente da locale si fa una git pull per sincronizzare i repository <br>
git merge feature-a       -> porta le modifiche della branch locale nella main locale.  <br>
git log --online          -> mostra le commit del repository remoto <br>
git pull -r origin main   -> effettua la rebase, ovvero porta le modifiche della main remota sulla branch corrente locale <br>
git rebase --continue     -> dopo avere risolto il conflitto modificando i file manualmente, si effettua la rebase <br>
