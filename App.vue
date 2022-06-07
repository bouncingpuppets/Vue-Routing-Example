<template>
  <div id="app">
    <router-link class="link" :to="{ path: '/hello', query: { name: 'Roo' } }"
      >Say hello</router-link
    >
    <router-link class="link" :to="{ path: '/goodbye', query: { name: 'Roo' } }"
      >Say goodbye</router-link
    >
    <br />
    <router-view>
      <p slot="test-hello">SLOT TEST HELLO!!!</p>
      <p slot="test-goodbye">SLOT TEST GOODBYE!!!</p>
    </router-view>
  </div>
</template>

<script>
export default {
  name: "app",
};
</script>

<style>
#app {
  margin: 60px;
}

.link {
  display: inline-block;
  padding: 10px;
}

.router-link-active {
  color: green;
}
</style>