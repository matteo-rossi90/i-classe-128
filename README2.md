## [deploy progetto vue su github pages](https://www.youtube.com/watch?v=yo2bMGnIKE8)

Una volta creata la repository, con il nostro progetto vue terminato, pushato su github, bisogna:
- modificare `vite.config.js` aggiungendo base: `/nome-repository/`
- buildare il progetto vue con `npm run build` (la build si troverà nella cartella `dist`)
- aggiungiamo la cartella `/dist` in staging con `git add dist -f` e fare commit con `git commit -m "messaggio di commit"` 
- lanciamo `git subtree push --prefix dist origin gh-pages` (una sorta di sottorepository che punta al branch gh-pages della repository github)
- il nostro progetto sarà disponibile su github pages