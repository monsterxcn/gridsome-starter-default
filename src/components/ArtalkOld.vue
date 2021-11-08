<template>
  <div id="Comments"></div>
</template>

<script>
import "artalk-v1/dist/Artalk.css"

export default {
  async mounted() {
    const Artalk = require('artalk-v1')
    var artalk = new Artalk({
      el:           '#Comments',
      pageKey:      'https://artalk-in-gridsome.vercel.app/about/',
      // pageTitle: 'gridsome-about',
      serverUrl:    'https://lab.monsterx.cn/ArtalkServer',
      // site:      'artalk-in-gridsome',
    })
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
