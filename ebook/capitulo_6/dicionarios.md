# Dicionários

Dicionário é um objeto que relaciona uma chave a um valor.

A chave é o que indexa um dicionário, isto é, ela corresponde ao conceito de índice. 

Desta forma, em vez de ter posições 0, 1, 2, 3 e assim por diante, podemos ter posições com os valores que desejamos, como “azul”, “amarelo” e “vermelho”. 

Por se tratarem de índices, uma consequência direta é que as chaves de um dicionários precisam ser únicas, e, caso você declare mais de uma vez a mesma chave, o valor será sobreposto.

```
dicionario_vazio = {}
camiseta = {"M":12, "G": 10, "GG":10}
dados = {
   "grupo": "PyLadies São Carlos",
   "fundação":2014,
   "integrantes": 37
}
alunas_curso = {"Ana": "BCC", "Amanda": "EnC"}
alunas_curso["Belém"] = "Biotec"
```

Para criar um dicionário vazio, atribua abre e fecha chaves à variável:
dicionario = {}

Para adicionar uma nova chave e seu respectivo valor a um dicionário existente, ou atualizar um valor de uma chave existente, atribua o novo valor ao dicionário na “posição” da nova chave:

```
dicionario['chave'] = 'valor'
```

Para acessar um valor, deve-se passar a chave:

```
dicionario['chave']
```

| Operador| Explicação| Exemplo| Saída
|--|--|--|--
| chave **in** dicionario| Verifica se uma chave existe em um dicionário.| camisetas_dg = {"P": 3, "M": 1}<br /><br /> "M" in camisetas_dg| True
| chave **not in** dicionario| Verifica se uma chave não existe em um dicionário.| camisetas_dg = {"P": 3, "M": 1}<br /><br /> "M" not in camisetas_dg| False
| del (dicionario [chave])| Deleta uma chave e seu respectivo valor de um dicionário.| fundacao = {2013: ["Natal"], 2014: ["Distrito Federal", "Recife", "São Carlos"], 2021:[]}<br /><br /> del (fundacao[2014])| {2013: ['Natal'], 2021: []}
| dicionario.keys()| Retorna um objeto iterável com todas as chaves de um dicionário.| brindes = {"caneca": 100, "bottom": 500 , "stickers": 1000} <br /><br />for brinde in brindes.keys():<br />....print(brinde)| caneca<br /> bottom<br /> stickers
| dicionario.values()| Retorna um objeto iterável com todos os valores de um dicionário.| brindes = {"caneca": 100, "bottom": 500 , "stickers": 1000}<br /><br /> for qtd in brindes.values():<br />....print(qtd)| 100<br /> 500<br /> 1000
| dicionario.items()| Retorna um objeto iterável com um tupla contendo chave e valor de um dicionário. Pode ser iterado com uma variável, que assumirá o valor da tupla inteira, ou duas, onde chave e valor terão variáveis respectivas.| brindes = {"caneca": 100, "bottom": 500 , "stickers": 1000}<br /><br /> for item in brindes.items():<br />....print(item)<br /><br /> for brinde, qtd in brindes.items():<br />....print(f"{qtd} unidades de {brinde}")| ('caneca', 100)<br /> ('bottom', 500)<br /> ('stickers', 1000)<br /> 100 unidades de caneca<br /> 500 unidades de bottom<br /> 1000 unidades de stickers
| dicionario.copy()| Retorna um novo dicionário, com uma cópia real do objeto. Se você fizer dict1 = dict2, ele criará apenas uma referência.| brindes = {"caneca": 100, "bottom": 500 , "stickers": 1000}<br /><br /> campanha = brindes.copy()| {'bottom': 500, 'caneca': 100, 'stickers': 1000}
| dicionario.clear()| Deleta todo o conteúdo do dicionário e retorna um dicionário vazio.| alunas = {"Introdução à Programação com Python": 60, "Introduçãão a Python": 57, "Python Intermediário": 79}<br /><br /> alunas.clear()| {}
| dicionario.get(chave)| Retorna o valor de uma dada chave, ou None caso ela não exista. É aconselhável o uso em vez de acesso direto em casos onde uma chave possa não existir, pois no acesso direto causaria erro.| coffee = {"bolo": 10, "refri": 6, "café": 3, "coxinha": 300, "pão de queijo": 300}<br /><br /> coffee.get("pão de queijo")| 300
| dicionario.pop(chave)| Retorna o valor de uma dada chave e exclui todo o elemento do dicionário.| camisetas_dg = {"P": 3, "M": 1}<br /><br /> camisetas_dg.pop("P")| 3
| dicionario.popitem()| Retorna um elemento do dicionário e o exclui do dicionário. Não é possível escolher qual elemento será retornado.| camisetas_dg = {"P": 3, "M": 1}<br /><br /> camisetas_dg.popitem()| ('M', 1)
| dicionario.update( dicionario)| Atualiza elementos existentes ou adiciona elementos caso estes não existam num dicionário base.| camisetas_dg = {"P": 3, "M": 1}<br /><br /> camisetas_dg.update({"G": 3, "GG": 2})| {'G': 3, 'GG': 2, 'M': 1, 'P': 3}

Para iterar sobre dicionários usando a chave como acesso:

```
for chave in dicionario:
   dicionario[chave]
```

Para iterar sobre os conjuntos chave valor de uma vez:

```
for item in dicionario.items():
   item # a saída é uma tupla, com elementos chave e valor
for chave, valor in dicionario.items():
   chave, valor # ou chave e valor explicitamente
```

```
universidade = {}
universidade['USP'] = 'Amarelo'
universidade['UFSCar'] = 'Vermelho'

'USP' in universidade
>>>True

'UNESP' in universidade
>>>False

'Amarelo' in universidade
>>>False

del universidade['USP']
universidade
>>> {'UFSCar': 'Vermelho'}
```

{% include "../templates/lista_exercicios.md" %}