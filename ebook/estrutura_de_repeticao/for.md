# For

Executam um conjunto de comandos repetidamente satisfazendo a determinada condição.

As duas estruturas de repetição mais comuns são **for** e **while**.Nesse capítulo trataremos do **for**.

**Sintaxe:**
```
for valor in sequência:
   código
```

**Exemplo:**
```
for i in range(1, 11):
   print(f'Oii, Lady {i}!')
```

## For... else
Antes de seguir nessa seção, sugerimos a leitura dos assuntos [Break](../break_e_continue/break.md) e [Continue](../break_e_continue/continue.md).

```
for (valor na sequência):
   comandos
else:
   comandos
```

```
for i in range(1, 11):
  if i == 5:
    break
   print(f'Oii, Lady {i}!')
else:
  print(f'Bem vindas!')
```

{% include "../templates/lista_exercicios.md" %}