js执行顺序问题，script标签写在上边的先执行，所以你的代码要放到你引入jquery的后边，同时你这样写的话，你的js是先执行的，但是你的button这时候还不存在，你放到后边，前面的html加载完js就能找到了

  


如果你非要放在head里的话，把你的代码放到window.onload里边

```js
window.onload=function(){


你的

js代码



}


或者用jquery的


$(document).ready(function(){


你的

js代码



})

```



  


