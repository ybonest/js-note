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

此例中，为所有元素绑定了点击事件，可见当子元素被点击时父元素的点击事件也被触发了，这就是事件冒泡

### 事件捕获
+ 定义：由外向内，父元素的事件会影响子元素的事件
