### 事件冒泡
+ 定义：由里向外，子元素事件的触发会影响父元素的事件

实例[(链接)](http://ybo.codenest.top/js-note/html/bubble.html)
<iframe style="overflow:hidden;height:400px;width:100%;border:1px solid #ccc" class="yboflag" src="html/bubble.html"></iframe>


+ 取消事件冒泡
```
function stopBubble(e){
  if(e&&e.stopPropagation){
    e.stopPropagation();  //非IE
  }else{
    window.event.cancelBubble = true;
  }
}
```

### 事件捕获
+ 定义：由外向内，父元素的事件会影响子元素的事件
