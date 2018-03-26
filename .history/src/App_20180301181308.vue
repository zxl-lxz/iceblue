<template>
  <div id="app">
    <ice-header></ice-header>
    <ice-team></ice-team>
  </div>
</template>

<script>
import IceHeader from 'components/ice-header/ice-header'
import IceTeam from 'components/ice-team/ice-team'
export default {
  name: 'App',
  components: {
    IceHeader,
    IceTeam
  }
}
</script>

<style>
 @import "assets/reset.css";
</style>
