## Welcome to my github page
***University of Bilibili, Class of 2027***

**Getting touch with:**

*Languages*
<div>
    <a href="https://developer.mozilla.org/en-US/docs/Web/javascript">
        <img src = "/image/logo-javascript.svg" alt="java-script-icon" width = "30" height="30">
    </a>
    <a href="https://developer.mozilla.org/en-US/docs/Web/HTML>">
        <img src = "/image/html-1.svg" alt="html-icon" width = "30" height="30">
    </a>
    <a href = https://developer.mozilla.org/en-US/docs/Web/CSS/Reference>
        <img src = "/image/css-3.svg" alt="css-icon" width = "30" height="30">
    </a>
    <a href="https://developer.apple.com/swift/">
        <img src = "/image/swift-15.svg" alt="swift-icon" width = "30" height="30">
    </a>
    <a href="https://dev.java">
        <img src = "/image/java-4.svg" alt="java-icon" width = "30" height="30">
    </a>
    <a href = "https://python.org">
        <img src="/image/python-5.svg" alt="python-icon" width="30" height="30">
    </a>
</div>

*Tech Stacks*
<div>
    <img src="/image/spring-3.svg" width="30" height="30">
    <img src="/image/vue-9.svg" width="30" height="30">
</div>

**Future plan**
<div>
    <img src = "image/cc.svg" width  = "30" height = "30">
    <img src="/image/c.svg" width = "30" height = "30">
</div>

-----------
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=EdwinZhanCN&langs_count=6)

**Beautiful logos are found here**
https://worldvectorlogo.com/
写了一个无缝滚动图片轮播的效果，想着纯css做简单点，所以没用js。代码如下：
<template>
<div class="scroll-view">
  <div class="scroll-section"
       v-for="(images) in [images1]"
       :key="images"
  >
    <div class="scroll-slide">
      <img v-show="response" v-for="image in images" :key="image" :src="image" alt="database-image"/>
    </div>
    <div class="scroll-slide">
      <img v-show="response" v-for="image in images" :key="image + '-copy'" :src="image" alt="database-image"/>
    </div>
  </div>
</div>
</template>

<style scoped>
*{
  margin:0;
  padding: 0;
}
.scroll-view{
  border-radius: 10px;
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-gap: 10px;
  margin-top: 20px;
  margin-bottom: 20px;
  animation: trans 8s ease-in-out;
}

.scroll-section{
  overflow: hidden;
  white-space: nowrap;
}

.scroll-slide img{
  width: 220px;
  height: 220px;
  margin-left: 10px;
}

.scroll-slide{
  will-change: transform;
  display: inline-block;
  animation: 20s slide infinite linear;
}

@keyframes slide {
  from {
    transform: translate3d(0, 0, 0);
  }
  to {
    transform: translate3d(-100%, 0, 0);
  }
}

</style>

我设置了`animation: 20s slide infinite linear;`, 动画结束时两个相同的轮滚模块整体回移来达成无缝的滚动效果。我知道这可能有延迟，但出乎我意料的是只有使用Safari时，动画结束整个元素会闪烁一下，而使用chrome和edge则不会。这是渲染逻辑不同导致的吗？有没有比较简单的方法来消除这个闪烁的问题，求大佬解答。

类似在Safari上CSS我遇到卡顿的还有`background-attachment: fixed;`属性，体验极差

