# While

Executam um conjunto de comandos repetidamente satisfazendo a determinada condição.

As duas estruturas de repetição mais comuns são **for** e **while**. Nesse capítulo trataremos do **while**.

**Sintaxe:**
```
while condição:
   comandos
```

**Exemplo:**
```
i = 1
while i <= 10:
   print(f'Oii, Lady {i}!')
   i += 1
```

## While... else

Antes de seguir nessa seção, sugerimos a leitura dos assuntos [Break](../capitulo_4/break.md) e [Continue](../capitulo_4/continue.md).

```
while (condição):
   comandos
else:
   comandos
```

```
i = 0
while (i <= 10):
  i += 1
  if i == 5:
    break
  print(f'Oii, Lady {i}!')
else:
  print('Bem vindas!')
```

{% include "../templates/lista_exercicios.md" %}