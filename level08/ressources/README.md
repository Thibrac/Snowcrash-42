Dans ce niveau on a un executable ```level08``` et un fichier ```token```

Quand on disas le main de ce prog on voit qu'il lit et affiche le contenu du fichier passe en param

On voit aussi que si le fichier s'appel "token" il ```exit(1)```

Donc on va simplement faire un lien symbolique du fichier ```ln -s /home/user/level08/token /tmp/redir```

Ensuite on execute le prog avec notre lien symbolique ```./level08 /tmp/redir``` et le mdp s'affiche : ```quif5eloekouj29ke0vouxean```

ensuite on va passer ```getflag``` a la session ```flag08``` pour trouver le flag : ```25749xKZ8L7DkSCwJkT9dyv6f```