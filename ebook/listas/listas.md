# Listas

É uma sequência de valores organizados entre colchetes [ ].

Esses dados podem ser de diferentes tipos: inteiros, floats, strings e inclusive outras listas. Exemplos:

```
dezenas = [10, 20, 30, 40]

comunidades = ['PyLadies Sul de Minas', 'PyLadies Paraíba', 'PyLadies Sorocaba',  ' PyLadies São Carlos',  ' PyLadies Mato Grosso']

lista_vazia = []
```

Os elementos de uma lista podem ser acessados pelo índice:

```
cores = ['amarelo', 'azul', 'branco', 'dourado']
```

Lembrando que a primeira posição de uma lista em Python é a posição 0:

```
cores[0]
>>> 'amarelo'

cores[2]
>>> 'branco'
```

Além de ser possível acessar cada elemento da lista pelo índice, é possível, inserir, alterar e deletar.

Listas são mutáveis, ou seja, é possível alterar seus elementos: adicionando, removendo e/ou substituindo-os com os métodos abaixo:

| Operador| Explicação| Exemplo| Saída
|--|--|--|--
| Concatenação (+)| Cria uma nova lista com a concatenação das listas passadas| natal = ["Débora", "Clara"]<br /><br />sao_carlos = ["Marília", "Belém"]<br /><br /> ladies = natal + sao_carlos| ['Débora', 'Clara', 'Marília', 'Belém']
| Repetição (*)| Cria uma nova lista com n concatenações da lista passada| pyladies = ["PyBar", "Papo", "GTs"]<br /><br /> vida = pyladies * 3| ['PyBar', 'Papo', 'GTs', 'PyBar', 'Papo', 'GTs', | 'PyBar', 'Papo','GTs']
| Indexação ([])| Retorna um elemento de uma lista. O primeiro índice é o zero.| capitulos = ['Recife', 'São Carlos', 'Salvador', 'Macaé']<br /><br /> capitulos = [1]| São Carlos
| elemento **in** lista| Verifica se um elemento está presente em uma lista.| letras = ['P', 'Y', 'L', 'A', 'D', 'I', 'E', 'S']| 'Y' in letras| True
| elemento **not in** lista| Verifica se um elemento está ausente em uma lista.| letras = ['P', 'Y', 'L', 'A', 'D', 'I', 'E', 'S']| 'Y' not in letras| False
| Fatiamento ([:])| Retorna um subconjunto de elementos de uma lista. Final não inclusivo. Passo é parâmetro opcional que se não passado é 1 por default. Os parâmetros default de início e fim são o início e fim da lista, respectivamente.| capitulos = ['Recife', 'São Carlos', 'Salvador', 'Macaé', 'Manaus', 'Rio']<br /><br /> capitulos[1:3]<br /><br /> capitulos[::2]| <br /><br /><br /><br /><br /><br /><br /><br />['São Carlos', 'Salvador']<br /><br /> ['Recife', 'Salvador', 'Manaus']
| lista.append(elemento)| Adiciona um novo elemento ao final da lista.| inteiros = [1, 2, 3]<br /><br /> inteiros.append(10)| [1, 2, 3, 10]
| lista.insert(posicao, elemento)| Adiciona um novo elemento numa determinada posição da lista. Todos os elementos daquela posição em diante são deslocados uma posição para frente.| disciplinas = ["SO", "IA"]<br /><br /> disciplinas.insert(0, "CAP")| ['CAP', 'SO', 'IA']
| lista.remove(elemento)| Remove o primeiro elemento especificado encontrado na lista.| nomes = ['Ceci', 'Bia']<br /><br /> nomes.remove('Ceci')| ['Bia']
| lista.count(elemento)| Conta quantas vezes o elemento especificado aparece na lista. Retorna zero se o elemento não pertencer à lista.| frutas = ["uva", "caju", "uva", "maçã"]<br /><br /> frutas.count("uva")| 2
| lista.index(elemento)| Retorna a posição da primeira ocorrência do elemento especificado. Caso não seja encontrado, um erro será lançado.| tamanhos = ["XP", "M", "GG", "XG"]<br /><br /> tamanhos.index("GG")| 2
| lista.pop(posição)| Remove e retorna o elemento da posição especificada. Caso não seja especificada uma posição, removerá o último elemento da lista.| inteiros = [5, 6, 7, 8, 9, 10]<br /><br /> inteiros.pop(2)| 7
| lista.sort()| Caso os elementos tenham implementação do operador menor (<) e sejam comparáveis (normalmente, de mesmo tipo), Python oferece uma função pronta para ordenar seu conteúdo. Caso os elementos não sejam comparáveis, um erro será lançado.| cores = ['rosa', 'verde', 'lilás', 'azul']<br /><br /> cores.sort()| ['azul', 'lilás', 'rosa', 'verde']
| lista.reverse()| Inverte as posições dos elementos de uma lista. O último passa a ser o primeiro, o penúltimo passa a ser o segundo e assim por diante.| coffee = ['café','bolo', 'refri']<br /><br /> coffee.reverse()| ['refri', 'bolo', 'café']
| list(objeto_iterável)| Cria uma lista a partir de um objeto iterável, por exemplo, uma string. Se não for objeto iterável, um erro será lançado| palavra = "Python"<br /><br /> list(palavra)| ['P', 'y', 't', 'h', 'o', 'n']
| len(lista)| Retorna o tamanho de uma lista. Funciona para qualquer objeto iterável. Se não for um objeto iterável, um erro será lançado.| ladies = ["Nathália", "Karol", "Juliana"]<br /><br /> len(ladies)| 3
| lista.extend(lista)| Insere os elementos da lista passada por parâmetro no final da lista original. É uma concatenação.| inteiros = [1, 2, 3]<br /><br /> inteiros.extend([4, 5, 6])| [1, 2, 3, 4, 5, 6]
| sum(lista_de_numeros)| Retorna a soma de uma lista de números. Só funciona com números.| inteiros = [16, -40, -15, 38, -4, 25]<br /><br /> sum(inteiros)| 20
| max(lista_ordenavel)| Retorna o elemento de valor máximo. A lista de entrada precisa permitir relações de ordem.| inteiros = [16, -40, -15, 38, -4, 25]<br /><br /> max(inteiros)| 38
| min(lista_ordenavel)| Retorna o elemento de valor mínimo. A lista de entrada precisa permitir relações de ordem| inteiros = [16, -40, -15, 38, -4, 25]<br /><br /> min(inteiros)| -40

Exemplo de como utilizar algumas das funções apresentadas:

```
coffee = ['refri', 'bolinha de queijo', 'bolo', 'coxinha']

coffee.append('café')
coffee.insert(0, 'água')
coffee.remove('refri')
```

Resultado esperado:

```
['água', 'bolinha de queijo', 'bolo', 'coxinha', 'café']
```

Para percorrer uma lista toda podemos acessar os elementos diretamente ou utilizar os índices para acessá-los:

```
# acessando diretamente
for elemento in lista
   elemento

# acessando através dos índices
for i in range(len(lista)):
   lista[i]
```

**Atenção!**

Acessando diretamente você pode apenas percorrer a lista, e visualizar seu conteúdo, acessando pelos índices você pode, além disso, alterar o conteúdo de uma posição.

```
ladies = ["Bia", "Ceci", "Débora"]
ladies[2] = "Débora"
```

A lista resultante será:

```
['Bia', 'Ceci', 'Débora']
```

{% include "../templates/lista_exercicios.md" %}
