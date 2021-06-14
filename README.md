# overflow:scroll;を使用した時に表示されるスクロールバーを非表示にする方法
「overflow:scroll;」を設定した時に表示されるスクロールバーを非表示する方法に関して書いていこうと思います。

```html
<div class="box">
  コンテンツ内容
</div>

<style>
  .box {
    height: 150px;
    overflow-y: scroll;
    /* IE, Edge 対応 */
    -ms-overflow-style: none;
    /* Firefox 対応 */
    scrollbar-width: none;
  }
  /* Chrome, Safari 対応 */
  .box::-webkit-scrollbar {
    display:none;
  }
</style>
```
