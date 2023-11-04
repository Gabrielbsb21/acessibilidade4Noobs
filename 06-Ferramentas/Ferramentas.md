# Ferramentas de Acessibilidade

Visão Geral:

- [Ferramentas de Acessibilidade](#ferramentas-de-acessibilidade)
  - [Avaliador e Simulador de Acessibilidade em Sítios (ASES)](#avaliador-e-simulador-de-acessibilidade-em-sítios-ases)
  - [*Markup Validation Service* (W3C)](#markup-validation-service-w3c)
  - [*Web Accessibility Evaluation Tool* (WAVE)](#web-accessibility-evaluation-tool-wave)
  - [Exemplo de código HTML com erros de acessibilidade](#exemplo-de-código-html-com-erros-de-acessibilidade)
  - [Recomendações](#recomendações)
    - [en-us](#en-us)
    - [pt-br](#pt-br)

## Avaliador e Simulador de Acessibilidade em Sítios (ASES)

- O [ASES](https://asesweb.governoeletronico.gov.br/) é uma ferramenta que permite avaliar e simular a acessibilidade de sítios da Internet, de acordo com as recomendações do Modelo de Acessibilidade em Governo Eletrônico [(eMag)](https://emag.governoeletronico.gov.br/), que por sua vez é baseada nas recomendações de acessibilidade da [**WCAG**](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/). O ASES é uma ferramenta de apoio à avaliação de acessibilidade, não substituindo a avaliação humana.

**Formas de utilizar o ASES**:

- Conta com a versao web que possui três formar de avaliar o conteúdo:
   1. URL: Avalia o conteúdo de um sítio da Internet, acessível publicamente, a partir de sua URL.
   2. Arquivo: Avalia o conteúdo de um sítio da Internet, acessível publicamente, a partir de um arquivo HTML.
   3. Código-fonte: Avalia o conteúdo de um sítio da Internet, acessível publicamente, a partir do código-fonte HTML.

## *Markup Validation Service* (W3C)

- O [Markup Validation Service](https://validator.w3.org/) é um serviço que permite validar documentos HTML, XHTML, SMIL, MathML, etc. O serviço é fornecido pelo W3C para ajudar autores de páginas da Web a validar a marcação de seus documentos. Os documentos podem ser validados em três formas diferentes, assim como o ASES o W3C também fornece avaliação por URL, por arquivo ou por fragmento de texto.  
  
## *Web Accessibility Evaluation Tool* (WAVE)

- O [WAVE](https://wave.webaim.org/) é uma ferramenta de avaliação de acessibilidade da Web desenvolvida pela WebAIM. Ele fornece visualizações visuais e alternativas de texto para ajudar os usuários a avaliar a acessibilidade de suas páginas da Web. Ele também examina o conteúdo para determinar se ele cumpre as práticas recomendadas de acessibilidade.

## Exemplo de código HTML com erros de acessibilidade

Código HTML (Clique para Expandir/Recolher)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Página com Erros de Acessibilidade</title>
</head>
<body>
    <div align="center">
        <h1><font size="6" color="blue">Bem-vindo</font></h1>
        <p>Este é o meu site incrível.</p>
    </div>
    
    <hr>
    
    <table border="1">
        <tr>
            <td><b>Título</b></td>
            <td>Texto principal</td>
        </tr>
        <tr>
            <td colspan="2">
                <img src="imagem.jpg" alt="Imagem">
            </td>
        </tr>
    </table>
    
    <br>
    
    <div style="text-align: center;">
        <a href="#" onclick="javascript:alert('Cliquei!');">Clique aqui</a>
    </div>
    
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
    
    <hr>
    
    <form>
        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome"><br>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email"><br>
        <input type="submit" value="Enviar">
    </form>
    
    <hr>
    
    <footer>
        <p>Todos os direitos reservados &copy; 2023</p>
    </footer>
</body>
</html>

```

seguindos os criterios de acessibilidade da eMag e WCAG, este código possui os seguintes erros e/ou recomendações:

- ASES:
  
| Categoria                         | Recomendação                                             | Quantidade | Linha(s) do código fonte |
| --------------------------------- | -------------------------------------------------------- | ---------- | ------------------------            |
| Erros da seção marcação           | ❌ Fornecer âncoras para ir direto a um bloco de conteúdo| 1          | 1                                   |
| Avisos da seção marcação          | ⚠️ Respeitar os Padrões Web                              | 2          | 28    29                                  |
|                                   | ⚠️ Organizar o código HTML de forma lógica e semântica   | 3          | 12, 38, 48                                  |
|                                   | ⚠️ Utilizar corretamente os níveis de cabeçalho          | 1          | 8                                   |
|                                   | ⚠️ Não utilizar tabelas para diagramação                 | 1          | 14                                  |
|                                   | ⚠️ Dividir as áreas de informação                        | 3          | 1, 1, 1                                   |
| Fim do conteúdo das recomendações |                                            |            |                          |

- W3C:
  
| Avaliação       | Descrição                                                                                            | Linha(s) do Código Fonte                 |
| --------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| **Avaliação 1** | Consider adding a lang attribute to the `<html>` start tag to declare the language of this document. | Linha 1, coluna 16 a Linha 2, coluna 6   |
| **Avaliação 2** | The `align` attribute on the `<div>` element is obsolete. Use CSS instead.                           | Linha 7, coluna 5 a Linha 7, coluna 24   |
| **Avaliação 3** | The `<font>` element is obsolete. Use CSS instead.                                                   | Linha 8, coluna 13 a Linha 8, coluna 40  |
| **Avaliação 4** | The `border` attribute on the `<table>` element is obsolete. Use CSS instead.                        | Linha 14, coluna 5 a Linha 14, coluna 22 |

<!-- - WAVE:-->

  **desafio proposto**:

- Identifcar os erros do código;
- Corrigir os erros;
- Testar o código o codigo com o ASES: <https://asesweb.governoeletronico.gov.br/>
- Testar o código com o W3C: <https://validator.w3.org/>

 [Exemplo do Código Corrigido](\exemplo_correto.html)

## Recomendações

### en-us

- Videos:
  - [Learn HTML – Full Tutorial for Beginners](https://www.youtube.com/watch?v=kUMe1FH4CHE);
  - [Why & When to Use Semantic HTML Elements over Divs](https://www.youtube.com/watch?v=bOUhq46fd5g);
  - [Accessibility: What's the difference between WCAG Levels A and AA?](https://www.youtube.com/watch?v=6V0zl-pSCSs);
  - [Web Content Accessibility Guidelines (WCAG 2.1) Crash Course](https://www.youtube.com/watch?v=NEK3aMPs1Us).

- Sites:
  - [Web Accessibility: The Ultimate Guide](https://blog.hubspot.com/website/web-accessibility);
  - [Your central source for information and resources on digital accessibility and WCAG conformance](https://wcag.com/);
  - [The Alliance for Access to Computing Careers](https://www.washington.edu/accesscomputing/30-web-accessibility-tips);
  - [Improving the User Experience](https://www.usability.gov/get-involved/index.html);

- Articles:
  - [Empirical Studies on Web Accessibility of Educational Websites: A Systematic Literature Review](https://ieeexplore.ieee.org/abstract/document/9092982);
  - [WCAG 2.1 and the Current State of Web Accessibility in Libraries](https://quod.lib.umich.edu/w/weave/12535642.0002.202/--wcag-21-and-the-current-state-of-web-accessibility?rgn=main;view=fulltext);
  - [Process Model for Continuous Testing of Web Accessibility](https://ieeexplore.ieee.org/abstract/document/9551272).

### pt-br

- Vídeos
  - [HTML Semântico - Aprenda a usar as tags semânticas do HTML5](https://www.youtube.com/watch?v=ZfNXhIptMko);
  - [article? section? div? nav? Qual tag HTML semântica escolher?](https://www.youtube.com/watch?v=BNcDPK8xPXA);
  - [Aprenda HTML semântico em 30 minutos](https://www.youtube.com/watch?v=tAFRHcEH-Pc).

- Sites:
  - [Guia de acessibilidade web](https://educadiversidade.unesp.br/guia-de-acessibilidade-web/);
  - [Acessibilidade Web – O Que É e Como Construir um Site Acessível?](https://www.hostinger.com.br/tutoriais/acessibilidade-web);
  - [Cartilha de Acessibilidade na Web](https://www.w3c.br/pub/Materiais/PublicacoesW3C/cartilha-w3cbr-acessibilidade-web-fasciculo-I.html).

- Artigos:
  - [Acessibilidade Web](https://www-periodicos-capes-gov-br.ezl.periodicos.capes.gov.br/index.php/buscador-primo.html);
  - [Acessibilidade web: uma avaliação do Sistema de Bibliotecas da Universidade Federal do Tocantins](https://capes-primo.ezl.periodicos.capes.gov.br/primo-explore/fulldisplay?docid=TN_cdi_doaj_primary_oai_doaj_org_article_db39009805164cd988adb1b9f50a7cff&context=PC&vid=CAPES_V3&lang=pt_BR&search_scope=default_scope&adaptor=primo_central_multiple_fe&tab=default_tab&query=any,contains,acessibilidade%20web&offset=0);
  - [Acessibilidade web em portais eletrônicos governamentais: panorama dos padroes universais e legislações brasileiras](https://revista.unitins.br/index.php/humanidadeseinovacao/article/view/2175).
