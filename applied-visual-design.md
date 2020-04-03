# Introduction to the Applied Visual Design Challenges

Novamente, ja havia trabalhado com alguns dos temas abordados pelo módulo, o que me permitiu reconhecer a qualidade do conteúdo. Alguns conceitos, a maioria, eu ja conhecia, outros não. Tentarei listar os principais assuntos:

- alinhamento (text-align)
- responsividade
- posicionamento 
- tamanho (width e height)
- decoração de texto (strong e underline)

Uma coisa interessanta de aprender foi a tag <kbg>hr</kbg>, que faz uma espécie de borda para o texto.


Pude aprender também uma nova propriedade para auxiliar na edição das cores, a <kbg>hsl()</kbg>, que permite trabalhar com o brilho e a saturação da cor a que se referencia.


Também me foi útil o conteúdo sobre linear-gradient. Eu já conhecia o método mas pude entender como funciona sua estrutura, que tem a seguinte forma:

```
background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);
```


Vale destacar a ótima explicação do curso sobre o comando <kbg>scale()</kbg>, sendo recomendado para uso em uma ação <kbg>:hover</kbg>
```
p:hover {
  transform: scale(2.1);
}
```

Uma função da propriedade <kbf>transform</kbg> que eu pude ter meu primeiro contato foi a <kbg>skewX()</kbg>. 
Essa função irá trabalhar com o eixo horizontal, mas posso também modificar o vertical com a função <kbg>skewY()</kbg>.


Quando estou utilizando uma animação em um <kbg>:hover</kbg> e quero que ela continue funcionando enquando eu estiver com o mouse em cima, uso a proriedade <kbg> animation-fill-mode: forwards; </kbg>.

Também posso definir o número de vezes que uma animação será executada, com a função <kbg>animation-iteration-count:</kbg>. Se eu quiser que ela execute sem parar, basta colocar o <kbg>infinite</kbg> após os dois pontos.

Antes do curso eu ja utilizava as palavras-chaves <kbg>ease</kbg>,<kbg>ease-out</kbg>,<kbg>ease-in</kbg> e <kbg>linear</kbg>, mas só durante as aulas que pude entender o conceito de cada um.
No <kbg>ease</kbg>, a animação começa devagar, acelera no meio e diminui no fim. No <kbg>ease-out</kbg>, ela começa rápido e diminui no fim, e na <kbg>ease-in</kbg> ela começa devagar e terminar rapido. Ja na <kbg>linear</kbg> a velocidade sobre de forma constante. Posso definir todas essas propriedades com a função <kbg>animation-timing-function</kbg>.
