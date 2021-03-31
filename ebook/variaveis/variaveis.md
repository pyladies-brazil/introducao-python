# Variáveis

De forma simplificada, variável é um nome que associamos a um valor ou expressão (informação).

**Sintaxe:** 
```
nome_da_variavel = conteudo
doce = 'brigadeiro'
```

**Convenções para nomenclatura:**

- usar **algarismos, letras ou \_**
- **nunca** começar com um algarismo
- **não usar palavras reservadas** do Python, como if, while, etc.
  
## Declaração e atribuição

Python é uma **linguagem dinâmica** e não é necessária nenhuma declaração e especificação prévia para utilização de uma variável, ela será declarada durante sua **primeira atribuição**. 

Python aceita atribuições encadeadas e mais de uma atribuição por vez usando vírgula.

Por ser uma linguagem dinâmica, as variáveis **não são associadas a tipos de dados**, seu tipo associado é diretamente o tipo de dado que armazena naquele momento, e pode variar no decorrer do código.

|Exemplo de entrada |Exemplo de saída
|--|--
|a = 10 |>>> a <br/>10
|a = 10 <br />a = "PyLadies" |>>> a <br />'PyLadies'
|inicio = fim = 0 |>>> inicio <br />0 <br />>>> fim <br />0
|capitulo, local = "PyLadies Floripa", "Florianópolis"|>>> capitulo <br />'PyLadies Floripa' <br />>>> local <br />'Florianópolis'

{% include "../templates/lista_exercicios.md" %}