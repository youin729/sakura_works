<template>

<body>
  <div class="wrapper ">
    <Sidebar />
    <div class="main-panel">
      <nav class="navbar navbar-expand-lg navbar-transparent navbar-absolute fixed-top ">
        <div class="container-fluid">
          <div class="navbar-wrapper">
            <a class="navbar-brand" href="javascript:;">地図で表示
            </a>
          </div>
        </div>
      </nav>
      <Map />
    </div>
    <Footer />
  </div>
</body>
</template>

<script>
import Sidebar from '@/components/Sidebar'
import Footer from '@/components/Footer'
import Map from '@/components/Map'

export default {
  components: {
    Sidebar,
    Footer,
    Map
  }
}
</script>