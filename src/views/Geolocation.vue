<template>
  <div>
    ole
    {{ loc }}
    <butto @click="getLocation"> get geolocation</butto>
  </div>
</template>

<script>
import { Plugins } from '@capacitor/core';
const { Geolocation: geo } = Plugins;

export default {
  name: "Geolocation",
  data () {
    return {
      loc: null
    }
  },
  methods: {
    async getLocation() {
      this.loc = await geo.getLocation()
      console.log(this.loc)
    }
  },

}
</script>

<style scoped>

</style>