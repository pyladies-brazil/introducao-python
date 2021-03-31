# Continue

E se você não quiser sair do loop, mas apenas “pular” alguns comandos? Use a cláusula **continue**! Ela permite que, ainda no meio do laço, você passe para a próxima iteração.

```
i = 1
while (i <= 10):
   i += 1
   if i == 2:
     continue
   print(f'Oii, Lady {i}!')
```

```
for i in range(1, 11):
   if i == 2:
       continue
   print(f'Oii, Lady {i}!')
```

{% include "../templates/lista_exercicios.md" %}