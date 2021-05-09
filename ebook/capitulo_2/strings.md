# Strings

Python é uma linguagem bastante reconhecida pelos recursos que oferece para processamento de textos. Strings são conjuntos de caracteres definidos **entre aspas simples ou duplas**. Para declarar strings com mais uma linha, usa-se três aspas em sequência.

```
"String de uma única linha"

'''
String com mais de
uma linha
'''
```
É possível utilizar os seguintes operadores aritméticos para manipular as strings:

|Operador | Explicação | Exemplo| Saída
|--|--|--|--
|Concatenação (+) | Cria uma nova string com a concatenação das duas strings passadas | "Amo" + "Python" | "AmoPython"
|Repetição (*) | Cria uma nova string com n repetições da string original | "PyLadies <3 "*3 | "PyLadies <3 PyLadies <3 PyLadies <3 "
|Indexação ([]) | Seleciona um caracter de uma string (inicia em 0) | "PyLadies"[1] | "y"

Também é possível manipulá-las usando os índices de seus caracteres:

![image](../assets/string-indice.png)

Abaixo alguns dos métodos mais utilizados:

|Operador | Explicação | Exemplo| Saída
|--|--|--|--
|Fatiamento ([::]) | Seleciona substring iniciando na posição de início, até o fim (não incluso), com passo n. Se não for definido início, iniciará no primeiro caracter. Se não for definido fim, irá até o último caracter. Se não for definido um passo, será 1. | "Com passo negativo"[8:3:-1] | "ossap"
|Verificação ( in) | Verifica se há determinada substring na string original | "Ladies" in "PyLadies Brasil" |True
|Verificação negativa (not in) |Verifica se não há uma substring na string original |"Py" not in "Python" |False
|Tamanho (len) |Retorna o tamanho de uma string |len("PyLadies Brasil") |15
|"string".startswith("substring") |Retorna verdadeiro se a string inicia com a substring passada, senão falso |"PyLadies Macaé".startswith( "Py") |True
|"string".endswith( "substring") |Retorna verdadeiro se a string termina com a substring passada, senão falso |"PyLadies Natal".endswith( "Recife") |False
|"string".replace("antigo", "novo", limite_opcional) |Substitui a string original pela nova string, com limite de substituições (se não houver, substitui todas as ocorrências) |"PyLadies Natal e Natal".replace("Natal", "Recife", 1) |"PyLadies Recife e Natal"
|"string".count( "substring") |Retorna número de ocorrências da substring na string original |"PyLadies amam Python".count("Py") |2
|"string".index("substring") |Retorna a posição onde a substring inicia na string original (buscando da esquerda para a direita) ou ValueError se não for encontrada |"PyLadies São Carlos".index("São") |9
|"string".rindex( "substring") |Retorna a posição onde a substring inicia na string original (buscando da direita para a esquerda) ou ValueError se não for encontrada |"PyLadies amam Python".rindex( "Py") |14
|"string".find( "substring") |Retorna a posição onde a substring inicia na string original (buscando da esquerda para a direita) ou -1 se não for encontrada |"PyLadies São Carlos".find( "Brasil") |-1
|"string".rfind( "substring") |Retorna a posição onde a substring inicia na string original (buscando da direita para a esquerda)  ou -1 se não for encontrada |"PyLadies Paraíba dominando o mundo".rfind( "ndo") |31
|"string".isalnum() |Retorna verdadeiro se a string é composta exclusivamente por letras e dígitos |"Mudar123".isalnum() |True
|"string".isalpha() |Retorna verdadeiro se a string é composta exclusivamente por letras |"PyLadies Manaus".isalpha() |False
|"string".isdigit() |Retorna verdadeiro se a string é composta exclusivamente por digitos |"10".isdigit() |True
|"string".isspace() |Retorna verdadeiro se a string é composta exclusivamente por caracteres espaço |"\n\t ".isspace() |True
|"string".capitalize() |Seta a primeira letra como maiúscula e as demais minúsculas |"pYtHon é a melhor LINGUAGEM <3".capitalize() |"Python é a melhor linguagem <3"
|"string".title() |Seta toda primeira letra de cada palavra maiúscula e as demais minúsculas |"pyladies brasil".title() |"Pyladies Brasil"
|"string".swapcase() |Inverte os cases de todas as letras |"pYlADIES bRASIL".swapcase() |"PyLadies Brasil"
|"string".lower() |Seta todas as letras minúsculas |"Python é LINDOO!".lower() |"python é lindoo!"
|"string".upper() |Seta todas as letras maiúsculas |"amo python!".upper() |"AMO PYTHON!"
|"string".center( numero, "caracter opcional") |Centraliza uma string entre N caracteres, preenchendo os demais com o caracter passado (se não for passado, será espaço) |"Py <3".center(9, "*") |"**Py <3**"
|"string".zfill() |Preenche com zeros à esquerda até completar n caracteres |"Py".zfill(5) |"000Py"
|"string".rjust( numero, "caracter opcional") |Alinha n caracteres à direita preenchendo a string com o caracter passado (ou espaços, na ausência deste) |"Py".rjust(5, "-") |"Py---"
|"string".ljust( numero, "caracter opcional") |Alinha n caracteres à esquerda preenchendo a string com o caracter passado (ou espaços, na ausência deste) |"Py".rjust(5, "+") |"+++Py"
|"string".split( "string de separação opcional") |Divide a string em várias substrings a partir de uma string de separação. Se não for passada string de separação, usará espaços. |"PyLadiesPyBar".split("Py") |['', 'Ladies', 'Bar']
|"string".strip( "string opcional") |Remove substrings do início e final da string. Se não for passada string, removerá espaços em branco. |"PyPyLadies PyLadiesPy".strip("Py") |"Ladies PyLadies"

## Split - Entrada de dados

Ainda se lembra que Python lê **dados de entrada como uma única linha de texto**? Por exemplo: como você extrairia um nome e uma idade digitados numa mesma linha?

Como todas as entradas do Python são consideradas textos, portanto strings, **você pode utilizar todas as funções de string sobre elas**, inclusive a função split()!

```
nome, idade = "Ana 27".split()
```

Você pode criar quantas variáveis sejam necessárias para armazenar seus dados. Lembre-se de **converter** o que for necessário depois!


{% include "../templates/lista_exercicios.md" %}
