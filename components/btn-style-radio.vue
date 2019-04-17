
<template>

    <div class="radio-btn-group btn-style-radio">
      
      <div class="radio" v-for="(content, i) in contents" :key="content.id">

        <input v-if="groupName" type="radio" :name="groupName" :value="content.value" :id="unique+i" >
        <input v-else           type="radio" :name="unique+i" :value="content.value" :id="unique+i" >
        <label :for="unique+i" v-html="content.message +':'+content.value +':'+ unique+i"></label>
        
      </div>
        
    </div>


</template>

<script>
export default {
    props: { 
      contents : Object, 
      groupName : String
      }, 
    data() {
        return {
            unique : Math.random().toString(36).substr(2,9)
        }
    }
}
</script>


<style lang="scss" scoped>

.btn-style-radio {
  // display: flex;
  
  .radio {
    margin: 0 .25rem;
    width: 100%;
    
    label {
      display: block;
      background: #fff;
      border: 1px solid #ddd;
      padding: 1.35rem 2.25rem;
      border-radius: 5px;
      cursor: pointer;
      color: #444;
      transition: box-shadow 400ms ease;
      margin: 1rem 0;
      
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

