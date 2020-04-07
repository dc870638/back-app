<template>
  <div class="home">
    <span ref='mg'>{{ msg }}</span>
    <button @click='changeCon'>
      点击改变文本
    </button>
  </div>
  
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    // HelloWorld
  },
  data(){
    return {
      msg:'将要改变的信息'
    }
  },
  methods:{
    changeCon(){
      // let that = this
      this.$nextTick(() => {
        
        this.msg = '改变后的信息'
      console.log(this.$refs.mg.innerText)
      })
    }
  }
}
</script>
