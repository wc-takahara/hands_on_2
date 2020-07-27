<template>
  <div>
    <button v-on:click="deleteList">削除</button>
    <ul>
      <li v-for="list in lists" v-bind:key="list.id">
        <span v-bind:class="[list.position =='部長'?'isBold':'isNormal']">{{list.name}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data:function() {
    return {
      lists: [
        {id:1, name:"山田", position:"部長"},
        {id:2, name:"田中", position:"平社員"},
        {id:3, name:"木村", position:"平社員"},
        {id:4, name:"加藤", position:"平社員"},
        {id:5, name:"山下", position:"平社員"},
      ],
    }
  },
  methods: {
    deleteList: function() {
      this.lists.pop();
    }
  }
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
  display: block;
  margin: 0 10px;
}
span.isBold {
  font-weight: bold;
}
a {
  color: #42b983;
}
</style>
