# Zip

Zip cria um iterável onde cada enésimo elemento é uma tupla com os respectivos enésimos elementos das listas utilizadas para gerá-lo. 

Se uma lista for maior que a outra, zip terá o número de elementos da lista menor. 

É possível iterar com uma única variável correspondente à tupla criada pelo zip, ou com o número de variáveis correspondente ao número de listas.

```
capitulos = ["PyLadies Natal", "PyLadies Recife", "PyLadies DF", "PyLadies São Carlos", "PyLadies Rio"]

ladies = ["Débora", "Ana Cecília", "Tânia", "Ana Dulce"]

for pyladies in zip(capitulos, ladies): # usando uma única
   print(pyladies)                # variável de controle

>>('PyLadies Natal', 'Débora')
>>('PyLadies Recife', 'Ana Cecília')
>>('PyLadies DF', 'Tânia')
>>('PyLadies São Carlos', 'Ana Dulce')
```

```
capitulos = ["PyLadies Natal", "PyLadies Recife", "PyLadies DF", "PyLadies São Carlos", "PyLadies Rio"]

ladies = ["Débora", "Ana Cecília", "Tânia", "Ana Dulce"]

for capitulo, lady in zip(capitulos, ladies): # com duas
  print(f"{lady} da {capitulo}") # variáveis de controle

>>Débora da PyLadies Natal
>>Ana Cecília da PyLadies Recife
>>Tânia da PyLadies DF
>>Ana Dulce da PyLadies São Carlos
```

{% include "../templates/lista_exercicios.md" %}