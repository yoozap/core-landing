<template>
  <div id="app">
    <EmailPopup/>
    <Header/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/modules/Header'
import Footer from './components/modules/Footer'
import EmailPopup from './components/EmailPopup'

export default {
  components: {
    EmailPopup,
    Header,
    Footer
  }
}
</script>
<style>

</style>
