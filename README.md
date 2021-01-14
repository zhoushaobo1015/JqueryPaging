# JqueryPaging
一个JQuery的分页插件
### [原地址](https://www.jq22.com/jquery-info23323)

 ```
/**
 * layout 参数说明：
 * 
 * total： 总条数
 * sizes: 显示每页条数选择框， TODO:pageSizes参数必填,否则无法生效
 * home： 首页按钮
 * prev： 上一页按钮
 * pager： 页码
 * last： 尾页按钮
 * next： 下一页按钮
 * jumper： 输入框跳转（包含事件：失去焦点，回车）触发
 * 
 * */
 

new Pagination({
    element: '#pages', // 渲染的容器  [必填]
    type: 1, // 样式类型，默认1 ，目前可选 [1,2] 可自行增加样式   [非必填]
    layout: 'total, sizes, home, prev, pager, next, last, jumper', // [必填]
    pageIndex: 1, // 当前页码 [非必填]
    pageSize: 10, // 每页显示条数   TODO: 如果使用了sizes这里就无须传参，传了也无效 [必填]
    pageCount: 9, // 页码显示数量，页码必须大于等于5的奇数，默认页码9  TODO:为了样式美观，参数只能为奇数， 否则会报错 [非必填]
    total: 1000, // 数据总条数 [必填]
    singlePageHide: false, // 单页隐藏， 默认true  如果为true页码少于一页则不会渲染 [非必填]
    pageSizes: [5, 20, 30, 40, 50], // 选择每页条数  TODO: layout的sizes属性存在才生效
    prevText: '上一页', // 上一页文字，不传默认为箭头图标  [非必填]
    nextText: '下一页', // 下一页文字，不传默认为箭头图标 [非必填]
    ellipsis: true, // 页码显示省略符 默认false  [非必填]
    disabled: true, // 显示禁用手势 默认false  [非必填]
    currentChange: function(index, pageSize) { // 页码改变时回调  TODO:第一个参数是当前页码，第二个参数是每页显示条数数量，需使用sizes第二参数才有值。
        console.log(index, pageSize);
    }
});
```
