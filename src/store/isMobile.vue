<script>
  export default{
    state: {
      isMobile: false
    },
    mutations: {
      mobileLayout(state){
        state.isMobile = true
      }
    },
    actions: {
      setmobileLayout: function({commit}){
        let w = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;
        console.log(w)
        if(w<960){
          commit('mobileLayout')
        }
      }
    }
  }

</script>
