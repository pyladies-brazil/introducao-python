# Map

Map é uma função de ordem superior que aplica uma função sobre cada elemento de um iterável. Você pode utilizá-la para aplicar as mais diversas funções, mas inicialmente iremos utilizá-la principalmente realizar conversões! Até o momento, você fazia isso:

```
nota1, nota2, nota3 = "9.5 8 10".split()
nota1 = float (nota1)
nota2 = float (nota2)
nota3 = float (nota3)
media = (nota1 + nota2 + nota3) / 3
```

Com map, você pode simplificar as conversões em uma única linha:

```
notas = "9.5 8 10".split()
notas = map(float, notas)
media = sum(notas) / 3
```

{% include "../templates/lista_exercicios.md" %}