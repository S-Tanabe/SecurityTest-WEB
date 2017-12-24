<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
html {
  background-color: #000;
  color: #ff8f8f;
  font-family: Fantasy, Source Code Pro,sans-serif,ヒラギノ角ゴシック Pro,Hiragino Kaku Gothic Pro,メイリオ,Meiryo,Osaka,sans-serif;
  line-height: 2;
}

#title {
  background-color: #882F2F;
  color: #FFF;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /*color: #2c3e50;*/
  margin-top: 60px;
}
</style>
