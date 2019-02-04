# Form Drass

> site para roupas feminias - form-drass

### Documentação para o Bootstrap 2

link para pesquisa: 
* [Loja Integrada](https://fordressandlove.lojaintegrada.com.br/documentacao)
* [Boostrap 2.0](https://getbootstrap.com/2.3.2/)

### Estrutura(_HTML_)

```html
<!-- cabeçalho -->
<div id="cabecalho">
    <div class="conteiner">
        ...
    </div>
</div>

<!-- secao-banners -->
<div class="secao-banners">
    <div class="conteiner">...</div>
</div>

<!-- body -->
<div id="corpo">
    <div class="conteiner">
        ...
    </div>
</div>

<!-- footer -->
<div id="rodape">
    <div class="conteiner">
        ...
    </div>
</div>
```

* `.container` - container da aplicação. Que tem:
  
  * `.tema-escuro` - background-color: #323232;
  
  * `.tema-transparente` - background-color: transparent;
  
  * tamanho fixo: 980px
  
  * tamanho minimo: 970px
  
  * tamanho máximo: 1140px
  
  traduzindo seria:

  ```css
    .container{
        min-width: 970px;
        max-width: 1140px;
    }
  ```

### Classes

Todas as páginas de loja são especificadas por uma classe referente ao seu contéudo.   
  * `.pagina-cadastro`
  
  * `.pagina-carrinho`
  
  * `.pagina-categoria`
  
  * `.pagina-conta`
  
  * `.pagina-finalizacao`
  
  * `.pagina-inicial`
  
  * `.pagina-marca`
  
  * `.pagina-produto`

para poder usar você adiciona a classe no `body`

```html
<body class="pagina-categoria categoria-nome-da-categoria"> 
...
</body>
```

> Alem das classes de página, existem também as classes específicas de `categoria, marca ou produto`. 

##### Listagem

Listagem de produtos

```html
<!-- toda listagem -->
<div class="listagem">
    <ul>
        <!-- linha de produtos -->
        <li class="listagem-linha">
            <ul class="row-fluid">
                <li class="span4">
                    <!-- cada produto -->
                    <div class="listagem-item">...</div>
                </li>
            </ul>
        </li>
    </ul>
</div>
```

#### Menu

Menu possui uma hierarquia: {`.nivel-um`,`.nivel-dois`,`.nivel-tres`}. Categoria possui um __ID__ especifico. que permite customizar os menus individualmente. 

```html
<div class="menu superior">
    <ul class="nivel-um">
        <li class="categoria-id-xxx">
            <a href="nome-da-categoria.html">...</a>
            <ul class="nivel-dois">...</ul>
        </li>
    </ul>
</div>
```

### @Widgets

adicionar botão na página

```html
<!-- botão padrão -->
<button class="botao"> ... </button>

<!-- cor principal  -->
<button class="botao principal"> ... </button>

<!-- pequeno -->
<button class="botao principal pequeno"> ... </button>

<!-- grande -->
<button class="botao principal grande"> ... </button>

<!-- icone -->
<button class="botao"><i class="icon-remove"></i>Botão com ícone</button>

```

##### Extensão

São utilizados algum plugins pré-definidos:

* [`Flexslider`](http://flexslider.woothemes.com/) - para fazer o carrosel

``` html
<div class="banner">
    <div class="flexslider">
        <ul>
            <li>
                <img src="img/banner01.jpg" alt="imagem">
                <p class="info-banner titulo"> Lorem ipsum dolor si</p>
            </li>
        </ul>
    </div>
</div>
```

mais adição: 

```js
$(window).load(function() {
  $('.flexslider').flexslider({
    animation: "slide"
  });
});
```

* [`ImageZoom`](http://preview.codecanyon.net/item/imagezoom-responsive-jquery-image-zoom-plugin/full_screen_preview/4805256) - para zoom e carrosel de minaturas.

### Css

Para poder utilizar as cores defindas no editor, você pode ter as seguintes classes:

* fundo-principal
* cor-principal
* borda-principal


##### TipoGrafia

* ##### Titulos
    Os textos de destaque na loja são: 
        1. preço
        2. nome do produtos
        3. menus
        4. titulos
        5. categorias
    todos eles são definidos pela classe: `.titulo`.

    ```css

    .titulo{
        font-family: 'Oswald', Arial, sans-serif;
        font-weight: 400;
    }

    ```

    adicionando o uso

    ```html
    <h4 class="titulo cor-principal"> ... </h4>
    ```
 * ##### Fonte Global
    ```css
    
    body{
        font-size: 'Open Sans', sans-serif;
        font-size: 12px;
        // pode ser alterado
        font-color: #666;
    }

    ```

