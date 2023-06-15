# WAI-ARIA (Accessible Rich Internet Applications)

WAI-ARIA, que significa Accessible Rich Internet Applications, é um conjunto de especificações desenvolvidas pelo World Wide Web Consortium (W3C) para melhorar a acessibilidade de aplicativos da web para pessoas com deficiência. O WAI-ARIA fornece uma série de atributos e propriedades que podem ser adicionados a elementos HTML para melhorar a semântica e a interação desses elementos com tecnologias assistivas, como leitores de tela.

O ponto é que a semântica não fica apenas na hora de marcar a informação com HTML puro. Como você faz para que um usuário com deficiência visual saiba que a informação que ele procura está dentro de um collapse, e esse collapse está fechado? Como você avisa que aquele lugar onde ele está navegando é o lugar mais importante da página? Que aquele monte de links que o leitor de tela está falando é o menu principal do site?

A web tradicional foi projetada principalmente para interação entre humanos e não possui recursos nativos para descrever totalmente a estrutura e a funcionalidade dos componentes de uma página para usuários com deficiência. O WAI-ARIA preenche essa lacuna, permitindo que os desenvolvedores web adicionem informações adicionais para descrever e fornecer contexto para elementos interativos e personalizados.

## Estendendo o Significado

A WAI-ARIA serve para estender o significado das interações do seu site. Quando as tags do HTML5 vieram, elas já começaram um trabalho importante de dar significado às estruturas do layout. Você consegue marcar agora o que é um menu de navegação, uma sidebar, um header, um footer etc. Esse trabalho é muito importante por que ajuda a definir a importância dos elementos que cada elemento contém.

A WAI-ARIA vai ajudar muito em aplicações onde a informação é dividida em várias porções na tela em diversos elementos que precisam de interação para que a informação seja visualizada, como um clique, fazendo com que a acessibilidade seja prejudicada e o usuário não consiga acessar todas as partes desse layout de maneira linear.

## Roles, States e Properties

A WAI-ARIA é divide a semântica em duas partes: Roles, que define que tipo de elemento o usuário está interagindo e States/Properties que são suportadas pelas Roles, que definem o estado daquele elemento.

Com a Role você fala que determinado elemento é uma collapse, com o States/Properties você diz se esse collapse está aberto ou fechado.

Existem três principais componentes do WAI-ARIA:

* **Papéis (Roles)**: Os papéis definem o tipo de componente ou widget presente na página, como botão, caixa de diálogo, menu, etc. Esses papéis ajudam a descrever a função e a finalidade dos elementos para os usuários.
  
* **Propriedades (Properties)**: As propriedades definem as características adicionais de um elemento, como seu estado atual, se está expandido, se está desabilitado, entre outros. Elas fornecem informações contextuais importantes para a interação e a compreensão do elemento.
  
* **Estados (States)**: Os estados representam as condições dinâmicas dos elementos, como se estão selecionados, abertos, focados ou inativos. Esses estados auxiliam na comunicação dos eventos que ocorrem em um elemento ao usuário.

## Observações Importantes

Ao usar o WAI-ARIA, os desenvolvedores podem criar aplicativos da web mais acessíveis, permitindo que pessoas com deficiência interajam com eles de maneira mais eficaz. Os leitores de tela e outras tecnologias assistivas podem interpretar as informações fornecidas pelo WAI-ARIA e fornecer feedback adequado aos usuários, tornando a experiência mais inclusiva.

É importante destacar que o uso adequado do WAI-ARIA requer um conhecimento sólido das práticas recomendadas e das diretrizes de acessibilidade, a fim de garantir uma implementação correta e eficiente. Além disso, é sempre recomendado projetar e desenvolver sites e aplicativos com acessibilidade em mente desde o início, em vez de tentar corrigir problemas de acessibilidade posteriormente.

[Próximo subseção: WCAG](./como-usar-wai-aria.md)