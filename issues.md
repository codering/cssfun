### CSS 老中医，专治各种疑难杂症

静静地看我吹牛逼....

#### 移除 texteare 下多余的padding

- 诊断：项目中发现 textarea 底部总会都 5px 左右的padding
- 配方：

    ```css
    textarea {
        vertical-align: bottom;
    }
    ```

    使用 display: block; 也行。。。 研究下

#### 移除 IE 10 及以上 input 自带的 clear button 以及 type="password" 带有的 icon

- 诊断：
  
    ![rm](https://cloud.githubusercontent.com/assets/6628666/9102004/3c4d6cb2-3c20-11e5-9c6f-613e71d992bc.png)

- 配方：

    ```css
    ::-ms-clear {
       display: none;
    }

    ::-ms-reveal {
       display: none;
    }
    ```

    see more:
    - http://stackoverflow.com/questions/14007655/remove-ie10s-clear-field-x-button-on-certain-inputs
    - http://msdn.microsoft.com/en-us/library/windows/apps/hh465740.aspx

#### display: inline-block 元素之间的间距移除

see solution at:
- <https://css-tricks.com/fighting-the-space-between-inline-block-elements/>
- <http://www.zhangxinxu.com/wordpress/2012/04/inline-block-space-remove-%E5%8E%BB%E9%99%A4%E9%97%B4%E8%B7%9D/>

#### IE8 实现兼容 rgba

  - 解决方案：

  1. http://www.liuhaihua.cn/archives/9256.html  DXImageTransform.Microsoft.gradient

  2. less 解决 http://www.lesscss.net/functions/#color-definition-argb-color-

#### safari 下 transition 引起的闪烁问题

- 加个 ` transform: translate3d(0, 0, 0);`
