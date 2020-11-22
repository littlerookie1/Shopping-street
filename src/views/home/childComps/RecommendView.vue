<template>
  <div class="recommend">
    <div v-for="item in recommends" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
  export default {
    name: "RecommendView",
    props: {
      recommends: {
        type: Array,
        default() {
          return [];
        }
      }
    }
  }
</script>

<style scoped>
  .recommend{
    display: flex;
    width: 100%;
    font-size: 12px;
    text-align: center;

    padding: 10px 0 20px;
    border-bottom: 8px solid #eeeeee;
  }

  .recommend-item{
    flex: 1;
    margin: 0 5px;
  }

  .recommend-item img{
    width: 100%;
  }
</style>
