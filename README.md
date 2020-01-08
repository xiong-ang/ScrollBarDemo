# Scroll Bar Skills

## How to display ScrollBar
```css
overflow-x: auto;
overflow-y: auto;
overflow: auto;
```

## How to display scrollbar in Complex case
* 当复杂case中scroll出现问题时，可以在容器中加一个<随意大小>子元素，然后，由子元素容纳其他内容。

## How to scroll to bottom by js
### 返回顶部 
```js
    element.scrollTop = 0
```
### 滚到底部
```js
    element.scrollTop = element.scrollHeight - element.clientHeight
```
## Load data when scrolling to bottom   
### 判断是否到底部
```js
element.scrollHeight - element.scrollTop === element.clientHeight
```
### 到达底部时加载   
```js
window.onscroll = () => {
  if (!this.isLoading && this.isCanLoad) {
    let scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
    let windowHeight = document.documentElement.clientHeight || document.body.clientHeight;
    let scrollHeight = document.documentElement.scrollHeight || document.body.scrollHeight;
    if (scrollHeight - scrollTop - windowHeight < 30) {
      this.loadMore();
    }
  }
}；
```

[Reference](https://www.cnblogs.com/wenruo/p/9754576.html)