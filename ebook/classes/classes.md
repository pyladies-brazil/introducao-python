# Classes

Classes são criadas utilizando a palavra reservada class, tem métodos definidos com a palavra reservada `def`.

Atenção à indentação e ao self! Para um método pertencer à uma classe, ele precisa estar indentado dentro da classe e definido com o argumento self.

Os métodos funcionam de forma análoga às funções, possuindo parâmetros e retorno opcionais.

```
class NomeDaClasse (HerancaOpcional):
   # Se não herdar de outra classe, não precisa nem dos parênteses
   def __init__(self, argumentos_opcionais):
       # Inicializador da classe
       # É executado quando a classe é instanciada

   def metodos_da_classe(self, argumentos_opcionais):
       # Realizam operações sobre a classe
```

```
class PyLadies:
   # Inicializador da classe
   def __init__(self, nome_capitulo, num_integrantes, integrantes):
       self.nome_capitulo = nome_capitulo
       self.num_integrantes = num_integrantes
       self.integrantes = integrantes
       print('Capítulo criado!')
   
   def __str__(self):
       return f"PyLadies {self.nome_capitulo}\n{self.num_integrantes} integrantes:\n" + "\n".join(self.integrantes)

   def adicionar_integrante(self, nome):
       self.num_integrantes += 1
       self.integrantes.append(nome)
```

Instanciando e inicializando a classe

```
pyladies_sao_carlos = PyLadies('São Carlos', 6, ["Amanda", "Ana Dulce", "Hemilyn", "Juliana Karoline", "Juliana Alves", "Thayana"])
```

Chamando o método adicionar integrante

```
pyladies_sao_carlos.adicionar_integrante("Marília")
```

Utilizando o método especial `__str__` para exibir a classe

```
print(pyladies_sao_carlos)
```
Em Python, o inicializador da classe é o `__init__`, que faz parte dos conhecidos dunder methods, os “métodos mágicos” do Python.

Existem muitos dunder methods que não iremos abordar neste momento, focaremos em `__init__`, que inicializa a classe, e `__str__`, que cria uma representação da classe voltada ao usuário e permite que um objeto seja passado diretamente em um print.

{% include "../templates/lista_exercicios.md" %}