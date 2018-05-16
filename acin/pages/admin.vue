<template>
<div>
  <form onsubmit="return alert" @submit.prevent="submeterFormulario" class="form">
      <h2>Utilizador</h2>
      <div class="input-control" >
          <label for="">Username</label>
          <input type="text" v-model="novoProduto.username">
           <label for="">Password</label>
          <input type="password" v-model="novoProduto.password">
            <label for="">Email</label>
          <input type="email" required v-model="novoProduto.email">
           <label for="">Localidade</label>
          <input type="text" v-model="novoProduto.localidade">
          <label for="">Morada</label>
          <input type="text"  v-model="novoProduto.morada">
          <label for="">Numero Telemovel</label>
          <input type="text" placeholder="123456789" v-model="novoProduto.ntelemovel">
          <label for="">Nome</label>
          <input type="text" v-model="novoProduto.nome">
          <label for="">Nif</label>
          <input type="text" placeholder="123456789" v-model="novoProduto.nif">
          <label for="">Genero</label>
          <div id="genero" >
            <select v-model="novoProduto.genero">
                <option value="1">masculino</option>
                <option value="2">feminino</option>
                <option value="3">other</option>
            </select>
          </div>
    </div>
      <button type="submit" class="button" >Enviar</button>
  </form>
  <form onsubmit="return alert" @submit.prevent="submeterFormulario" class="form">
      <h2>Produto</h2>
      <div class="input-control" >
           <label for="">Nome do Produto</label>
          <input type="text"  placeholder="Ex: Sushi Tipo 1" v-model="novoProduto.nome">
            <label for="">Valor</label>
          <input type="number"  placeholder="Ex: 8€" required v-model="novoProduto.valor">
           <label for="">Unidades</label>
          <input type="number"  placeholder="Ex: 1,2,3,4,5,6,7,8,9" v-model="novoProduto.unidades">
            <label for="">Imagem</label>
          <input type="file" v-="novoProduto.imagem"> -->
          <label for="">Descricao</label>
          <input type="text" placeholder="Ex: Excelente sushi (etc)." v-model="novoProduto.descricao"> -->
         <label for="">Data</label>
          <input type="date" v-model="novoProduto.data">

     </div>
      <button type="submit" class="button" >Enviar</button>
  </form> 
</div>
</template>

<script>
import axios from 'axios';
export default {
    data(){
        return{
            novoProduto:{
                
            }
        }
    },
    methods:{
        submeterFormulario(){
            return axios.post('http://192.168.1.48:3001/addUser', this.novoProduto);//addProduto ou addUser
        }
    }
}
</script>

<style scoped>
select{
    width: 100%;
}
select:hover{
    color: white;
    background-color: black;
}
.form{
    max-width: 550px;
    box-sizing: border-box;
    margin: 30px;
    margin-top: 60px;
    padding: 30px;
    text-align: justify;
    box-shadow: 0 0 24px rgba(0,0,0,0.3);
    width: 100%;
}
.button{
    font: inherit;
    cursor: pointer;
    border-radius: 4px;
    border: 1px solid #06c4d1;
    background-color: white;
    color:#06c4d1;
    text-decoration: none;
    padding: 10px 30px;
}
.button:hover,
.button:active{
    color:#fff;
    background-color:#06c4d1;
}
.input-control{
    margin:10px 0;
}
.input-control label{
    display: block;
    font-weight: bold;
    color:#06c4d1;
}
.input-control input{
    display: block;
    width: 100%;
    box-sizing: border-box;
    font: inherit;
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 5px;
}
.input-control input:focus{
    background-color: #eee;
    outline: none;
}
</style>
