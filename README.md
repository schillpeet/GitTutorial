# GitHub Tutorial
Tutorial for beginner [see](https://boolie.org/git-github-anfaenger-tutorial/)

### Dateien auf den Server pushen
1. $ git status
2. $ git add README.md
3. $ git commit -m "Mein Kommentar"
4. $ git push

### Mastering Markdown
It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to MasterinkMarkdown](https://guides.github.com/features/mastering-markdown/)

### Repo, was man sich wünscht, zu sich nehmen
Gehe in das Verzeichnis, in dem du arbeiten möchtest und 'clone' das Repo, das du bearbeiten willst:
1. `fork anklicken`
2. `$ git clone https://github.com/schillpeet/GitTutorial`

### Branches
#### Um nicht erstmal in einer Sicherheitskopie zu arbeiten, erstellen wir ein Branch, den wir passend bezeichnen
Erstellten branch nennen wir hier 'test':<br>
`$ git branch test`

So wechseln wir in den Branch 'test' rein. OUTPUT: zu Branch 'test' gewechselt<br>
`$ git checkout test`

Anm.: mit fol Kommando kann man einen Branch erstellen und direkt auch in diesen wechseln:<br>
`$ git checkout -b test`

Branches anzeigen lassen:<br>
`$ git branch`

Um in den main branch wieder zu wechseln:<br>
`$ git checkout main`

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
`git push --set-upstream origin branchName`

## Kollaboration - Arbeiten mit anderen:
**Remote repositories** manchen die gemeinsame Arbeit möglich. Liste alle remote Repos auf:
`$ git remote -v`<br>
OUTPUT example:<br>
origin  https://github.com/schillpeet/cloud_haiku.git (fetch)
origin  https://github.com/schillpeet/cloud_haiku.git (push)

Branch in den master wechseln:
`<git checkout master>`

### Mergen
`<git merge README_Info>`

Beide Branches sind jetzt zusammen gesetzt worden.

### Blockquotes
As Kanye West said:
> We're living the future so
> the present is our past.

### Inline code
I think you should use an
`<addr>` element here instead.
