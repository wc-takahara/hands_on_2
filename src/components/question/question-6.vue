<template>
  <!-- 問題 問題4で削除ボタンをページの先頭に置きましたが、
            リスト内に削除ボタンを置いて、削除ボタンを押したら、そのリストを削除できるようにしましょう。-->
  <!-- 使うもの v-on -->
  <div>
    <ul>
      <li v-for="(list, index) in lists" v-bind:key="list.id">
        <span v-bind:class="[list.position =='部長'?'isBold':'isNormal']">{{index}}番目 {{list.name}}<button>削除</button></span>
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
    deleteList: function(index) {
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
