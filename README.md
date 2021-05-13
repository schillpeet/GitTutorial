# GitHub Tutorial
Tutorial for beginner [see](https://boolie.org/git-github-anfaenger-tutorial/)

### Dateien auf den Server pushen
1. $ git status
2. $ git add README.md
3. $ git commit -m "Mein Kommentar"
4. $ git push

### Mastering Markdown
It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to MasterinkMarkdown](https://guides.github.com/features/mastering-markdown/)

## Repo, was man sich wünscht, zu sich nehmen
Gehe in das Verzeichnis, in dem du arbeiten möchtest und 'clone' das Repo, das du bearbeiten willst:
1. `fork anklicken`
2. `$ git clone https://github.com/schillpeet/GitTutorial`

## Branches
### Um nicht erstmal in einer Sicherheitskopie (original Datei) zu arbeiten, erstellen wir ein Branch, den wir passend bezeichnen
Erstellte einen neuen branch (hier) namens 'test':<br>
`$ git branch test`

Branches wechseln, hier in den branch 'test' rein.<br>
`$ git checkout test`<br>
> OUTPUT:<br>
> zu Branch 'test' gewechselt<br>

In den branch master wechseln:<br>
`$ git checkout master`

Um in den main branch wieder zu wechseln:<br>
`$ git checkout main`

Anm.: mit fol Kommando kann man einen Branch erstellen und direkt auch in diesen wechseln:<br>
`$ git checkout -b test`

Branches anzeigen lassen:<br>
`$ git branch`

## Änderungen
Wenn wir eine neue Datei erstellt oder verändert haben, dann benutzen wir fol Kommando:<br>
`$ git add neueDatei`<br>
(dadurch steht die Datei in einer besonderen Position, durch fol Kommando machen wir die Änderung offiziell)<br>
`$ git commit`<br>
oder<br>
`$ git commit -m "mein Kommentar"`

Mit diesem Kommando fragen wir ab, ob alle Veränderungen unseres branches, die wir gemacht haben, auch schon hochgeladen haben:<br>
`$ git status`

Branch auf den Server pushen mit Upstream:<br>
Bevor man die Datei pushed, sollte man überprüfen, ob sich etwas verändert hat (s.nächstes Kapitel) oder führe die Kommandos ($git remote add upstream https://...; $git fetch upstream; $git merge upstream/master) durch.<br>
`git push --set-upstream origin branchName`

## Kollaboration - Arbeiten mit anderen:
**Remote repositories** manchen die gemeinsame Arbeit möglich. D.h. wenn wir die Datei geforked haben, sie bearbeitet, sie geadded und committed haben, dann müssen wir ja jetzt wissen, ob sich die Datei zwischenzeitlich schon mal geändert hat. Dies erfolgt mittels remote<br> 

Liste alle remote Repos auf:<br>
`$ git remote -v`<br>
> OUTPUT:<br>
> origin  https://github.com/schillpeet/cloud_haiku.git (fetch)<br>
> origin  https://github.com/schillpeet/cloud_haiku.git (push)<br>

Nun geben wir einen neuen remote Repo upstream an, der mit dem fork mittels **git remote add** synchronisiert. Dadurch erhalten wir eine Referenz auf das aktuelle Repo. Hierbei ist nur wichtig, dass wir den original-owner-username sowie das original-repo am Ende hinschreiben. Wenn sich nichts geändert hat, dann können wir direkt weiter machen mit **fetch** und anschließend **mergen**. 
Falls sich etwas verändert hat:<br>
> `$ git checkout neueDatei` ("neueDatei" ist der Name von dem branch den wir geadded haben)<br>
> `$ git merge master`<br>

`$ git remote add upstream https://github.com/original-owner-username/original-repository.git`<br>
Konkret (bspw):<br>
`$ git remote add upstream https://github.com/do-community/cloud_haiku.git`<br>

> OUTPUT: $ git remote -v<br>
> origin  https://github.com/schillpeet/cloud_haiku.git (fetch)<br>
> origin  https://github.com/schillpeet/cloud_haiku.git (push)<br>
> upstream        https://github.com/do-community/cloud_haiku.git (fetch)<br>
> upstream        https://github.com/do-community/cloud_haiku.git (push)<br>

Um nun den fork aus unserem Arbeitsverzeichnis heraus zu synchronisieren, verwenden wir:<br>
`$ git fetch upstream`<br>
> OUTPUT:<br>
> Von https://github.com/do-community/cloud_haiku
>  * [neuer Branch]    ltagliaferri-patch-1 -> upstream/ltagliaferri-patch-1
>  * [neuer Branch]    master               -> upstream/master

Anm. (laut Tutorial): eig sollte in der letzten Zeile "main -> upstream/main" stehen und, dass commits nun in der lokalen branch upstream/main liegen sollen. Als nächstes soll man dann in den main branch wechseln. Allerdings steht ja bei mir "master -> upstream/master". Ich kann also in den master branch wechseln, aber nicht in den main branch:<br>
`$ git checkout main` (eigentlich)<br>
`$ git checkout master` (funktioniert allerdings nur)<br>

##  Mergen
`$ git merge upstream/main`<br>
bzw. (master wird korrekt sein!)<br>
`$ git merge upstream/master`<br>
> OUTPUT:<br>
> Bereits aktuell.<br>


### Blockquotes
As Kanye West said:
> We're living the future so
> the present is our past.

### Inline code
I think you should use an
`<addr>` element here instead.
