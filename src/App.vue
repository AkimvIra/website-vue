<template>
  <div id="app">
    <div class  = "global">
      <section id = "home-page"  class = "full-heigh">
        <PageHeader />
      </section>

      <section id = "text" class = "bg">
        <PageText />
      </section>

      <section id = "image-block" class = "bg">
        <PageImageLine />
      </section>

      <section id = "news" class = "bg">
        <PageNews />
      </section>

      <section id = "contact" class = "bg">
        <PageAcordion /> 
      </section>
      
      <section id = "footer" class = "bg">
        <PageFooter />  
      </section>

    </div>
  </div>
</template>
  
<script>
import PageHeader from './components/PageHeader.vue';
import PageText from './components/PageText.vue';
import PageImageLine from './components/PageImageLine.vue';
import PageAcordion from './components/PageAcordion.vue';
import PageNews from './components/PageNews.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  name: 'App',
  components: {
    PageHeader,
    PageText,
    PageImageLine,
    PageAcordion,
    PageNews,
    PageFooter

  },
  data(){
    return{
    }
  }
}
</script>
  
<style>
  #app {
    font-family: Arial, Helvetica, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-color: rgb(241, 241, 241);
  }

  body{
    margin: 0;
  }

  #home-page{
    min-height: 90vh;
  }
  
  p{
    font-size: 18px;
    line-height: 27px;
    margin: 0 0 30px;
  }

</style>