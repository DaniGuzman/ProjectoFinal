<template>
  <section class="container">
    <div class="navbar" ></div>
    <!-- <div>
      <logo/>
    </div> -->
    <br>
    <br>
    <br> 
    <div class="conteudos">    

       <div class="column left" style="background-color:rgb(255, 255, 255); display: flex;justify-content: center;margin: 80px;align-content: center;">
          <h2>Sushi tipo 1 Breve descricao</h2>
       </div>
    <div class="linha">
        <div class="column left" style="background-color:rgb(102, 204, 255);height:300px;width:250px;text-align:center;">
          <h2>Sushi tipo 1</h2>
          <p>Breve descricao</p>
        </div>
        <div class="column middle" style="background-color:rgb(102, 204, 255);height:300px;width:250px;text-align:center;">
          <h2>Sushi tipo 2</h2>
          <p>Breve descricao</p>
        </div>
        <div class="column right" style="background-color:rgb(102, 204, 255);height:300px;width:250px;text-align:center;">
          <h2>Sushi tipo 3</h2>
          <p>Breve descricao</p>
        </div>
        <div class="column right" style="background-color:rgb(102, 204, 255);height:300px;width:250px;text-align:center;">
          <h2>Sushi tipo 3</h2>
          <p>Breve descricao</p>
        </div>
    </div>
    <!-- <div class="conteudos"> 
      <div class="linha" >
        <img src="acinimg.png" alt="">
        </div> 
      </div>   -->
    </div>
  </section>
</template>

<script>
import appQuote from "@/components/app-quote.vue";
import Logo from "~/components/Logo.vue";
export default {
  components: {
    Logo,
    appQuote
  },
  data() {
    return {
      userId: " "
    };
  },
  methods: {
    onLoadUser() {
      this.$router.push("/users/" + this.userId);
    }
  }
};
</script>


<style scoped>
.conteudos{
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 100%;
}
.linha{
  display: flex;
  justify-content: space-around;
  margin: 80px;
  align-content: center;
}
.container {
  min-height: 100vh;
  display: flex;
  width: 100%;
}
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links {
  padding-top: 15px;
}
.userCafe {
  padding: 20px;
}

</style>

