# CSS Grid 

"CSS Grid ajuda a criar facilmente designs web complexos. Ele funciona transformando um elemento HTML em um contêiner de grade com linhas e colunas para que você coloque os elementos filhos onde quiser dentro da grade."

Eu não havia trabalhado muitas vezes com Grid então aprendi muita coisa nova. Como cada etapa requer um exercício eu já pude colocar em prática e fixar o conteúdo. Será muito útil pra mim daqui em diante.

# Columns

Após adicionar o <kbg>display: grid</kbg>, posso transformar o grid em colunas com o <kbg>grid-template-columns</kbg>.
```
.container {
  display: grid;
  grid-template-columns: 50px 50px;
}
```
Isso dará à sua grid duas colunas com 50 px de largura cada. O número de parâmetros fornecidos à propriedade grid-template-columns indica o número de colunas na grade e o valor de cada parâmetro indica a largura de cada coluna.

# Rows

É o mesmo processo das colunas, apenas uso <kbg>grid-template-rows</kbg>.

# Units of size

- **fr**: define a coluna ou linha para uma fração do espaço disponível,

- **auto**: define a coluna ou linha para a largura ou altura do seu conteúdo automaticamente,

- **%**: ajusta a coluna ou linha para a largura percentual de seu contêiner.

# Column gap

Até agora, nas grades que você criou, todas as colunas foram apertadas uma contra a outra. Às vezes, você quer um espaço entre as colunas. Para adicionar um espaço entre as colunas, use a propriedade <kbg>grid-column-gap</kbg> assim:

```
grid-column-gap: 10px;
```

# Row gap

O esqueme é o mesmo do anterior, agora adicionando espaço entre as linhas com o <kbg>grid-row-gap</kbg>.

# Atalho para o gap, espaçando linha e coluna ao mesmo tempo

<kbg>grid-gap</kbg> é uma propriedade abreviada de <kbg>grid-row-gap</kbg> e <kbg>grid-column-gap</kbg> dos dois desafios anteriores, mais conveniente de usar. Se <kbg>grid-gap</kbg> tiver um valor, ele criará um gap entre todas as linhas e colunas. No entanto, se houver dois valores, ele usará o primeiro para definir o <kbg>grid-row-gap</kbg> e o segundo valor <kbg>grid-column-gap</kbg>.

# Grid Column para controlar o espaço.

o <kbg>grid-column</kbg> vai servir com uma espécie de container para outros grids, contendo eles dentro dele.

Para controlar a quantidade de colunas que um item consumirá, você pode usar a propriedade <kbg>grid-column</kbg> em conjunto com os números de linha em que deseja que o item inicie e pare.

Aqui está um exemplo:

```
grid-column: 1/3;
```
Isso fará com que o item inicie na primeira linha vertical da grade à esquerda e se estenda até a terceira linha da grade, consumindo duas colunas. A primeira linha é a do extremo esquerdo, então se o final for 4, consumirá duas colunas

# Grid row

Junto com o grid-column posso usar o <kbg>grid-row</kbg> para definir o altura do meu grid.

**grid-column define width enquando o grid-row define height**.

**uso o justify-items para alinhar horizontalmente e o align-items para justificar verticalmente**.

# Grid-template-areas

Você pode agrupar células do seu grid em uma área e dar um nome personalizado à área. Faça isso usando grid-template-areas no contêiner desta maneira:
```
grid-template-areas:
  "header header header"
  "advert content content"
  "footer footer footer";
```

Após criar o modelo de uma área para seu grid container, como mostrado no desafio anterior, você pode colocar um item em sua área personalizada, referenciando o nome que você deu. Para fazer isso, use a propriedade <kbg>grid-area</kbg> em um item como este:
```
grid-area: header;
```

**é muito util utilizar o grid-area: footer; e o grid-area: header;**

# Use grid-area Without Creating an Areas Template

A propriedade da <kbg>grid-area</kbg> que você aprendeu no último desafio pode ser usada de outra maneira. Se sua grid não tiver um modelo de áreas para referência, você poderá criar uma área rapidamente para que um item seja colocado assim:
```
item1 { 
grid-area: 1/1/2/4; 
}
```

Isso está usando os números de linha que você aprendeu anteriormente para definir onde será a área para este item. Os números no exemplo acima representam estes valores:

```
grid-area: horizontal line to start at / vertical line to start at / horizontal line to end at / vertical line to end at;
```

# Reduce Repetition Using the repeat Function

Digamos que você queira uma grade com 100 linhas da mesma altura. Não é muito prático inserir 100 valores individualmente. Felizmente, existe uma maneira melhor - usando a função <kbg>repeat</kbg> para especificar o número de vezes que você deseja que sua coluna ou linha seja repetida, seguida por uma vírgula e o valor que você deseja repetir.

Aqui está um exemplo que criaria a grade de 100 linhas, cada linha com 50 px de altura.
```
grid-template-rows: repeat(100, 50px);
```

Você também pode repetir vários valores com a função de repetição e inserir a função entre outros valores ao definir uma estrutura de grade. Aqui está o que parece:
```
grid-template-columns: repeat(2, 1fr 50px) 20px;
```
Isso significa:
```
grid-template-columns: 1fr 50px 1fr 50px 20px;
```
#  Limit Item Size Using the minmax Function

É usado para limitar o tamanho dos itens quando o contêiner da grade muda de tamanho. Para fazer isso, você precisa especificar o intervalo de tamanho aceitável para o seu item. Aqui está um exemplo:
```

grid-template-columns: 100px minmax(50px, 200px);
```

No código acima, <kbg>grid-template-columns</kbg> está definido para criar duas colunas; o primeiro tem 100px de largura e o segundo tem a largura mínima de 50px e a largura máxima de 200px.

# Create Flexible Layouts Using auto-fill

A função de repetição vem com uma opção chamada <kbg>auto-fill</kbg>. Isso permite inserir automaticamente o maior número possível de linhas ou colunas do tamanho desejado, dependendo do tamanho do contêiner. Você pode criar layouts flexíveis ao combinar o <kbg>auto-fill</kbg> com o minmax, assim:
```
repeat(auto-fill, minmax(60px, 1fr));
```

# Auto-fit 

A única diferença é que, quando o tamanho do contêiner excede o tamanho de todos os itens combinados, o <kbg>auto-fill</kbg> continua inserindo linhas ou colunas vazias e empurra seus itens para o lado, enquanto o <kbg>auto-fit</kbg> recolhe essas linhas ou colunas vazias e estende seus itens para ajuste do tamanho do recipiente.
