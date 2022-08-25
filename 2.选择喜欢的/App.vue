<template>
  <div>
<div v-for="(item,index) in arr" :key="index">
<input type="checkbox"  v-model="newArr" :value="item" >
{{item}}
</div>

<ul>
  <li v-for="(item,index) in newArr" :key="index">
  {{item}}
  </li>
</ul>
  </div>
</template>

<script>
export default {
data () {
  return {
    arr:["科幻", "喜剧", "动漫", "冒险", "科技", "军事", "娱乐", "奇闻"],
    newArr:[]
  }
}
}
</script>

<style>

</style>