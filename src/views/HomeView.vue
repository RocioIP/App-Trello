<template>
  <div class="home">
    <app-header :user="user"></app-header>
    <Home />
    <app-footer></app-footer>
  </div>
</template>

<script>
// @ is an alias to /src
import AppHeader from '@/components/AppHeader.vue';
import Home from '@/components/Home.vue';
import AppFooter from '@/components/AppFooter.vue';
export default {
  name: 'HomeView',
  components: {
    AppHeader,
    Home,
    AppFooter,
  },
};
</script>
