<template>
  <div>
    <ul>
      <li v-for="list in lists" v-bind:key="list.id">
        <span v-bind:class="list.style">{{list.name}}</span>
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
