<template>
  <div class="uk-padding-small">
    <div class="bg-head"><h3>#แจ้งเตือน</h3></div>
    <div class="bg-content">
      <div class="uk-padding-small uk-text-center">
        <h1 class="p-5" v-if="error.statusCode === 404">
          404-ไม่พบหน้า!
        </h1>
        <h1 class="p-5" style="color:red" v-else>
          เกิดข้อผิดพลาด!
        </h1>
        <nuxt-link class="wlink" to="/"><h3>กลับหน้าแรก</h3></nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  head: {
    title: "แจ้งเตือน พบข้อผิดพลาด"
  }
}
</script>
<style scoped>
.wlink h3 {
  text-decoration: none;
  color: #eb622c;
  display: inline;
}
.wlink:hover {
  text-decoration: none;
  color: #222;
}
</style>
