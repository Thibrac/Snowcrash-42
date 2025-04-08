Dans ce niveau on a aucun fichier ni prog mais on peut fouiller ```getflag```

On le disas dans gdb mais il y a une protection ```ptrace``` donc il faut la contourner

```sh
catch syscall ptrace
commands 1
set ($eax) = 0
continue
end
```

Une fois contourne on peut acceder au reste du code decompile et on voit les comparaisons de ```getuid()```

On assigner la valeur '3014' a $eax au moment de la comparaison car on veut le flag14

On run le continue le programme qui nous donne le flag ```7QiHafiNa3HVozsaXkawuYrTstxbpABHD8CPnHJ```