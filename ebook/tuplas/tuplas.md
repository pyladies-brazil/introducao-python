# Tuplas

Tuplas são estruturas de dados iteráveis imutáveis.

Geralmente, têm seus itens delimitados por parênteses , mas também podem ser declaradas simplesmente por separar os itens com vírgulas, com exceção de quando se quer criar uma tupla vazia.

```
tupla1 = (1,2,3)
tupla2 = 1,2,3
tupla_vazia = ()

>>> print(tupla1, tupla2, tupla_vazia)
(1,2,3) (1,2,3) ()
```
Métodos mais usados:

| Operador| Explicação| Exemplo| Saída
|--|--|--|--
| Concatenação (+)| Cria uma nova tupla unindo duas tuplas.| recife = ("Juliana", "Ana Cecília")<br /><br /> rio = ("Bianca", "Thais")<br /><br /> recife_rio = recife + rio| ('Juliana', 'Ana Cecília', 'Bianca', 'Thais')
| Repetição (*)| Cria uma nova tupla concatenando n repetições da tupla passada.| produtoras = ("dands", "gio", "ceci")<br /><br /> papo_entre_pyladies = produtoras * 3| ('dands', 'gio', 'ceci', 'dands', 'gio', 'ceci', 'dands', 'gio', 'ceci')
| Indexação ([])| Seleciona um elemento de uma tupla.| sao_carlos = ("Amanda", "Ana Dulce", "Belém", "Juliana", "Teclado")<br /><br /> sao_carlos[2]| Belém
| Fatiamento ([:])| Cria uma nova tupla com um subconjunto de elementos de uma tupla, baseado nos parâmetros inicio, fim e passo, cujos respectivos defaults são zero, tamanho da tupla e um.| ladies = ("Ana Paula", "Larissa", "Maria Paula", "Pâmela", "Renata")<br /><br /> ladies[1:3]<br /><br /> ladies[2::2]| <br /><br />('Larissa', 'Maria Paula')<br /><br /> ('Maria Paula', 'Renata')
| elemento **in** tupla| Verifica se um elemento está presente em uma tupla.| recife = ("Ana Cecília", "Chaina", "Juliana", "Amanda", "Carolina")<br /><br /> "Chaina" in recife| True
| elemento not **in** tupla| Verifica se um elemento está ausente em uma tupla.| produtoras = ("Ana Cecília", "Ana Dulce", "Belém", "Chaina", "Maria Paula", "Alynne", "Maria Paula", "Renata", "Larissa")<br /><br /> "Maria Paula" not in produtoras| False
| tupla.count(elemento)| Conta quantas vezes o elemento especificado aparece na tupla. Retorna zero se o elemento não pertencer à tupla.| frutas = "uva", "caju", "uva", "maçã", "açaí"<br /><br /> frutas.count("uva")| 2
| tupla.index(elemento)| Retorna a posição da primeira ocorrência do elemento passado. Se não for encontrado, um erro será lançado.| tamanhos = ("XP", "M", "GG", "XG")<br /><br /> tamanhos.index("GG")| 2
| len(lista)| Retorna o tamanho de uma tupla. Funciona para qualquer objeto iterável. Se não for um objeto iterável, um erro será lançado.| ladies = ("Renata", "Maria Paula", "Belém")<br /><br /> len(ladies)| 3

**Atenção**

Tuplas podem conter objetos mutáveis, como listas.

Ao inserir um novo número na lista dentro da tupla (posição 0), não alteramos em nada a tupla, já que as referências que ela guarda são as mesmas! Apenas modificamos a lista dentro dela, mas sem mudar o identificador.

```
>>> tupla = ([1,2,3],[4,5])
>>> id(tupla)
140393279659016
>>> tupla[0].append(4)
>>> tupla
([1,2,3,4], [4,5])
>>> id(tupla)
140393279659016
```

Geralmente, vemos as listas possuindo itens todos do mesmo tipo, enquanto tuplas são mais encontradas obtendo itens de diversos tipos, mas isso não significa que listas não possam ser heterogêneas e tuplas homogêneas!

“As listas são destinadas a serem sequências homogêneas, enquanto que os Tuplas são estruturas de dados heterogêneas.” Phillip J. Eby

{% include "../templates/lista_exercicios.md" %}