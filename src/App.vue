<template>
  <div id="app">
    <NavBar />
    <TeamCard />
    <FooterPag/>
  </div>
</template>

<script>
import NavBar from './components/NavBar';
import TeamCard from './components/TeamCard';
import FooterPag from './components/FooterPag';
export default {
  name: 'App',
  components: {
    TeamCard,
    NavBar,
    FooterPag,
  }
}
</script>

