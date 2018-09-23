# OneQRCode
微信、支付宝、QQ 三合一收款二维码（单页版）

## 注意事项

 - 使用前将 `index.html` 中的收款链接改成你自己的；
 - 请用专门的 Html 编辑器(如 notepad++)进行编辑，切勿直接用记事本编辑，否则可能出现中文乱码！
 - 请将 `index.html` 上传至你的网站空间使用。直接在本地打开将无法运行；
 - 本作品禁止任何形式的倒卖，转载请注明出处。

## 原理
在 微信、支付宝、QQ 中扫描到一个网址二维码后，一般会通过内置的浏览器打开这个网址。通过判断内置浏览器的 UA，即可得出当前扫码的具体支付平台。

````
if(navigator.userAgent.match(/Alipay/i)) {
    // 支付宝
} else if(navigator.userAgent.match(/MicroMessenger\//i)) {
    // 微信
} else if(navigator.userAgent.match(/QQ\//i)) {
    // QQ
} else {
    // 其它
}
````

其中，支付宝可以通过直接跳转收款链接唤起付款功能，而 QQ、微信 则需展示出对应的收款码，由用户自行长按识别真正的收款二维码实现唤起付款。

详细请阅读：

[多合一收款二维码原理及实现](https://mkblog.cn/922/)

[详细使用说明请查阅项目wiki](https://github.com/mengkunsoft/OneQRCode/wiki)

# License

````
MIT License

Copyright (c) 2018 mengkun

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
````