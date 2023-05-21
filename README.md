# css-reset

CSS 样式重置目的是为了保证元素在各个浏览器中样式的一致性。
这里记录为什么要设置这些属性的原因，都是询问 ChatGPT 的，😄！
当然问的都是我想知道的内容，已经知道的正经人谁去问啊。

为什么要使用 css-reset，当然是前端 ui 库现在不提供默认的全局样式重置啊。

`-webkit-text-size-adjust: 100%;`是一个用于调整移动设备上文本大小的 CSS 属性。它适用于使用 WebKit 内核的浏览器（如 Safari 和 Chrome）。
这个属性的作用是防止浏览器自动调整移动设备上的文本大小，以保持一致的显示效果。移动设备通常会根据视口大小和分辨率自动调整文本大小，以提供更好的可读性和用户体验。然而，有时这种自动调整可能会导致开发者所期望的文本大小失真。
通过将 -webkit-text-size-adjust 设置为 100%，你告诉浏览器不要自动调整文本大小，而是保持文本在其原始大小上的显示。
`font-feature-settings`是一个用于控制字体特征（font features）的 CSS 属性。它允许你激活或禁用字体中的特定功能，例如连字（ligatures）、小型大写（small caps）、数字格式（numeral styles）等。
具体来说，font-feature-settings 属性接受一个字符串值，用于指定要应用的字体特征。常见的值包括以下几种：

- "normal": 禁用所有字体特征，使用字体的默认设置。
- "inherit": 继承父元素的字体特征设置。
- "unset": 重置字体特征设置为默认值。
- "initial": 将字体特征设置为初始值。

`font-variation-settings`是一个用于控制可变字体（variable fonts）的 CSS 属性。可变字体是一种特殊类型的字体，可以通过调整轴（axes）来实现在字体设计空间内的无限变化。

## QA

给 html 设置 font-family 结果导致在 chrome 和 safari 字体高度不一致，难绷。
chrome 用的是 PingFangSC
safari 用的是 AppleSystemUIFont

`line-height`是可继承属性，给 html 元素设置 line-height 会被 body 继承吗？
A:不同的浏览器可能会有自己的默认样式，其中包括 line-height 的值。这些默认样式可能会在 html 和 body 元素上设置不同的 line-height 值，导致二者不完全继承。所以说给 body 设置 line-height:inherit 是避免浏览器默认样式引起的问题，继承权重最低。
表单相关元素的字体需要主动设置一下，因为浏览器会为其设置字体。
