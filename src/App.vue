<template>
  <div id="app" class="wrapper">
    <div class="header">
      <div class="row inner">
        <div class="col-md-1">
        </div>
        <div class="col-md-10">
          <mainmenu></mainmenu>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="inner">
        <div class="raw scrollable">
          <div class="col-md-1">
          </div>
          <div class="col-md-10">
            <div class="page myDiv">
              <router-view></router-view>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="row inner">
        <div class="col-md-1">
        </div>
        <div class="col-md-10 bg">
          Nice Vuejs Application
          <br> Version 1.0 (C) 2017
        </div>
      </div>

    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
Vue.use(BootstrapVue)
// import VueImg from 'v-img'
// Vue.use(VueImg)
import 'bootstrap/dist/css/bootstrap.css'
// import 'bootstrap-vue/dist/bootstrap-vue.css'
import MainMenu from '@/components/MainMenu'
import Hello from '@/components/Hello'

export default {
  name: 'app',
  components: {
    mainmenu: MainMenu,
    hello: Hello
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /*margin-top: 3px;*/
}

.bg {
  background-color: #A9A9A9;
}

.lpad {
  padding-left: 10em;
  padding-right: 10em;
}

.page {
  display: block;
  text-align: center;
  font-size: 16px;
  color: #eee;
  border: 1px solid white;
}

.myDiv {
  height: 100%;
  max-height: calc(100vh - 50px);
  width: 100%;
  background-color: #FF0000;
}

html,
body {
  height: 100%;
  margin: 0;
}

.wrapper {
  height: 100%;
  width: 100%;
  display: table;
}

.header,
.content,
.footer {
  display: table-row;
}

.header,
.footer {
  background: lightgrey;
}

.inner {
  display: table-cell;
}

.content .inner {
  height: 100%;
  position: relative;
  background: lightgrey;
}

.scrollable {
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  overflow: auto;
}
</style>