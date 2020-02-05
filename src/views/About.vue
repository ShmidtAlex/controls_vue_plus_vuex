<template>
  <div class="about">
    <h1>This is a test page</h1>
    <div class="controls_wrapper_block">
      <h3>Here is the control component</h3>
      <div class="controls_themselvs">
        <div class="control">
          <control-group />
        </div>
      </div>
    </div>
 </div>
</template>

<script>

  import controlGroup from '../components/controlGroup';

  export default {
    components: {
      controlGroup
    },
    data: function() {
      return {
         
      }
    },
    mounted: function(){
      //add all necessary event for input
      var inputsArr = document.querySelectorAll('INPUT');
     
      inputsArr.forEach(function(elem){
        elem.addEventListener("keydown", e => {
          // console.log(e.target.value);
          // elem.target.value = elem.target.value.replace(/[aeiou]/g, '*');
        });
        elem.addEventListener("keyup", e => {
          // elem.target.value = elem.target.value.replace(/[aeiou]/g, '*');
        });
        elem.addEventListener("keypress", e => {
          // elem.target.value = e.target.value.replace(/[aeiou]/g, '*');
        });
        // elem.addEventListener("input", e => {});
      })
    },
    computed: {
      
    },
    methods: {
     
    } 
  }
  
</script>
