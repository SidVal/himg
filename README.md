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

### Botón HTML (directo)

```html
<a href="javascript:(function()%7Bjavascript%3A(function()%7B%0A%20%20var%20s%3Ddocument.createElement('style')%3B%0A%20%20s.innerHTML%3D'figure%3Eimg%5Bclass*%3DprogressiveMedia%5D%2Cfigure%3Eimg%5Bclass*%3Dimage%5D%2Cdiv%5Bclass*%3DprogressiveMedia%5D%2Cdiv%5Bclass*%3Dwidget%5D%2Cimg%2Cimg.block%2Cvideo%2Ciframe%7Bdisplay%3Anone!important%7D.lightbox%2C.thumbBlock%7Bz-index%3A-1!important%7Dimg%3Anot(%5Bstyle*%3D%22display%3A%20none%22%5D)%2Cvideo%3Anot(%5Bstyle*%3D%22display%3A%20none%22%5D)%2Ciframe%3Anot(%5Bstyle*%3D%22display%3A%20none%22%5D)%7Bdisplay%3Anone!important%7D'%3B%0A%20%20document.head.appendChild(s)%3B%0A%7D)()%3B%7D)()%3B">Direct-Hide-IMGs</a>
```

`-- >` <a href="javascript:(function()%7Bjavascript%3A(function()%7B%0A%20%20var%20s%3Ddocument.createElement('style')%3B%0A%20%20s.innerHTML%3D'figure%3Eimg%5Bclass*%3DprogressiveMedia%5D%2Cfigure%3Eimg%5Bclass*%3Dimage%5D%2Cdiv%5Bclass*%3DprogressiveMedia%5D%2Cdiv%5Bclass*%3Dwidget%5D%2Cimg%2Cimg.block%2Cvideo%2Ciframe%7Bdisplay%3Anone!important%7D.lightbox%2C.thumbBlock%7Bz-index%3A-1!important%7Dimg%3Anot(%5Bstyle*%3D%22display%3A%20none%22%5D)%2Cvideo%3Anot(%5Bstyle*%3D%22display%3A%20none%22%5D)%2Ciframe%3Anot(%5Bstyle*%3D%22display%3A%20none%22%5D)%7Bdisplay%3Anone!important%7D'%3B%0A%20%20document.head.appendChild(s)%3B%0A%7D)()%3B%7D)()%3B">Direct-Hide-IMGs</a>
