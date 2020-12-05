
<template>
  <div id="app">
    <NavBar />
    <TeamCard />
    <Services />
  </div>
</template>

<script>
import NavBar from './components/NavBar';
import TeamCard from './components/TeamCard'
import Services from "./components/Services"
export default {
  name: 'App',
  components: {
    Services,
    TeamCard,
    NavBar
  }
}
</script>

