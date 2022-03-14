<template>
  <div class="e-nuxt-container">
    <div class="e-nuxt-content">
      <h1>mKiosk</h1>
      <p>version: {{ version }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      version: null,
    }
  },
  mounted(){
    this.getVersion()
  },
  methods: {
    getVersion(){
      this.version = process.env.npm_package_version;
    }
  }
}
</script>

<style>
.e-nuxt-container {
  display: -webkit-flex;
  display: flex;
  width: 100%;
  min-height: 100vh;
  font-family: Helvetica, sans-serif;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
}

.e-nuxt-content {
  padding: 50px;
  text-align: center;
}


</style>
