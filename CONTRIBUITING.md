# Como contribuir
Muito obrigada por nos ajudar a compor este material! A ferramenta utilizada é a [HonKit](https://github.com/honkit/honkit/), que gera arquivos HTML estáticos a partir de arquivos Markdown (.md). No [README](README.md) explicamos direitinho como você pode rodar o projeto na sua máquina.

Caso você só queira visualizar como ficará o seu markdown, só precisa usar o [Hackmd](https://hackmd.io/). Ou seja, caso você **nunca** tenha escrito uma documentação em Markdown, pode ser a sua chance!:rocket:

**Sumário**

1. [Antes de iniciar](#antes-de-iniciar)
   - [Forkando e clonando o repositório](#forkando-e-clonando-o-repositório)
2. Realizando alterações
   - [Modificando e-Book](#modificando-e-book)
     - [Alterando artigo existente](#alterando-artigo-existente)
     - [Criando novo artigo](#criando-novo-artigo)
   - [Modificando lista de vídeos](#modificando-lista-de-vídeos)
   - [Atualizando slides](#atualizando-slides)
4. [Enviando as modificações](#enviando-as-modificações)
   - [1. Commit seu código](#1-commit-seu-código)
   - [2. Atualize seu fork](#2-atualize-seu-fork)
   - [3. Envie as modificações](#3-envie-as-modificações)


## Antes de iniciar
### Forkando e clonando o repositório

1. Faça o fork do projeto
2. Clone seu fork para a sua máquina:
```
git clone <Link do seu fork>
```

3. Crie uma branch para as modificações em que trabalhará: 
```
git checkout -b <nome-da-branch-das-modificações>
```

## Modificando e-Book
### Alterando artigo existente
Navege pelo [Sumário](ebook/SUMMARY.md), encontre o artigo que deseja modificar, acesse-o e modifique o seu Markdown. Após testes no [Hackmd](https://hackmd.io/) ou no próprio e-book, envie as modificações seguindo as orientações da sessão [Enviando as modificações](#enviando-as-modificações).

### Criando novo artigo
Verifique se o assunto já não está contido em nenhum artigo existente.

A estrutura de diretório é a seguinte:

```
├── ebook
    ├── book.json
    ├── README.md
    ├── SUMMARY.md
    ├── capitulo_1/   
        └── assunto.md
```
1. Crie uma nova pasta e dentro dela um arquivo.md
2. Insira o conteúdo do arquivo usando a seguinte estrura:
```
# Assunto

[Conteúdo]

{% include "../templates/lista_exercicios.md" %} #Essa linha adicionará o link para a lista de exercícios
```
3. Adicione esse novo artigo no [Sumário](ebook/SUMMARY.md)
4. Após testes no [Hackmd](https://hackmd.io/) ou no próprio e-book, envie as modificações seguindo as orientações da sessão [Enviando as modificações](#enviando-as-modificações).

## Modificando lista de vídeos
Acesse o arquivo [serie_youtube](serie_youtube.md) e insira o link para o vídeo correspondente na tabela.

## Atualizando slides
Substitua o arquivo (.pdf) com os slides por outro com exatamente mesmo nome. Isso é necessário para não quebre os links que remetem ao slides e que estão presentes no e-book e demais partes desse repositório.

## Enviando as modificações
### 1. Commit seu código
1. Verifique os arquivos modificados:
```
git status
```

2. Adicione na staging area apenas os arquivos que vocẽ modificou:
```
git add <nome do arquivo> #adicione aqui todos os arquivos modificados separando-os por um espaço em branco
```

3. Faça um comentário sobre as modificações realizadas
```
git commit -m "Insira a sua mensagem aqui"
```

### 2. Atualize seu fork
Como esse projeto é feito a várias mãos, é interessante que antes de enviar as modificações você sempre atualize seu fork com as novas informações do repositório original.

1. Adicione o repositório original:
```
git remote add upstream https://github.com/pyladies-brazil/introducao-python.git
```

2. Verifique que você está na sua branch principal:
```
git checkout main
```

3. Atualize sua branch principal:
```
git pull upstream main
```

4. Atualize a branch a qual você realizou as modificações:
```
git checkout <nome-da-branch-das-modificações>
git rebase main
```

### 3. Envie as modificações
1. Faça push desses commits para sua branch: 
```
git push origin <nome-da-branch-das-modificações>
```

Acesse a [página de pull requeste do repositório](https://github.com/pyladies-brazil/introducao-python/pulls), lá deve aparecer uma janela com destaque amarelo. Clique no botão para criar um novo pull request, preecha a mensagem e salve.

Feito!!!:sunflower:

> Deu tudo certo? Compartilhe este material para colegas, amigas suas que estejam querendo estudar Python, mas que também serve para iniciantes que estejam aprendendo as suas primeiras linguagens de programação. :heart:

:::info
:bulb: **Dica:** Dúvidas podem ser enviadas [abrindo uma nova issue](https://github.com/pyladies-brazil/introducao-python/issues).
:::
