On a dans ce niveau un executable ```level13```

On va le disas et voir qu'il y a une comparaison ```0x0804859a <+14>:	cmp    $0x1092,%eax```

On va passer apres la cmp et changer le "ZF" (zero flag) avec ```set $eflags |= (1 << 6)```

On continue l'execution du prog et la flag apparait ```2A31L79asukciNyi8uppkEuSx```