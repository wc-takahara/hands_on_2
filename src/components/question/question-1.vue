<template>
  <!-- 問題 用意してあるデータをv-forを使って表示してください(キー は id)表示するのは、名字だけで大丈夫です。 -->
  <!-- 使うもの v-for v-bind -->
  <div>
    <ul>
      <li>
        <span><!-- ここに名字が表示されるように --></span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data:function() {
    return {
      lists: [
        {id:1, name:"山田"},
        {id:2, name:"田中"},
        {id:3, name:"木村"},
        {id:4, name:"加藤"},
        {id:5, name:"山下"},
      ],
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
a {
  color: #42b983;
}
</style>
