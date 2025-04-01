En cherchant un peu on trouve ce fichier ```cat /etc/passwd```

Avec cette ligne ```flag01:42hDRfypTqqnw:3001:3001::/home/flag/flag01:/bin/bash```

On va extraire le fichier avec ```scp -P 4242 level01@192.168.56.101:/etc/passwd ~/Downloads```

Et on le fait passer dans john the ripper avec ```./john passwd```

On obtient ```flag01:abcdefg:3001:3001::/home/flag/flag01:/bin/bash```

