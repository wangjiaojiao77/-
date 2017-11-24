# 移动端滚动穿透

```
// 弹窗弹出的时候，固定body
function fixedBody(){
    var scrollTop = document.body.scrollTop || document.documentElement.scrollTop;
    document.body.style.cssText += 'position:fixed;top:-'+scrollTop+'px;';
}

// 弹窗关闭时，恢复body
function looseBody() {
    var body = document.body;
    body.style.position = '';
    var top = body.style.top;
    document.body.scrollTop = document.documentElement.scrollTop = -parseInt(top);
    body.style.top = '';
}
```
