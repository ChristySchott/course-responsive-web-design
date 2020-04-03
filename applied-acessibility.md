# Applied Acessibility

Com certeza, o momento mais importante do curso até agora. Além de estudar sobre algo tão necessário e importante como a acessibilidade, pude aprender muitos conceitos novos. Para entender do que se trata o módulo, deixarei aqui a sua introdução traduzida para o português:

" "Acessibilidade" geralmente significa ter conteúdo da Web e uma interface do usuário que pode ser entendida, navegada e interagida por um público amplo. Isso inclui pessoas com deficiência visual, auditiva, de mobilidade ou cognitiva.

Os sites devem estar abertos e acessíveis a todos, independentemente das habilidades ou recursos de um usuário. Alguns usuários confiam na tecnologia assistida, como um leitor de tela ou software de reconhecimento de voz. Outros usuários podem navegar através de um site apenas usando um teclado. Manter as necessidades de vários usuários em mente ao desenvolver seu projeto pode ajudar bastante na criação de uma Web aberta.

Aqui estão três conceitos gerais que esta seção explorará nos seguintes desafios:

- ter um código bem organizado que usa marcação apropriada
- garantir a existência de alternativas de texto para conteúdo não textual e visual
- criar uma página de fácil navegação que seja compatível com teclado

Ter conteúdo da web acessível é um desafio contínuo. Um ótimo recurso para seus projetos daqui para frente são as Diretrizes de Acessibilidade para Conteúdo da Web (WCAG) do W3 Consortium. Eles definem o padrão internacional de acessibilidade e fornecem vários critérios que você pode usar para verificar seu trabalho.

O HTML5 introduziu o elemento <kbg>figure</kbg>, junto com a legenda da figura relacionada. Usados ​​juntos, esses itens agrupam uma representação visual (como uma imagem, diagrama ou gráfico) junto com sua legenda. Isso fornece um aumento de acessibilidade duplo, agrupando semanticamente o conteúdo relacionado e fornecendo uma alternativa em texto que explica a figura.

Sintaxe do <kbg>figure</kbg>:
```
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>
```

## Acesskey

Algo totalmente novo para mim foi o <kbg>acesskey</kbg>, ou chave de acesso, que permite o usuário navegar entre os links usando apenas o teclado.
O HTML5 permite que esse atributo seja usado em qualquer elemento, mas é particularmente útil quando usado com os interativos. Isso inclui links, botões e controles de formulário.

Um exemplo:
```
<button accesskey = "b"> Botão importante </button>
```

## Tabidenx para adicionar foco do teclado a um elemento

Certain elements, such as links and form controls, automatically receive keyboard focus when a user tabs through a page. It's in the same order as the elements come in the HTML source markup. This same functionality can be given to other elements, such as div, span, and p, by placing a <kbg>tabindex="0"</kbg> attribute on them. Here's an example:

```
<div tabindex="0">I need keyboard focus!</div>
```

Também posso usar o <kbg>tabindex</kbg> para definir a ordem de elementos acessados pelo teclado:
```
<div tabindex="1">I get keyboard focus, and I get it first!</div>

<div tabindex="2">I get keyboard focus, and I get it second!</div>
```
