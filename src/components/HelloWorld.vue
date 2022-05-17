<template>
  <div class="hello">

    <div class="container">
      <div class="message">
        <input type="text" placeholder="Message" v-model="message_value">
        <button @click="message_send">Send</button>
      </div>

    </div>
    <div class="container">
      <input type="text" placeholder="Message">
      <button>Send</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  data() {
      return {
        message_value: "",
         
      }
  },
     methods: {
         message_send() {
           let message_array = [];
           message_array.push(this.message_value);
           console.log(message_array);
        }
     }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.hello
{
  max-width: 1200px;
  margin: 0 auto;
  display:flex;
  justify-content: space-between;
}
.container
{
  min-width: 500px;
  min-height: 600px;
  border-radius: 5px;
  border: 1px solid rgb(119, 118, 118);
  padding: 25px;

  position:relative;
}
.message
{
  width: 90%;
  position:absolute;
  bottom:25px;
  display: flex;
}
input, button{
  padding: 8px 20px;
  border:none;
  outline:none;
  border-radius: 5px;
 
}
input{
  flex-grow: 1;
}
button {
  background-color: #42b983;
  color:white;
  font-weight: bold;
  cursor: pointer;
  margin-left:5px;
  
  
}
</style>
