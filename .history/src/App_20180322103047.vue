<template>
  <div id="app">
    <ice-header></ice-header>
    <ice-team></ice-team>
    <ice-ach></ice-ach>
  </div>
</template>

<script>
import IceHeader from 'components/ice-header/ice-header'
import IceTeam from 'components/ice-team/ice-team'
import IceAch from 'components/ice-achievements/ice-ach'
export default {
  name: 'App',
  components: {
    IceHeader,
    IceTeam,
    IceAch
  }
}
</script>

<style>
@import 'assets/reset.css';

html,
body,
div {
  height: 100%;
}
</style>
