<template>
  <div class="hello">
    <h1 style="text-align:center">isMobile? {{isMobile}}</h1><br><br>
    <div :class="{containerphone:isMobile,containerpc:!isMobile}">

      <p>告别传统纸质合同异地快递的方式，签订一份合同几分钟就可以完成。随时签，随地签。支持手机、平板等各种移动设备。</p>
      <p>国家出台法律支持《中华人民共和国合同法》《中华人民共和国电子商务法》《中华人民共和国电子签名法》规范。</p>
      <p>避免纸质合同快递中的丢失；金融级别的存储，保存永久，防遗失；传输采用https和SSL证书加密方式，更安全；符合ISO27。</p>
      <p>随时快精准找到目标合同；保密性强，防篡改，求证更可靠。</p>
    </div>
  </div>
  </div>
</template>

<script>
import {mapState,mapActions} from 'vuex'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
    }
  },
  computed:{
    isMobile(){
      return this.$store.state.isMobile.isMobile
    }
  },
  created(){
    this.setmobileLayout()
  },
  methods: {
    ...mapActions([
      'setmobileLayout'
    ])
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" type="text/stylus" scoped>
  .containerpc{
    width:1200px;
    margin:0 auto;
    display flex;
    justify-content:space-between
    p{
      float:left;
      width:200px;
    }
  }

  .containerphone{
    width:400px;
    margin:0 auto;
    p{
      float:left;
      width:380px;
      margin:10px;
    }
  }

</style>
