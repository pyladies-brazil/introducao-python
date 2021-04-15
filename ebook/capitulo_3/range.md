# Range

A função **range()** gera um iterável com N elementos, a partir de parâmetros de início, final e passo fornecidos. Seu formato geral é:

```
range(inicio,fim,passo)
```

Range gera um conjunto de dados começando em início, terminando em fim, e iterando de passo em passo.
Mas também pode ser escrita como:

```
range(inicio,fim)
range(fim)
```

Na função range, se for passado apenas um parâmetro, a função considerará como o parâmetro fim, se forem passados dois parâmetros, como início e fim, por padrão.

Início e passo são parâmetros não-obrigatórios, e recebem como valores padrão 0 e 1, respectivamente, como padrão caso não sejam passados.

Fim é um limitante não-inclusivo, isto é, o último elemento será estritamente menor que fim.

{% include "../templates/lista_exercicios.md" %}