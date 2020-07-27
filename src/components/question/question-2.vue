<template>
  <!-- 問題 先ほどのオブジェクトにstyleという項目を追加しました。
            この項目を使ってisBoldの場合はフォントを太字にしてください。
            isBold の場合は、フォントを太字にisNormalの場合は、フォントは通常通り(CSSは登録してあります。) -->
  <!-- 使うもの v-bind -->
  <div>
    <ul>
      <li v-for="list in lists" v-bind:key="list.id">
        <span>{{list.name}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data:function() {
    return {
      lists: [
        {id:1, name:"山田", style:"isBold"},
        {id:2, name:"田中", style:"isNormal"},
        {id:3, name:"木村", style:"isNormal"},
        {id:4, name:"加藤", style:"isNormal"},
        {id:5, name:"山下", style:"isNormal"},
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
span.isNormal {
  font-weight: normal;
}
span.isBold {
  font-weight: bold;
}
a {
  color: #42b983;
}
</style>
