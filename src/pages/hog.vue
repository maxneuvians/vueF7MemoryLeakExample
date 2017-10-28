<template id="hog">
  <f7-list>
    <f7-list-item v-for="number in data" :title="number"></f7-list-item>
  </f7-list>
</template>

<script>
export default {
  name: 'hog',
  template: '#hog',
  destroyed(){
    console.log("I have been destroyed")
  },
  data(){
    return {
      data: Array.apply(null, {length: 100}).map(Number.call, Number)
    }
  }
}
</script>
