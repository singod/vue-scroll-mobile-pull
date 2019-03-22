# vue-scroll H5 滚动组件支持下拉刷新和上拉加载更多

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

## 示例

<img src="http://img2.jpjie.com/h5/1fq66vw1k2wj20p00goq7n.gif"/>

## 使用方法

```vue

<template>
  <div id="app">
    <scroll ref="scroll"
            :data="listData"
            @onScroll="onScroll"
            @pullingUp="onScrollBottom"
            @pullingDown="onPullingDown">
      <div class="list">
        <div class="item" v-for="(item, index) in listData" :key="index">
        </div>
      </div>
    </scroll>
  </div>
</template>

## 配置说明
| 参数     | 类型     | 描述 | 必需 | 默认值 |
| :------------- | :------------- | :------------- | :------------- | :------------- |
| data         | array      | 滚动列表渲染的数据 | 是 | [] |
| onScroll         | function      | 监听列表滚动 | 否 | |
| pullingUp         | function      | 滚动到底部加载更多触发 | 否 |  |
| pullingDown         | function      | 下拉刷新回调方法 | 否 |  |