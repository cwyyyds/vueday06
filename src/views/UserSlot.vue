<template>
  <div>
    <pannelA>
      <template v-slot:name="scope">
        <input type="text" v-model="scope.row.name" />
      </template>
      <template v-slot:age="scope">
        <input type="text" v-model="scope.row.age" />
      </template>
      <template v-slot:headImgUrl="scope">
        <a :href="scope.row.headImgUrl" v-if="scope.row.type == 0">{{
          scope.row.headImgUrl
        }}</a>
        <img
          :src="scope.row.headImgUrl"
          alt=""
          v-else-if="scope.row.type == 1"
        />
        <p v-else>{{ scope.row.headImgUrl }}</p>
      </template>
    </pannelA>
    <pannelA></pannelA>
  </div>
</template>

<script>
import pannelA from '../components/pannel/pannelA.vue'
export default {
  components: {
    pannelA,
  },
}
</script>

<style></style>
