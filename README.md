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

overflowをかけている要素の「-ms-overflow-style: none;」「scrollbar-width: none;」を指定するだけで対応可能です。Chrome, Safariまで対応する場合は「::-webkit-scrollbar」に「display:none;」を指定します。

基本的には「IE, Edge 対応」までの指定をしておけば問題ないかと思います！

以上、スクロールバーを非表示にする方法でした。時にはスクロールバーがあった方が良い場面もありますが、UIとデザインのバランスを考慮して、削除するか判断してみてください。是非参考になれば幸いです。
