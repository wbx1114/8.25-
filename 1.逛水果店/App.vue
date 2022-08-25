<template>
  <div>
    <table border="1">
      <tr>
        <th>欢迎光临水果店~~</th>
      </tr>
      <tr>
        <th>苹果10￥/斤,折扣 8折</th>
      </tr>
      <tr>
        <td>
          请输入你要买的斤数：
          <input type="text" v-model="num" />
        </td>
      </tr>
      <tr>
        <th>
          <button @click="btn">结账买单~</button>
        </th>
      </tr>
      <tr>
        <td>
          结账单:总价:{{ totle }}元 折后价:{{ disCount }}元 省了:{{ save }}元
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: '',
      totle: '',
      disCount: '',
      save: '',
    };
  },
  methods: {
    btn() {
      this.totle = this.num * 10;
      this.disCount = this.totle* 0.8,
      this.save = this.totle - this.disCount;
    },
  },
};
</script>

<style>
</style>