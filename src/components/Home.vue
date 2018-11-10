<template>
  <div>
    <nav-bar></nav-bar>
    <div class="welcome--popup slide-up" v-if="hideMsg">
      <h2 class="fade-in">{{ title }}</h2>
      <span class="fade-in--slow">{{ caption }}</span>
    </div>
  </div>
</template>

<script>

import NavBar from './NavBar';

export default {
  name: 'Home',
  components: { NavBar },
  data() {
    return {
      hideMsg: true,
      title: 'Welcome',
      caption: 'Find the best place to be.',
    };
  },
  mounted() {
    setInterval(() => {
      // this.hideMsg = !this.hideMsg;
    }, 2000);
  },
}
</script>

<style scoped>

  /* The animation code */
  @keyframes slide-up {
      from { top: 100%; }
      to { top: 30% }
  }
  @keyframes fade-in {
      from { opacity: 0; }
      to { opacity: 100 }
  }
  .welcome--popup {
    width: 100%;
    position: absolute;
    top: 30%;
    left: 50%;
  }
  .slide-up {
    transform: translate(-50%);
    animation-name: slide-up;
    animation-duration: 1s;
    
  }
  .fade-in {
    animation-name: fade-in;
    animation-duration: 1s;
    animation-delay: 0.5s;
    animation-fill-mode: both;
  }
  .fade-in--slow {
    animation-name: fade-in;
    animation-duration: 1s;
    animation-delay: 1s;
    animation-fill-mode: both;
  }
  h2 {
    text-align: center;
  }
  span {
    display: block;
    text-align: center;
    margin-top: 8px;
  }
</style>
