<template>
  <v-layout class="bg-img">
    <WorkBtn class="action" />
    <Nav />
    <MobileNav />
  </v-layout>
</template>

<script>
import Nav from '../components/Nav'
import MobileNav from '../components/MobileNav'
import WorkBtn from '../components/WorkBtn'
export default {
  components: {
    Nav,
    WorkBtn,
    MobileNav,
  },
}
</script>
<style lang="scss">
a {
  color: $primary;
  text-decoration: none;
}
.mobile {
  display: none;
}
.bg-img {
  background-image: url('../assets/space.svg');
  background-position: right;
  background-repeat: no-repeat;
  background-size: contain;
  .action {
    margin-right: 15rem;
  }
}
@media only screen and (max-width: 1500px) {
  .bg-img {
    background-position: bottom;
    background-size: cover;
  }
}

@media only screen and (max-width: 900px) {
  .header {
    display: none;
  }
  .bg-img {
    background-image: url('../assets/mobilehome.png');
  }
  .discover {
    top: 25vh;
  }
  .mobile {
    background-color: $primary;
    position: fixed;
    width: 100vw;
    display: flex;
    bottom: 0vh;
    justify-content: space-around;
    color: white;
    font-size: 1.3rem;
  }
}
</style>
