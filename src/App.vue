<template>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lexend:100,200,300,400,500,600,700,800,900">
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sora:100,200,300,400,500,600,700,800,900">
    
  <div id="nav">
    <router-link to="/AboutPage"><SiteHeader/></router-link>
    
  </div>
  <router-view/>

  <div class="container">
    <transition name="fade">
      <div div class="content">  
        <ImageSlider/>
        <HistoryBox/>
        <CollapsibleCard/>
      </div>
    </transition>

    <footer class ="footer">
        <FooterFeet/>
    </footer>
  </div>

</template>

<script>
import SiteHeader from '@/components/SiteHeader.vue'
import ImageSlider from '@/components/ImageSlider.vue'
import CollapsibleCard from '@/components/CollapsibleCard.vue'
import FooterFeet from '@/components/FooterFeet.vue'

export default {
  name: 'App',
  components: {
    SiteHeader,
    ImageSlider,
    CollapsibleCard,
    FooterFeet
  }
}
</script>

<style>
:root{
  --white: #FFFFFF;
  --prime: #2B3B73;
  --light: #9EABD7;
  --black: #1F1D1D;
  --acc: #B99433;
  --dacc: #97762f;
  --header: "Sora", "Verdana", sans-serif;
  --text: "Lexend", "Arial", sans-serif;
}
html, body{
  margin: 0;
  height: 100%;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--black);
  margin: 0px;
  text-align: left;
}
.spacer{
  margin-top: 40px;
}
.container{
  position: relative;
  display: flex;
  min-height: 100vh;
  flex-direction: column;
  justify-content: space-between;
}
.content{
  flex: 1;
}
.footer{
  position: absolute;
  bottom: 0;
  width: 100%;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>