## absolute绝对定位
absolute会使元素脱离文档流，不占据文档空间，absolute的位置相对于最近的有定位的父元素（即使用的left，top等都是相对于最近的有定位的父元素），width和height也是相对最近的有定位的父元素，如下示例
```html
<div style="width: 480px; height: 300px; position: fixed;">
    <!-- w-100 h-100 表示宽度高度 100% -->
    <a class="w-100 h-100" style="position: absolute;">
        <div>
            <div style="width: 100%; height: 100%; position: absolute;">
                测试 div
            </div>
        </div>
    </a>
</div>
```
测试 div的宽高是 480，300

## relative相对位置
relative占据文档空间，relative的位置相对于其原来所在位置（即使用的left，top等都是相对于其原来的位置），width和height则是相对于父元素

## fixed固定定位
fixed会使元素脱离文档流，不占据文档空间，fixed的位置相对于浏览器（这是是fixed与absolute的区别）（即使用的left，top等都是相对于浏览器，如top: 500px，那么他距离浏览器上边界为500px），width和height也是相对与浏览器