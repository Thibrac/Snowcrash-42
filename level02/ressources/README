Avec la commande ```ls``` dans ce niveau 02 on vois un fichier ```level02.pcap```

Les fichiers .pcap sont des fichiers utilisés pour enregistrer les données du trafic réseau

On telecharge ce ficier .pcap avec la commande ```scp -P 4242 level02@192.168.56.101:level02.pcap ~/Downloads```

On passe dans le logiciel Wireshark qui permet de lire et traiter les ces donnees

On suit le chemin ```analyse > follow > TCP stream``` 

Et la on voit clairement des infos de password: ```Password: ft_wandr...NDRel.L0L```

Apres decodage en hexdump on s'appercois qu'il y a des '.' qui sont des DEL donc il faut supprimer

le mdp de ```su flag02``` est donc ```ft_waNDReL0L``` et avec ```getflag``` on a ```kooda2puivaav1idi4f57q8iq```






































