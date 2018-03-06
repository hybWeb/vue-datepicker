<template>
  <div id="app">
    <VueDatePicker v-model="time" placeholder="请选择开始日期" format="YYYY-MM-DD HH:mm"  :disabled-date="disabledDate"  showButtons @confirm="confirm" clearable />
  </div>
</template>

<script>
import VueDatePicker from './components/date-picker/VueDatepickerLocal'
export default {
  name: 'App',
  components: {
    VueDatePicker
  },
  data () {
    return {
      time: new Date()
    }
  },
  methods: {
    confirm () {
      console.log(this.time)
    },
    disabledDate (time) {
      var myDate = new Date()
      return time > myDate.getTime()
    }
  }
}
</script>

<style></style>
