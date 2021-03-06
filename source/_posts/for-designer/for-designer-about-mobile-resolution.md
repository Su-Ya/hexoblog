---
title: 如何取得手機版面的設計解析度
date: 2017-06-29 15:43:10
tags: '團隊溝通技巧'
categories: '給平面設計師的'
---

# 給平面設計師的: 如何取得手機版面的設計解析度

![](https://i.imgur.com/UvHo0gv.png)

在一般的情況，同一個型的手機可以得到兩種顯示規格。
下面來介紹一下兩種規格取得的方式以及它們的差異。

## 使用前端的「手機模擬器」

由於手機的螢幕解析度有Retina，它是一種針對文字可以精細化。
但是這樣的規格並不適合用在網頁設計，字會太小。

### 手機官網
![](https://i.imgur.com/UddGE6H.png)

### Chrome模擬器
1. 開啟瀏覽器
2. 打開「開發者模式」(滑鼠右鍵: 選「檢查」)
3. [啟動「手機模擬器」](https://developers.google.com/web/tools/chrome-devtools/device-mode/)
4. [找出你要模擬的手機型號](https://developers.google.com/web/tools/chrome-devtools/device-mode/emulate-mobile-viewports)
5. 即可在旁邊看見它的解析度

![](https://i.imgur.com/PVP60Wv.png)

:::info
官網規格 iPhone6: 1334×750
Chrome模擬器規格 iPhone6: 667×375 ~(為了方便和官方技術規格對照，長邊放前面)~
:::

## 渲染解析度、物理解析度^[[浅谈iOS屏幕适配](http://liumh.com/2015/10/21/ios-image-related-matching/)]

> 渲染: 網頁呈現過程的一種瀏覽器處理方式

渲染解析度是為了讓小螢幕上保持內容可讀性而設計的。讓使用者在小螢幕，高解析的情況之下，也可以看得見文字的清析度。

但是這和平設計師無關呀！這是工程師的事！
對！這是瀏覽器開發和手機開發工程師的事，也不是前端工程師的事。

我們只是在他們開發出來的基礎上進行創作行為。
所以和平面設計師、前端工程師有關的是「要用什麼解析度開規格」!!

要使用渲染解析度

> 以iPhone6為例
官網規格是物理解析度: 1334×750
Chrome模擬器規格是渲染解析度: 667×375

可以將「物理解析度」除以「渲染解析度」即可得到畫面的渲染原則

> 以iPhone6為例
寬度: 1334 ÷ 667 = 2
高度: 750 ÷ 375 = 2
所以瀏覽器以四個pixel圍成的正方形當作一個pixel給顯示訊號。
