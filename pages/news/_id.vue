<template>
  <div>
    <h1>new-content: {{$route.params.id}}</h1>
    <li>
      <nuxt-link :to="{name: 'index'}">HOME</nuxt-link>
    </li>
  </div>
</template>

<script>
  export default {
    // 校验动态路由参数
    validate ({ params }) {
      return /\d+/.test(params.id)
    },
    data () {
      return {
        title: this.$route.params.title
      }
    },
    // 独立设置head信息
    head () {
      return {
        title: this.title,
        meta: [
          { hid: 'description', name: 'news', content: 'This is news page' }
        ]
      }
    }
  }
</script>