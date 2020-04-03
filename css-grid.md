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


