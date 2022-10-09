# dynamic expose module:
监控DOM元素是否曝光在可视区,  基于window.IntersectionObserver 实现，摒弃scroll的方式，理论上性能会好一些。不用绑定很多的滚动监听，在不支持的环境里会降级成scroll，使用者不用担心兼容性问题
### example:
```
import dyncExpose from 'dync_expose';
const exposeId = 'my_dom_isRepeat';  // If the id contains 'isRepeat', repeated exposure after the callback will still trigger the callback;

dyncExpose({
  id: exposeId, // id it means your dom's id,  and Id is the only one on this page;
  target: document.querySelector('xxx'),
  parent: null,  // null, it means document.body;
  cb() {
    // If the element is exposed, the callback function will be triggered
  },
});

<div id="my_dom_isRepeat">xxx</div>
```

