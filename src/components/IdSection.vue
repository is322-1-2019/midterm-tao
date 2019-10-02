<template>
  <section>
    <b-field grouped>
      <b-field label="เลขที่บัตรประชาชน">
        <b-input v-model="IdInfo.IDcard"></b-input>
      </b-field>
    </b-field>

    

    
       
    
    <b-button type="is-success">ตกลง</b-button>

    <p>{{IdInfo}}</p>
  </section>
</template>


<script>
export default {
  data() {
    return {
      IdInfo: {
        IDcard: ""
      },

      
    };
  },
  
};
</script>