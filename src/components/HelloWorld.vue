<template>
  <div>
    <h3>process.envs</h3>
    <ul>
      <template v-if="envs">
        <li>{{ `FOO: ${envs.FOO}` }}</li>
        <li>{{ `VUE_APP_FOO: ${envs.VUE_APP_FOO}` }}</li>
        <li>{{ `FOO_VUE_APP: ${envs.FOO_VUE_APP}` }}</li>
      </template>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  computed: {
    envs() {
      return process ? process.env : null
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
</style>
