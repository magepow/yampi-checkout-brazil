[<img src="https://github.com/magepow/themeforest/blob/master/shopify/shopify_affiliate.jpg" >](https://shopify.pxf.io/VyL446)

## Yampi Checkout Integration with Shopify

#### This guide integrater Yampi Checkout Brasil with shopify dropshipping use theme dev by Alothemes

**[Our Shopify Themes](https://themeforest.net/user/alotheme)**

* [Uminex - Fastest Shopify 2.0 Theme](https://1.envato.market/c/1314680/275988/4415?u=https://themeforest.net/item/uminex-fastest-shopify-20-theme/46350215)

* [Dukamarket - Multipurpose Shopify Theme](https://1.envato.market/c/1314680/275988/4415?u=https://themeforest.net/item/dukamarket-multipurpose-shopify-theme/36158349)

* [Davici - Multipurpose Shopify Theme](https://1.envato.market/c/1314680/275988/4415?u=https://themeforest.net/item/davici-ultimate-shopify-2-theme-rtl-supported/41949840)


<!-- * [Demo](https://easyshopp.me) -->
* [Checkout Page](https://seguro.easyshopp.me)
* [Checkout Page](https://seguro.ultillix.com)
* [Como desinstalar o Checkout da Yampi no Shopify?](https://help.yampi.com.br/pt-BR/articles/6067083-como-desinstalar-o-checkout-da-yampi-no-shopify)
* [Docs](https://help.revy.io/article/16-yampi-checkout)

### Setup step by step:

#### Step 1: Add file snippets/YampiSnippet.liquid in this repository to snippets/YampiSnippet.liquid your theme.

* [Click to view YampiSnippet.liquid](https://github.com/magepow/yampi-checkout-brazil/blob/main/snippets/YampiSnippet.liquid)

#### Step 2: Add code below to file layout/theme.liquid below close body tag

```
<!-- Não remova. Checkout Yampi. -->
{% capture yampi_snippet_content %}{% include 'YampiSnippet' %}{% endcapture %} {% unless yampi_snippet_content contains 'Liquid error' %} {% include 'YampiSnippet' %} {% endunless %}
<!-- Não remova. Checkout Yampi. --> 
```

#### Step 3: Add code below to file assets/jquery.custom.js

```
$('body').on('ajax:addToCart', function (e, data) {
    /*
    console.log(data.form);
    console.log(data.response);
    */
    if(typeof yampiClick === 'function') {
        yampiClick();
    }
});
```

### Guide step by step via images:

#### Step 1:
![Add to directory snippets](https://github.com/magepow/yampi-checkout-brazil/blob/main/media/snippet.png)


#### Step 2:
![Add to layout/theme.liquid](https://github.com/magepow/yampi-checkout-brazil/blob/main/media/yampi_snippet.png)

#### Step 3:
![Add to file assets/jquery.custom.js](https://github.com/magepow/yampi-checkout-brazil/blob/main/media/yampi_ajaxcart_callback.png)
