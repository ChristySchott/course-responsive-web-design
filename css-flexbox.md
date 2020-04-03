# CSS Flexbox

" A interface do usuário de um site ("UI") tem dois componentes. Primeiro, existem os elementos visuais, como cores, fontes e imagens. Segundo, há o posicionamento ou posicionamento desses elementos. No Web design responsivo, um layout UI deve acomodar muitos navegadores e dispositivos diferentes que acessam o conteúdo.

O CSS3 introduziu flexes boxes, ou flexbox, para criar layouts de página para uma interface de usuário dinâmica. É um modo de layout que organiza elementos de maneira previsível para diferentes tamanhos de tela e navegadores. Embora um pouco novos, todos os navegadores modernos populares suportam o flexbox. Esta seção aborda como usar o flexbox e as diferentes opções de layout que ele oferece.
 
Tópicos da sessão:
- Use display: flex to Position Two Boxes
- Add Flex Superpowers to the Tweet Embed
- Use the flex-direction Property to Make a Row
- Apply the flex-direction Property to Create Rows in the Tweet Embed
- Use the flex-direction Property to Make a Column
- Apply the flex-direction Property to Create a Column in the Tweet Embed
- Align Elements Using the justify-content Property
- Use the justify-content Property in the Tweet Embed
- Align Elements Using the align-items Property
- Use the align-items Property in the Tweet Embed
- Use the flex-wrap Property to Wrap a Row or Column
- Use the flex-shrink Property to Shrink Items
- Use the flex-grow Property to Expand Items
- Use the flex-basis Property to Set the Initial Size of an Item
- Use the flex Shorthand Property
- Use the order Property to Rearrange Items
- Use the align-self Property

-------
## Justify-Content

- **flex-start**: alinha itens ao início do container flex. Para uma linha, isso empurra os itens para a esquerda do contêiner. Para uma coluna, isso empurra os itens para o topo do contêiner. Esse é o alinhamento padrão se nenhum conteúdo justificado for especificado.
- **flex-end**: alinha os itens ao final do contêiner flex. Pra uma linha, isso empurra os itens à direita do contêiner. Para uma coluna, isso empurra os itens para o fundo do contêiner.
- **space-between**: alinha os itens ao centro do eixo principal, com espaço extra colocado entre os itens. O primeiro e o último itens são empurrados para a extremidade do contêiner flexível. Por exemplo, em uma linha, o primeiro item fica no lado esquerdo do contêiner, o último item fica no lado direito do contêiner e, em seguida, o espaço restante é distribuído igualmente entre os outros itens.
- **space-around**: semelhante ao space-between, mas o primeiro e o último itens não estão bloqueados nas bordas do contêiner, o espaço é distribuído em todos os itens com um meio espaço em cada extremidade do contêiner flex.
- **space-uniformly**: distribui o espaço uniformemente entre os itens flexíveis com um espaço completo em cada extremidade do contêiner flexível

------
##Align-Items

- **flex-start**: alinha itens ao início do container flex. Para linhas, isso alinha itens à parte superior do contêiner. Para colunas, isso alinha os itens à esquerda do contêiner.
- **flex-end**: alinha os itens ao final do contêiner flex. Para linhas, isso alinha os itens na parte inferior do contêiner. Para colunas, isso alinha os itens à direita do contêiner.
- **center**: alinha os itens ao centro. Para linhas, isso alinha verticalmente os itens (espaço igual acima e abaixo dos itens). Para colunas, isso as alinha horizontalmente (espaço igual à esquerda e à direita dos itens).
- **stretch**: estique os itens para encher o recipiente flexível. Por exemplo, os itens de linhas são esticados para preencher o contêiner flexível de cima para baixo. Este é o valor padrão se nenhum valor de alinhamento de itens for especificado.
- **baseline**: alinhar itens às linhas de base. Linha de base é um conceito de texto, pense nele como a linha em que as letras se assentam.

-------
## flex-wrap

- **nowrap**: esta é a configuração padrão e não quebra itens.
- **wrap**: agrupa os itens da esquerda para a direita, se estiverem em uma linha, ou de cima para baixo, se estiverem em uma coluna.
- **wrap-reverse**: agrupa os itens da direita para a esquerda, se estiverem em uma linha, ou de baixo para cima, se estiverem em uma coluna.

-------

## Flex Shorthand Property

There is a shortcut available to set several flex properties at once. The flex-grow, flex-shrink, and flex-basis properties can all be set together by using the flex property.

For example, flex: 1 0 10px; will set the item to flex-grow: 1;, flex-shrink: 0;, and flex-basis: 10px;.

-------

## Align-self

This property allows you to adjust each item's alignment individually, instead of setting them all at once. This is useful since other common adjustment techniques using the CSS properties float, clear, and vertical-align do not work on flex items.

<kbg>align-self</kbg> accepts the same values as <kbg>align-items</kbg> and will override any value set by the <kbg>align-items</kbg> property.
