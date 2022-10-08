# dynamic expose module:

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

