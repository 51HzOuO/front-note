### 使用 [uView 组件库-tabs](https://uviewui.com/components/tabs.html) + uni-app 内置的 [swiper 组件](https://uniapp.dcloud.net.cn/component/swiper.html) 实现页面内 tab 滑动切换

#### 1. 使用 uView-tabs 实现 tab 栏及当前 tab 名称的展示，swiper 实现 tab 内容切换

- `uView-tabs` 组件用于实现标签栏(tab)的展示，`swiper` 组件用于实现不同标签页内容的切换。
- `tabs` 组件提供了 `current` 属性，用于控制当前 tab 的索引。通过事件绑定，确保 `swiper` 的 `current` 属性与 `tabs` 的
  `current` 属性保持一致。

#### 2. 为每个 tab 页面抽象出一个独立的组件

- 每个 tab 页面可以被抽象为一个 `component` 组件，这样可以提高代码的可维护性。
- 组件之间通过 Vue2 的 `props` 实现数据的注入与展示。
- 使用内置的 `this.$emit` 方法进行事件传递。

示例参考 `Test02.vue`。

> 大部分内容都是组件库的使用, 注意保持 `tabs` 和 `swiper` 的 `current` 属性一致即可。

- 参考博客:
    - [uniapp制作简单的tab切换](https://blog.csdn.net/weixin_54721820/article/details/136322010)
    - [uniapp组件之tab选项卡滑动切换功能实现 vue2版本+vue3版本](https://blog.csdn.net/weixin_42220130/article/details/139411023)
