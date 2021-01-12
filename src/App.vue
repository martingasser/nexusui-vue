<template>
  <div id="position" />
  <div>x position: {{x}}</div>
  <div>y position: {{y}}</div>
</template>

<script>
import Nexus from 'nexusui'

export default {
  name: 'App',
  data () {
    return {
      x: 0,
      y: 0
    }
  },
  mounted () {
    this.dial = new Nexus.Position('#position')
    this.dial.on('change', this.positionChange)
  },
  methods: {
    positionChange (p) {
      this.x = p.x
      this.y = p.y
    }
  }
}
</script>