<template>
  <div id="map"></div>
</template>

<style>
  #map {
    position: relative;
    overflow: hidden;
    z-index: 2;
    height: calc(100vh - 70px);
    margin-top: 70px;
  }
</style>
<script>
import loadGoogleMapsApi from 'load-google-maps-api'

async (context, inject) => {
  const gmap = await loadGoogleMapsApi({
    key: context.env.apiKey
  })

  inject('gmap', gmap)
}

export default {
  data() {
    return {
      map: null
    }
  },
  mounted() {
    const element = document.getElementById('map')
/*
    const lating = new this.$gmap.LatLng(35.680153982276565, 139.7624033935538)
    const g = new this.google.maps.Marker({
    map: this.$refs.googleMap,
      position: lating
    })
*/
    const map = new this.$gmap.Map(element, {
        center: { lat: 35.680153982276565, lng: 139.7624033935538 },
        zoom: 15
      },
      this.map = map
    )
  }
}
</script>