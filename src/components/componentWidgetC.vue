<template>
  <div>
    <h3>Widget C</h3>
    <pre>{{ widgetData }}</pre>
  </div>
</template>
<script>
export default {
  name: 'WidgetC',
  props: ['widgetData']
}
</script>
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>