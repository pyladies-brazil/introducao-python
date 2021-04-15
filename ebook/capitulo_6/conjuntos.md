# Conjuntos

Segundo a documentação oficial de Python, um conjunto é:

“Um objeto set é uma coleção não ordenada de objetos hasheáveis distintos.”

Em Python, um conjunto é representado por valores entre chaves (ex.: int, string ou qualquer objeto cuja classe implemente o método `__hash__`) .

**Obs:** cuidado para não confundir com dicionários.

Declarando um conjunto vazio:

```
conjunto_vazio = set()
```

Criando um conjunto a partir de uma lista:

```
novo_conjunto = set(lista)
```

Criando um conjunto com valores:

```
novo_conjunto = {1, 2, 3, 4, 5}
```

Métodos mais usados:

| Operador| Explicação| Exemplo| Saída
|--|--|--|--
| elemento **in** conjunto| Verifica se um elemento pertence ao conjunto.| locais = {"Goiânia", "Nova Iguaçu", "Sul de Minas", "Sergipe"}<br /><br /> "Sergipe" in locais| True
| elemento **not in** conjunto| Verifica se um elemento não pertence ao conjunto.| locais = {"Goiânia", "Nova Iguaçu", "Sul de Minas", | "Sergipe"}<br /><br /> "Goiânia" not in locais| False
| len( conjunto)| Retorna o tamanho do conjunto| locais = {"Goiânia", "Nova Iguaçu", "Sul de Minas", "Sergipe"}<br /><br /> len(locais)| 4
| conjunto.add( elemento)| Adiciona um elemento a um conjunto.| locais = {"Parnaíba", "Rosana", "Blumenau"}<br /><br /> locais.add("Macaé")| {'Blumenau', 'Macaé', 'Parnaíba', 'Rosana'}
| conjunto.remove( elemento)| Remove um elemento especificado de um conjunto e retorna None. Se não houver o elemento, um erro será lançado| locais = {'Blumenau', 'Macaé', 'Parnaíba', 'Rosana'}<br /><br /> locais.remove('Macaé')| {'Blumenau', 'Parnaíba', 'Rosana'}
| conjunto.pop()| Retorna e exclui um elemento do conjunto. Não se determina o elemento escolhido, o algoritmo escolhe.| locais = {'Blumenau', 'Macaé', 'Parnaíba'}<br /><br /> locais.pop()| 'Blumenau'
| conjunto.clear()| Remove todos os elementos de um conjunto.| locais = {'Blumenau', 'Macaé', 'Parnaíba'}<br /><br /> locais.clear()| {}
| conjunto.update( conjunto)| Adiciona os elementos do conjunto passado no conjunto original.| locais = {'Blumenau', 'Macaé'}<br /><br /> locais.update('Rosana')| {'Blumenau', 'Macaé', 'Parnaíba'}
| conjunto.issubset(conjunto)| Retorna verdadeiro se o conjunto está contido no conjunto passado.| brasil = {"Paraíba", "Caxias do Sul", "Florianópolis", "São José dos Campos", "Manaus", "Sorocaba"}<br /><br /> sp = {"Sorocaba", "São José dos Campos"}<br /><br /> sp.issubset(brasil)| True
| conjunto.issuperset( conjunto)| Retorna verdadeiro se o conjunto  contém o conjunto passado.| brasil = {"Paraíba", "Caxias do Sul", "Florianópolis", "São José dos Campos", "Manaus", "Sorocaba"}<br /><br /> sp = {"Sorocaba", "São José dos Campos"}<br /><br /> brasil.issuperset(sp)| True
| conjunto.union( conjunto)| Retorna um novo conjunto com a união dos elementos dos dois conjuntos.| brasil = {"Maceió", "Ribeirão Preto", "Teresina"}<br /><br /> rs = {"Porto Alegre"}<br /><br /> rs.union(brasil)| {"Maceió", "Porto Alegre", "Ribeirão Preto", "Teresina"}
| conjunto.isdisjoint( conjunto)| Retorna verdadeiro se os conjuntos são disjuntos, isto é, se eles não tem nenhum elemento em comum.| brasil = {"Maceió", "Ribeirão Preto", "Teresina"}<br /><br /> rs = {"Porto Alegre"}<br /><br /> rs.isdisjoint(brasil)| True
| conjunto. intersection(conjunto)| Retorna um novo conjunto com os elementos comuns entre o primeiro e segundo conjunto. É a operação inversa do symmetric difference.| multiplos_6 = {12, 18, 24}<br /><br /> multiplos_4 = {8, 12, 16, 20, 24}<br /><br /> multiplos_6.intersection(multiplos_4)| {12,24}
| conjunto. intersection_update( conjunto)| Retira do primeiro conjunto os elementos que não estão na intersecção entre os dois conjuntos. É a operação inversa do symmetric difference update.| multiplos_6 = {12, 18, 24}<br /><br /> multiplos_4 = {8, 12, 16, 20, 24}<br /><br /> multiplos_6.intersection_update(multiplos_4)| {12,24}
| conjunto. difference(conjunto)| Retorna um novo conjunto com os elementos do primeiro conjunto que não estão contidos no segundo.| multiplos_6 = {12, 18, 24}<br /><br /> multiplos_4 = {8, 12, 16, 20, 24}<br /><br /> multiplos_6.difference(multiplos_4)| {18}
| conjunto. difference_update( conjunto)| Retira os elementos da intersecção dos dois conjuntos do primeiro conjunto.| multiplos_6 = {12, 18, 24}<br /><br /> multiplos_4 = {8, 12, 16, 20, 24}<br /><br /> multiplos_6.difference_update(multiplos_4)| {18}
| conjunto. difference(conjunto)| Retorna um novo conjunto com os elementos únicos dos dois conjuntos. É a operação inversa do intersection.| multiplos_6 = {12, 18, 24}<br /><br /> multiplos_4 = {8, 12, 16, 20, 24}<br /><br /> multiplos_6.symmetric_difference(multiplos_4)| {8, 16, 18, 20}
| conjunto.symmetric_difference_update( conjunto)| Atualiza o primeiro conjunto com os elementos únicos dos dois conjunto. É a operação inversa do intersection_update.| multiplos_6 = {12, 18, 24}<br /><br /> multiplos_4 = {8, 12, 16, 20, 24}<br /><br /> multiplos_6.symmetric_difference_update(multiplos_4)| {8, 16, 18, 20}

{% include "../templates/lista_exercicios.md" %}