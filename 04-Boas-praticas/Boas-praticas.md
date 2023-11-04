# Boas práticas

Abaixo vamos comentar sobre alguns recursos fáceis de serem implementados:

## HTML Semântico

É impressionante como a quantidade de sites e páginas na *web* crescem cada dia mais. Por isso, juntamente com o crescimento da internet, também aumenta os padrões, técnicas e práticas de desenvolvimento *web*.

Diante disso, o HTML com uma boa semântica visa descrever o significado do conteúdo presente em documentos HTML, deixando tudo mais claro, tanto para desenvolvedores, quanto para *browsers*. Todos os componentes devem ser identificados de acordo semanticamente. Exemplo: uma lista  de itens deve ser marcada com a tag UL ou LI.

Outro exemplo e o uso do elemento *button*, que tem diversos estilos já aplicados nele mesmo e é embutido com padrões de acessibilidade pelo teclado, botões estes que podem ser navegados por meio da tecla Tab, e ativados utilizando a tecla Enter.

Vamos listar aqui mais algumas boas práticas:

* Em geral, a cor do componente deve ter contraste suficiente em relação a cor de fundo. Para verificar, é recomendada a ferramenta [Adobe Color](https://color.adobe.com/pt/create/color-contrast-analyzer).
  
* Componentes interativos devem ter uma área clicável de no mínimo 54px por 54px.
  
* Devem ser acessíveis via teclado.
  
* Se for um componente complexo que não existe no HTML, é possível recorrer ao [WAI-ARIA (*web* Accessibility Initiative – Accessible Rich Internet Applications)](https://www.w3.org/WAI/standards-guidelines/aria/), uma especificação que complementa o HTML. (Vamos falar sobre o WAI-ARIA em capítulos futuros).

## Conteúdo multimídia

* Todo conteúdo não-textual deve ter uma alternativa em texto.
  
* Imagens não decorativas devem ter texto alternativo. As decorativas devem ter atributo alt vazio (alt=””). Para decidir se a imagem deve ter texto alternativo, o W3C preparou uma [“árvore de decisão sobre alt“](https://www.w3.org/WAI/tutorials/images/decision-tree/).
  
* Vídeos devem ter legenda e intérprete de libras (caso tenham áudio) e, se for o caso, audiodescrição.
  
* Áudios devem ter transcrição e serem identificados com legenda. Para a legenda, recomenda-se o uso das *tags figure e figcaption*.

## Texto

* Evite alinhamento centralizado nos blocos de texto e não utilize textos justificados. (O ideal são textos alinhados à esquerda, pois trazem um ponto de partida fixo para a leitura).
  
* Os textos devem ter espaçamento suficiente entre as letras, parágrafos e palavras. Acesse o [Critério de Sucesso](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/#text-spacing) da WCAG para saber mais detalhes.
  
* Títulos devem ser identificados semanticamente com as *tags* de cabeçalho (H1, H2, H3, etc). Não é recomendado pular níveis de cabeçalho.
  
* O texto deve ter um tamanho de fonte adequado. Recomendado para corpo de texto: 20px.
  
* Mudanças de língua devem ser avisadas semanticamente (atributo “lang” da tag span).

## Formulários

* Todos os campos de formulários devem ter rótulos identificados semanticamente *tag label*.
  
* Erros não devem ser comunicados apenas por cor. Devem ser claros, para que o usuário possa corrigir.
  
* Oferecer sugestões de preenchimento.

## Botões e *links*

* Deve ser possível compreender do que se trata o *link*/botão apenas por seu texto (ou nome), fora de contexto. Títulos como “saiba mais”, “clique aqui” são práticas ruins.
  
* Caso abra um PDF, o usuário deve ser avisado.
  
---

[Próximo capítulo: WAI-ARIA](../05-Wai-aria/Wai-aria.md)
