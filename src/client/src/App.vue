<template>
  <div id="app">
    <component :is="layout">
      <router-view />
    </component>
  </div>
</template>

<script>
export default {
  name: 'App',
  computed: {
    layout() {
      return (this.$route.meta.layout || 'default') + '-layout';
    }
  }
};
</script>

<style>
#app,
body,
html,
.container-fluid {
  height: 100%;
}
</style>
