<template>
  <div class="item">
    <button class="add" @click="add">添加</button>
    <ul>
      <li v-for="(item,index) in list" :key="item.id">{{ item.date }}{{ item.text }}{{ item.time }}<button @click="remove(index)">删除</button></li>
    </ul>
    </div>
</template>
<script>
export default {
  name :'ItemVue',
  props: ['date','time','text'],
  data(){
    return {
      list: [],
    }
  },
methods: {
  remove(index){
      this.list.splice(index, 1);
    },
    add(){
     this.list.push({date:this.date,text:this.text,time:this.time})
    }
}}
</script>
<style>
.item {
  margin-top: 20px;
  text-align: left;
}

li {
  display: flex;
  list-style: none;
  justify-content: space-between;
  margin-bottom: 10px;
}

li button {
   border: 0;
   background-color: red;
   border-radius:5px;
   color: #fff;
}

.add{
width: 100%;
margin: 0 auto;
border: 0;
border-radius: 10px;
background-color: #333;
color: #fff;
}

</style>