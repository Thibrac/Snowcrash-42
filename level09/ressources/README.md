Dans ce niveau on a un axecutable ```level09``` et un fichier ```token```

Le fichier est crypte et l'executale est la pour decrypter

On va reverse la logique de l'executable avec ce code en C dans ```cd /tmp/```:

```C
#include <stdio.h>

int main(int ac, char **av) {
    for(int i = 0; av[1][i]; ++i) {
        av[1][i] -= i;
    }
    printf("%s\n", av[1]);
}
```

On lui passe le contenu du oken avec ```./a.out $(cat /home/user/level09/token)``` pour obtenir le mdp : ```f3iji1ju5yuevaus41q1afiuq```

On va passer ```getflag``` apres ```su flag09``` pour avoir le flag ```s5cAJpM8ev6XHw998pRWG728z```