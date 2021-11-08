<template>
  <div id="Comments"></div>
</template>

<script>
import "artalk/dist/Artalk.css"

export default {
  async mounted() {
    const script = document.createElement('script')
    script.onload = function () {
      // initArtalk()
      var artalk = new Artalk({
        el:        '#Comments',
        pageKey:   'https://artalk-in-gridsome.vercel.app/',
        pageTitle: 'gridsome-index',
        server:    'https://artalk.monsterx.cn/',
        site:      'artalk-in-gridsome',
      })
    }
    script.async = true
    script.defer = true
    script.src = "https://cdn.jsdelivr.net/npm/artalk@2.0.6/dist/Artalk.js"
    document.getElementsByTagName("head")[0].appendChild(script)
  }
}
</script>

<style scoped>
#Comments {
  display: block;
  padding: 20px;
  border-radius: 5px;
  background-color: #F6F7F8;
  box-shadow: 0 10px 20px rgba(0,0,0,.2);
}
</style>
