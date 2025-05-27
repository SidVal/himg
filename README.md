# himg

Es muy loco que esto lo creé en el 2018, on Sep 24, 2018

## Limitaciones

Chrome notifica ciertos problemas con inyección del CSS en algunos sitios web que tienen políticas estrictas

Ejemplo:

![image](https://github.com/user-attachments/assets/d68ed390-30a2-40ec-a965-26da29a7681c)

Cuando esto ocurra, tendrás que ejecutar la carga directa del código en la consola del Chrome:

```JS
javascript:(function(){
  var s=document.createElement('style');
  s.innerHTML='figure>img[class*=progressiveMedia],figure>img[class*=image],div[class*=progressiveMedia],div[class*=widget],img,img.block,video,iframe{display:none!important}.lightbox,.thumbBlock{z-index:-1!important}img:not([style*="display: none"]),video:not([style*="display: none"]),iframe:not([style*="display: none"]){display:none!important}';
  document.head.appendChild(s);
})();


```
