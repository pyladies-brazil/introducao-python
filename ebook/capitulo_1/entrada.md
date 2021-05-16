# Entrada

Python considera **todas as entradas como texto, cada linha digitada como um único conteúdo contínuo**. Para declarar uma entrada, deve-se usar o comando:

```python
input("Texto opcional que será exibido ao usuário")
```

## Conversão de tipo de dados

| Tipo                          | Comando de conversão |
| ----------------------------- | -------------------- |
| Booleano (`bool`)             | `bool(variavel)`     |
| Inteiro (`int`)               | `int(variável)`      |
| Real (`float`)                | `float(variável)`    |
| Texto (`str`)                 | `str(variável)`      |
| Números complexos (`complex`) | `complex(variável)`  |

Suponha que você digite numa mesma linha seu nome, sua idade e grupo PyLadies de origem, Python reconhecerá tudo como uma mesma entrada de texto, sem divisões. Caso você deseje um tipo diferente, será necessário converter explicitamente. Exemplo de utilização:

```python
comunidade = int(input('Digite o número de PyLadies: '))
```

Mas há uma restrição, a conversão só pode ser aplicada a um valor por vez! E em Python, todos os valores digitados em uma mesma linha serão considerados o mesmo texto, portanto por hora use um valor por linha, ensinaremos como contornar esse problema em breve!

{% include "../templates/lista_exercicios.md" %}