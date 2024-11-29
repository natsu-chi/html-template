# HTML Template
這是一個包含前端框架與套件的 HTML 範本，適合用來展示網頁設計和進行簡單的 Demo。

## 引入的套件
專案使用以下套件實現頁面佈局、圖片顯示：
* Bootstrap v5.3.3
* Bootstrap Icons v1.11.3
* jQuery v3.7.1
* Lightbox v2.11.4：顯示圖片的燈箱效果。
* Animate.css v3.7.2：CSS 動畫。
* Wow.js：CSS 動畫。

## 引用的外部資源
1. **Bootstrap** (CSS & JS)<br/>
    CSS 分成兩種方式引入，擇一就好：
    * 原生 CSS<br/>
        直接 link 引用
        ```
        <link rel="stylesheet" href="css/bootstrap.min.css">
        ```
    * Sass<br/>
        專案使用 npm 方式引用檔案，但也可使用檔案導入 + VSCode 的 Sass 編譯器套件編譯 (LiveSass complier)。
        
        需先下 `npm install`，安裝相依檔案。

        `node_modules/bootstrap/scss/_variables.scss` 可以修改變數，就可以將 Sass 編譯成 Css
        ```
        $ sass ./node_modules/bootstrap/scss/bootstrap.scss ./css/custom.css
        ```
        加上 `--watch` 可以執行 Sass 檔案監聽 (Ctrl+c 停止)
        ```
        sass --watch ./node_modules/bootstrap/scss/bootstrap.scss ./css/custom.css
        ```

        引用編譯完成 CSS
        ```
        <link rel="stylesheet" href="css/custom.css">
        ```
    JavaScript 引入
    ```
    <script src="js/bootstrap.bundle.js"></script>
    ```
2. **Bootstrap Icons**
    ```
    <link rel="stylesheet" href="css/icons/font/bootstrap-icons.min.css">
    ```
    來源路徑在 `css/icons`
    Icon class 名稱參考官方文件：https://icons.getbootstrap.com/
3. **jQuery**
    因為套件需求，專案使用完整版 jQuery
    ```
    <script src="js/jquery-3.7.1.min.js"></script>
    ```
4. **Lightbox**
    ```
    <link rel="stylesheet" href="css/lightbox.min.css">
    <script src="js/lightbox.min.js"></script>
    ```
    HTML 使用
    ```
    <body>
      <!-- 單張圖片 -->
      <a href="images/demo01.jpg" data-lightbox="set01" data-title="My caption">
        <img src="images/demo01.jpg" alt="" width="300px" />
      </a>
      <!-- 多張圖片 -->
      <a href="images/demo01.jpg" data-lightbox="set02">
        <img src="images/demo01.jpg" alt="" width="300px" />
      </a>
      <a href="images/demo02.jpg" data-lightbox="set02">
        <img src="images/demo02.jpg" alt="" width="300px" />
      </a>
      <script>
        lightbox.option({
          resizeDuration: 200,
          wrapAround: true,
        });
      </script>
    </body>
    ```
    官方文件說明：https://lokeshdhakar.com/projects/lightbox2/
5. **Animate.css**
    ```
    <link rel="stylesheet" href="css/animate.min.css" />
    ```
6. **Wow.js**
    需搭配 Animate.css
    ```
    <script src="js/wow.min.js"></script>
    ```
    HTML 使用
    ```
    <body>
      <div class="container">
        <div class="wow fadeInRight">
            Wow.js 文字動畫 Demo
        </div>
      </div>
      <script>
        new WOW().init();
      </script>
    </body>
    ```

