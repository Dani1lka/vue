<template>
 <div class="container pt-1">
  <div class="card">
    <h1>Динамический компанент</h1>
    <appButton :color="active === 'one'?'primary':''" @action="active='one'">One</appButton>
    <appButton :color="active === 'two'?'primary':''" @action="active='two'">Two</appButton>
  </div>
  <div class="card"> 
    <appTextOne v-if="active === 'one'"></appTextOne>
    <appTextTwo v-else-if="active==='two'"></appTextTwo>
  </div>
 
  <!-- <div>
    <app-list>
      <template #default="{idx,iter}">
        <span style="color:red" >
          <strong>{{idx+1}}</strong>
          Item: {{ iter }}
        </span>
      </template>
    </app-list>
  </div> -->


  <!-- <appBlock>
    <template v-slot:header>
      <h3>Это заголовок карточки</h3>
    </template>
    
    <template v-slot:default>
      <hr>
      <h1>Default text</h1>
      <hr>
    </template>
  
  <template v-slot:footer>
    <h2>Это footer</h2>
  </template>
  </appBlock> -->


 </div>
</template>

<script>
// import appBlock from './appBlock.vue';
// import AppList from './appList.vue';

import appTextOne from './appTextOne.vue'
import appTextTwo from './appTextTwo.vue'
import appButton from './appButton.vue'
export default {
  name: 'App',
  components:{appTextOne,appTextTwo,appButton},
  data(){
    return{
      active:'one',
    }
  },

}
</script>

