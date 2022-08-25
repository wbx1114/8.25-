<template>
  <div>
    <div v-for="(item, index) in arr" :key="index">
      <input type="checkbox" v-model="checkNum" :value="item" />
      <span>{{ item }}</span>
    </div>
 <p>选中的数的累计和是：{{getSum}}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [9, 15, 19, 25, 29, 31, 48, 57, 62, 79, 87],
      checkNum: [],
    };
  },
  computed: {
    getSum() {
     return this.checkNum.reduce((sum, acc) => {
        return (sum += acc);
      }, 0);
    },
  },
};
</script>

<style>
</style>