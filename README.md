
#jquery.pagination.js
##JS分页插件： 简单、易用、轻量级


在线演示：[http://www.byex.cn/jquery.pagination](http://www.byex.cn/jquery.pagination/)

Written by: hishion

##使用步骤

###Step 1: 引入资源文件


```html
<div class="pagination"></div>

<!-- mbSlider Javascript file -->
<script src="jquery.pagination.js"></script>
```


###Step 2: 调用 mbUploadify 

```javascript
$('.pagination').pagination({
    total: 100,
    onJump: function(index){
        console.log(index);
    }
}); 
```

##配置项

以下为全部配置项
```
$('.pagination').pagination({
    /*总页数*/
    total: 0,
    /*每页条数*/
    row: 10,
    /*最大页码量,调这个值分页页码数量会变化*/
    num: 2,
    /*当前页索引*/
    current: 1,
    /*
        自定义分页模板
        first, last, prev, next 请保证 data-index 值正确否则click事件无响应
        item 必须有，其它可选
    */
    template: {
        first:'<li class="first" data-index="first"><a href="javascript:;">首页</a></li>',
        last: '<li class="last" data-index="last"><a href="javascript:;">最后一页</a></li>',
        prev: '<li class="prev" data-index="prev"><a href="javascript:;">上一页</a></li>',
        next: '<li class="next" data-index="next"><a href="javascript:;">下一页</a></li>',
        ellipsis: '<li class="ellipsis" data-index="ellipsis"><a href="javascript:;">...</a></li>',
        item: '<li class="page-{{dataIndex}}" data-index="{{dataIndex}}"><a href="javascript:;">{{index}}</a></li>',
        wrapElement: 'ul'
    },
    /*回调 $.noop.call(this, current, context);*/
    onJump: $.noop
}); 
```

