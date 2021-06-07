<template>
  <div>
    <div class="container ">
      <h4 class="text-center mt-3">Import Your Text For Convert</h4>
      <div class="myTextArea">
        <textarea v-model="text"></textarea>
      </div>
      <div class="row d-flex justify-content-center">
        <div class="col-md-5 converted-box  m-2">
          <div class="title mb-3   d-flex justify-content-between">
            <span class="ml-1">Full UpperCase</span>
            <button class="badge badge-warning text-dark">Copy Text</button>
          </div>
          <div class="text-body ">           
            {{ text | toUppercase }}
          </div>
        </div>
        <div class="col-md-5 converted-box  m-2">
          <div class="title mb-3   d-flex justify-content-between">
            <span class="ml-1">Full LowerCase</span>
            <button class="badge badge-warning text-dark">Copy Text</button>
          </div>
          <div class="text-body ">           
            {{ text | toLowercase}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data(){
    return{
      text: 'This Is Sample Text For Test ! Remove Text And Test Your Text.'
    }
  },
  filters:{
    toUppercase(value){
      return value.toUpperCase();
    },
    toLowercase(value){
      return value.toLowerCase();
    }
  }
}
</script>

<style scoped>
.myTextArea{
  display: flex;
  justify-content: center;
}
.myTextArea textarea{
  padding: 5px;
  width: 90%;
  margin: 5px auto;
  min-height: 130px;
  /* margin: 40px auto; */
  /* margin-left: auto; */

}
.converted-box{
  border: 1px solid rgb(0, 0, 0);
  border-radius: 8px;
  padding: 15px;
}

.title{
  background-color: rgb(61, 77, 88);
  color: #fff;
  border-radius: 4px;
  padding: 2px;
}


/* Small devices (landscape phones, 576px and up) */
@media (min-width: 576px) {  
 
}
 
/* Medium devices (tablets, 768px and up) The navbar toggle appears at this breakpoint */
@media (min-width: 768px) {  
 .myTextArea textarea{
  width: 70%;
 }
}
 
/* Large devices (desktops, 992px and up) */
@media (min-width: 992px) { 
 
}
 
/* Extra large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) {  
    
}
 
</style>
