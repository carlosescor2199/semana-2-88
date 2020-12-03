<template>
  <div id="app">
    <NavBar />
    <TeamCard />
  </div>
</template>

<script>
import NavBar from './components/NavBar';
import TeamCard from './components/TeamCard'
export default {
  name: 'App',
  components: {
    TeamCard,
    NavBar
  }
}
</script>

