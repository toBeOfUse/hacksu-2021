<template>
  <div class="footer">
    <div class="icon-row">
    <a class="social" href="https://www.facebook.com/groups/hacksu"><img src="../assets/facebook-white.svg"></a>
    <a class="social" href="https://twitter.com/_hacksu"><img src="../assets/twitter-white.svg"></a>
    <a class="social" href="https://www.instagram.com/hacksu/"><img src="../assets/instagram-white.svg"></a>
    <a class="social" href="https://github.com/hacksu"><img src="../assets/github-padded-white.svg"></a>
    <a v-if="discord" class="social" v-bind:href="discord"><img src="../assets/discord-square-white.svg"></a>
    </div>
  </div>
</template>

<script>
import { discord } from '@/details';

export default {
  name: 'SocialMedia',
  data() {
    return {
      discord,
    }
  },
}
</script>

<style lang="scss" scoped>

.footer {
  padding-bottom: 5vh;
  background-color: rgb(20, 32, 39);
  text-align: center;
  .icon-row {
    display: flex;
    width: 450px;
    max-width: 95vw;
    margin: 0 auto;
  }
  .social {
    display: inline-block;
    padding: 5vh 1.25vh;
    width: 100%;
    img {
      width: 100%;
      transition: transform 0.25s, filter 0.25s;
    }
    &:hover {
      img {
        transform: scale(1.1);
        filter: brightness(120%);
      }
    }
  }
}

</style>
