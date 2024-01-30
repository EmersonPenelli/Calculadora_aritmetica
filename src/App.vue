<script>
  import CalculadoraAritmetica from './components/CalculadoraAritmetica.vue';

  export default {
  components: {
    CalculadoraAritmetica
  }
};
</script>

<template>
    <div id="app">
      <CalculadoraAritmetica />
    </div>
  
</template>

<style scoped>

#app {
  font-family: 'Avenir', 'Helvetica', 'Arial', sans-serif;
  text-align: center;
  color: #2c3e50;
  background: linear-gradient(135deg, #64bccf, #d17585); 
}

input, select {
  font-size: 22px; 
  margin: 15px; 
  padding: 15px; 
  border-radius: 8px; 
  border: none; 
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1); 
  background-color: rgba(255, 255, 255, 0.9); 
}

select {
  font-size: 30px; 
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
  cursor: pointer;
}
</style>
