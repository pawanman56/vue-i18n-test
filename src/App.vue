<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloI18n/>
</template>

<script>
import HelloI18n from './components/HelloI18n'

export default {
  name: 'App',

  components: {
    HelloI18n
  },

  created () {
    const locale = localStorage.getItem('locale');

    if (locale) this.$i18n.locale = locale;
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.btn {
  display: inline-block;
  font-weight: 600;
  color: #1B1C1D;
  text-align: center;
  vertical-align: middle;
  user-select: none;
  background-color: transparent;
  border: 1px solid;
  padding: 0.25rem 0.5rem;
  font-size: 0.875rem;
  line-height: 1.5;
  border-radius: 0.2rem;
  margin-left: 0.25rem;
  margin-right: 0.25rem;
}

.btn:hover {
  cursor: pointer;
}
</style>
