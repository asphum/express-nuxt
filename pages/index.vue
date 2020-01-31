<template>
  <div class="uk-padding-small">
    <div class="bg-content">
      <h1>หน้าแรก ยินดีต้อนรับ</h1>
      <div class="row row-cols-2 row-cols-md-4 no-gutters">
        <NLink
          to="/"
          v-lazy-container="{ selector: 'img' }"
          class="col coveralbum"
        >
          <img
            class="img-fluid"
            data-src="https://img.freepik.com/free-photo/man-through-hole-paper_1368-47349.jpg"
            data-loading="https://img.freepik.com/free-photo/man-through-hole-paper_1368-47349.jpg?size=100&ext=jpg"
          />
          <h6 class="textcoveralbum m-3 text-truncate">
            ดื่มนมกันเถอะ ดื่มนมกันเถอะ ดื่มนมกันเถอะ
          </h6>
        </NLink>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      posts: [],
      links: []
    };
  },
  methods: {
    loadMore(key) {}
  },
  async asyncData({ $axios }) {
    let { data, links } = await $axios.get("/photos");
    console.log(links);
    return {
      posts: data,
      links
    };
  },
  head: {
    title: "หน้าแรก"
  }
};