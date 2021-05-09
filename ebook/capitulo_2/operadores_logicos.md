# Operadores Lógicos

Os operadores lógicos (também conhecidos como operadores booleanos) são utilizados para auxiliar a criar estruturas de decisão.

Em Python eles são escritos por extenso (em inglês):

| Operador Booleano | Python |
| ----------------- | ------ |
| e                 | `and`  |
| ou                | `or`   |
| negação           | `not`  |


## Precedência

Precedência indica qual o operador calculado primeiro, listadas por ordem de prioridade.
Todas as expressões serão avaliadas antes dos operadores lógicos.

| Operador | Nome       |
| -------- | ---------- |
| `()`     | Parênteses |
| `not`    | Negação    |
| `and`    | E          |
| `or`     | Ou         |

Exemplos:

|Exemplo de entrada                                                  |Exemplo de saída|
|--------------------------------------------------------------------|----------------|
| True and False                                                     | False          |
| num = 100<br /> nume % 2 == 0 and num % 5 == 0 and 0 <= num <= 100 | True           |
| 1+2+3+4+5+6 == 7*(7-1)//2 and 7*(7-1)//2 % 3 == 0                  | True           |
| num = 25<br /> num % 5 == 0 or num % 2 == 0 and 10 <= num <= 20    | True           |
| num = 36<br /> num % 4 == 0 and num % 6 == 0 and not num % 8 == 0  | True           | 

Os valores considerados falsos em Python são: 

| Constantes | Números zero  | Sequências vazias |
| ---------- | ------------- | ----------------- |
| `False`    | `int (0)`     | `list ( [] )`     |
| `None`     | `float (0.0)` | `tuple ( () )`    |
|            |               | `dict ( {} )`     |
|            |               | `set ( )`         |
|            |               | `str ( "" )`      |
|            |               | `range ( 0 )`     |


{% include "../templates/lista_exercicios.md" %}