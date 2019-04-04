
<template>

    <div class="radio-btn-group btn-style-radio">
      
      <div class="radio" v-for="content in contents" :key="content.id">
        <input type="radio" name="radio" :value="content.id" :id="content.message" >
        <label :for="content.message">{{ content.message }} : {{ content.value }} </label>
      </div>
        
    </div>


</template>

<script>
export default {
    props: ['contents'], 
    data() {

    }
}
</script>


<style lang="scss" scoped>

.btn-style-radio {
  display: flex;
  
  .radio {
    margin: 0 .25rem;
    
    label {
      background: #fff;
      border: 1px solid #ddd;
      padding: .5rem 1.25rem;
      border-radius: 5px;
      cursor: pointer;
      color: #444;
      transition: box-shadow 400ms ease;
      
      &:hover {
        box-shadow: 0 2px 5px 0 rgba(0,0,0,0.16), 0 2px 10px 0 rgba(0,0,0,0.12);
      }
    }
    
    input[type="radio"] {
      display: none;
    }
    
    input[type="radio"]:checked+label {
      background: #2196F3;
      color: #fff;
      border-color: #2196F3;
    }
  }
}

// other styles
.show {
  font-weight: 400;
  color: #444;
  
  span {
    background: #f5f5f5;
    color: #F44336;
    border-radius: 3px;
    padding: .25rem .5rem;
    font-size: 1.25rem;
    border: 1px solid #f1f1f1;
  }
}
</style>

