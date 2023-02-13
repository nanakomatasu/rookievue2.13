<template>
  <div class="edit">
       <p>日期：</p>
       <input type="date" v-model='date'>
       <p>时间:</p>
       <input type="time" v-model="time">
       <p>事件:</p>
       <input type="text" v-model="text">
  <ItemVue :date="date" :time="time" :text="text"/>
  </div>
</template>
<script>
import ItemVue from './item.vue';
export default {
    name: "EditVue",
    data() {
        return {
            date: "",
            time: "",
            text: "",
        };
    },
    components: { ItemVue }
}
</script>
<style>
.edit {
  text-align: left;
}

.edit input {
  width: 100%;
}

.add {
  height: 20px;
  color: #fff;
}

</style>