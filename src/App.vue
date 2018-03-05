<template>
  <div id="app">
    <vue-datepicker-local v-model="time" placeholder="请选择开始日期" format="YYYY-MM-DD HH:mm"  :disabled-date="disabledDate"  showButtons @confirm="confirm" clearable />
  </div>
</template>

<script>
  import VueDatepickerLocal from './components/VueDatepickerLocal';

export default {
  name: 'App',
  components: {
    VueDatepickerLocal,
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
