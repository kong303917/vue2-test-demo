<template>
  <div id="app" v-loading.fullscreen.lock="fullscreenLoading">
    <NavMenu></NavMenu>
    <Container></Container>
  </div>
</template>

<script>
import './components/common/style.scss';
import NavMenu from './components/common/NavMenu.vue';
import Container from './components/common/Container.vue';

export default {
  components: {
    NavMenu, Container,
  },
  data() {
    return {
      fullscreenLoading: true,
    };
  },
  created() {
    debugger;
  },
  mounted() {
    debugger;
    const vm = this;
    vm.$nextTick(() => {
      vm.fullscreenLoading = false;
    });
  },
};
</script>
