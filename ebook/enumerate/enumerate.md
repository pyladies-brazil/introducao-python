# Enumerate

Enumerate cria um iterável onde cada elemento é uma tupla com a posição do elemento original da lista e o próprio elemento, respectivamente.

```
capitulos = ["PyLadies Natal", "PyLadies Recife"]
for capitulo in enumerate(capitulos): # usando uma única 
   print(capitulo)                # variável de controle

>>(0, 'PyLadies Natal')
>>(1, 'PyLadies Recife')
```

```
capitulos = ["PyLadies Natal", "PyLadies Recife", "PyLadies DF", "PyLadies São Carlos", "PyLadies Rio"]

for indice, capitulo in enumerate(capitulos):   # com duas
   print(indice, capitulo)         # variáveis de controle

>> 0 PyLadies Natal
>> 1 PyLadies Recife
>> 2 PyLadies DF
>> 3 PyLadies São Carlos
>> 4 PyLadies Rio
```
{% include "../templates/lista_exercicios.md" %}