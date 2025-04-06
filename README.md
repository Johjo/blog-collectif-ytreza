Installation : 

1. Effectuer un git clone du repository.
2. Récupérer les sub modules 

```
git submodule init
git submodule update

```

Lancer le serveur :
```
hugo server
```

Lancer le serveur avec les drafts :
```
hugo server --buildDrafts
```
ou
```
hugo server -D
```

Ajouter un nouveau contenu :
```
hugo new content content/posts/my-first-post.md
```

`content/posts/my-first-post.md` est le chemin du nouveau post. **Attention de ne pas oublier le .md**

