<template>
  <div >
      <slot></slot>
  </div>
</template>

<script>
import appQuote from '@/components/app-quote.vue';
import Logo from '~/components/Logo.vue'
export default{
    components:{
        Logo,
        appQuote
    }, 
  data(){
    return {
      userId:' '
    }
  },
  methods:{
    onLoadUser(){
      this.$router.push('/users/' + this.userId)
    }
  }
}
</script>
<style scoped>
div{
    background-color: white;
    box-shadow: 0 0 24px rgba(0, 0, 0, 0.3);
    margin: 20px;
    padding: 3rem;
    width: 420px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between; 
}
</style>

