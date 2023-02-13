<template>
  <div class="hello">
    <h3>记事本</h3>
     <EditVue />
  </div>
</template>

<script>
import EditVue from './edit.vue';
export default {
  name: 'HelloWorld',
  components: {
    EditVue,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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

button {
  width: 300px;
 padding:5px 0;
 border-radius: 10px;
  margin-top: 30px;
  border: 0;
  color: #fff;
  background-color: #333;
}

h3 {
  margin: 0;
}
</style>
