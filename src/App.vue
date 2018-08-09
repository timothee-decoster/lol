<template>
  <div id="app">
    <router-view/>
    <Sidebar/>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar';

export default {
    name: 'App',
    components: {
        Sidebar
    }
};
</script>

<style>
body {
    font-family: 'Helvetica Neue', Arial, sans-serif;
    color: #fff;
    background-color: #2c3e50;
    -webkit-font-smoothing: antialiased;
}

* {
    box-sizing: border-box;
}
</style>
