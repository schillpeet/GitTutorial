# GitHub Tutorial
Tutorial for beginner [see](https://boolie.org/git-github-anfaenger-tutorial/)

### Dateien auf den Server pushen
1. $ git status
2. $ git add README.md
3. $ git commit -m "Mein Kommentar"
4. $ git push

### Mastering Markdown
It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to MasterinkMarkdown](https://guides.github.com/features/mastering-markdown/)

### Dateien vom Server holen
#### im neu erstellten Verzeichnis
$ git clone https://github.com/schillpeet/GitTutorial

### Blockquotes
As Kanye West said:
> We're living the future so
> the present is our past.

### Inline code
I think you should use an
`<addr>` element here instead.


### Branches
Branch erstellen und wechselt auch sofort in diesen:
`<git checkout -b "README_Info">`

Branches anzeigen lassen:
`<git branch>`

Branch auf den Server pushen mit Upstream:
(nach *git add README.md* und *git commit -m "was auch immer"*)
`<git push --set-upstream origin README_Info>`

Branch in den master wechseln:
`<git checkout master>`
