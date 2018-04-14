<script>
  import Vuex from 'vuex'
  import Vue from 'vue'
  import isMobile from './isMobile'

  Vue.use(Vuex)
  export default new Vuex.Store({
    modules:{
      isMobile
    }
  })

</script>
