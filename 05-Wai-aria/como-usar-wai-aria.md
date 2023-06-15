# Como usar o WAI-ARIA?

O uso adequado do WAI-ARIA envolve a aplicação dos atributos, papéis e estados corretos nos elementos da página para melhorar sua acessibilidade, como mencionado na seção anterior.

## Roles

As funções do ARIA atribuem um significado semântico ao conteúdo, permitindo que leitores de tela e outras ferramentas apresentem e suportem a interação com o objeto de acordo com as expectativas do usuário para esse tipo de objeto. Essas funções podem ser usadas para descrever elementos que não estão nativamente presentes no HTML ou que existem, mas ainda não têm suporte completo nos navegadores.

Normalmente, os elementos semânticos no HTML já possuem uma função atribuída. Por exemplo, um elemento ```<input type="radio">``` tem a função de "rádio". Por outro lado, os elementos não semânticos, como ```<div>``` e ```<span>```, não possuem uma função atribuída por padrão. Nesses casos, o atributo role pode ser utilizado para fornecer uma função semântica.

As funções do ARIA são adicionadas a elementos HTML utilizando role="tipo-de-função", em que o tipo de função é o nome de uma função especificada pelo ARIA. Algumas funções exigem a inclusão de estados ou propriedades associadas do ARIA, enquanto outras são válidas apenas quando usadas em conjunto com outras funções.

Por exemplo, se um elemento ```<ul>``` recebe a função role="tabpanel", leitores de tela o anunciarão como um "painel de guias". No entanto, se esse painel de guias não tiver guias aninhadas, o elemento com a função de painel de guias não será realmente um painel de guias, e a acessibilidade será afetada negativamente.

Para verificar todas as Funções WAI-ARIA, acesse o [Link](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles)

## Propriedades (Properties)

As Properties ARIA (Propriedades) definem semânticas adicionais não suportadas no HTML padrão.

Um exemplo é ```<button aria-haspopup="true">```. Essa propriedade estende o botão padrão para fazer com que um leitor de tela anuncie que o botão, se ativado, acionará um pop-up.

Para consultar a lista completa de estados e propriedades WAI-ARIA acesse [Taxonomy of WAI-ARIA States and Properties](https://www.w3.org/TR/wai-aria-1.2/#state_prop_taxonomy)

## Estados (States)

Os States ARIA (Estados) são atributos que definem a condição atual de um elemento.

Eles geralmente mudam com base na interação feita ou em alguma variável dinâmica. Um exemplo é ```<input aria-invalid="true">```. Essa propriedade fará com que um leitor de tela leia essa entrada como inválida no momento (o que significa que precisa ser corrigida), mas esse valor de estado pode ser facilmente alterado para false dinamicamente com base no quê é preenchido. 

Para consultar a lista completa de estados WAI-ARIA acesse [ Global States](https://www.w3.org/TR/wai-aria-1.2/#global_states)

## Dicas Importantes

* Entenda as necessidades de acessibilidade: Familiarize-se com as necessidades das pessoas com deficiência e como elas interagem com a web. Isso ajudará você a identificar quais elementos e interações podem se beneficiar do uso do WAI-ARIA.
  
* Identifique os componentes apropriados: Analise sua página e identifique os elementos interativos, como botões, menus, caixas de diálogo, barras de progresso, etc., que precisam de informações adicionais para serem adequadamente interpretados por tecnologias assistivas.
  
* Adicione propriedades e estados: Use atributos como "aria-label", "aria-labelledby" e "aria-describedby" para fornecer descrições adicionais aos elementos. Essas propriedades ajudam a fornecer contexto e informações claras para os usuários.
  
* Mantenha os estados atualizados: Atualize os estados dos elementos conforme necessário. Por exemplo, use o atributo "aria-expanded" para indicar se um menu está aberto ou fechado, o atributo "aria-selected" para indicar itens selecionados em uma lista, etc.
  
* Valide sua implementação: Utilize ferramentas de validação de acessibilidade, como as fornecidas pelo W3C, para verificar se você está aplicando corretamente o WAI-ARIA e se sua página está em conformidade com as diretrizes de acessibilidade.
  
  
Lembrando que essas são apenas orientações básicas. O WAI-ARIA é uma especificação detalhada e complexa, e é recomendado estudar e seguir as diretrizes e práticas recomendadas para garantir uma implementação correta e eficaz. O W3C fornece uma documentação completa sobre o WAI-ARIA, que pode ser um recurso valioso para aprender mais sobre como usá-lo adequadamente.