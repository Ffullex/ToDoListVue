<template>
  <div class="heart">
    <button class="buttheart" v-on:dblclick="prepare">
      {{blackHeart}}
    </button>
  </div>
</template>

<script>
export default {
  name: "Like",
  data: () => ({
    blackHeart: '🖤',
  }),
  methods: {
    prepare: function () {
        this.blackHeart = '❤️';
    },
  }
}
</script>

<style scoped>
.buttheart {
  border: none;
  background-color: aliceblue;
  margin-left: 10px;
}
</style>