# vue-mobile-adapater

> vue项目手机移动适配

## 运行

``` bash

npm install

npm run dev

```

## 使用

*由屏幕大小判断手机，平板，电脑，把判断值isMobile放在Vuex中；
>

``` bash
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
```
*首页改变

``` bash
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
```

然后，然后就可以用啦～～～～～
Happy ending!
