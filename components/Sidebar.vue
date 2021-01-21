<template>
  <div class="sidebar" data-color="green" data-background-color="white">
    <div class="logo">
      <a href="http://www.sakura-tech.co.jp/" class="simple-text logo-mini">
        <img src="~/assets/img/logo.gif" alt="ロゴ" width="200">
      </a>
    </div>
    <div class="sidebar-wrapper">
      <ul class="nav">
        <li v-for="(link, i) in links" :key="`bad-sample_${i}`" class="nav-item">
          <a class="nav-link" href="javascript:void(0)" @click.prevent="onClick(link.path)">
            <i class="material-icons">{{ link.icon }}</i>
            <p>{{ link.label }}</p>
          </a>
        </li>
      </ul> 
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      links: [
        { label: '公共工事一覧', icon:'dashboard', path: '/' },
        { label: '地図で表示', icon:'location_ons', path: '/map' }
      ]
    }
  },
  methods: {
    isInternalLink (path) {
      return !/^https?:\/\//.test(path)
    },
    onClick (path) {
      if (this.isInternalLink(path)) {
        this.$router.push(path)
      } else {
        location.href = path
      }
    }
  }
}
</script>