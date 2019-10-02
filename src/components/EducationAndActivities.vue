<template>
  <section>
    <b-field grouped>
      <b-field label="เลขที่บัตรประชาชน" expanded>
        <b-input v-model="EduInfo.IDcard"></b-input>
      </b-field>
    </b-field>

    <b-field grouped expanded>
      <b-field label="ชื่อวุฒิ" expanded>
        <b-select v-model="EduInfo.eduCertificate">
          <option>ม.3</option>
          <option>ม.6/ปวช</option>
          <option>ปริญญาตรี</option>
          <option>ปริญญาโท</option>
          <option>ปริญญาเอก</option>
        </b-select>
      </b-field>

        <b-field label="สาขาวิชาเอก" expanded>
        <b-input v-model="EduInfo.major"></b-input>
      </b-field>

      <b-field label="เกรด" expanded>
        <b-input v-model="EduInfo.gpa"></b-input>
      </b-field>

    </b-field>



    <b-field grouped>
        <b-field label="ชื่อสถานศึกษา" expanded>
        <b-input v-model="EduInfo.school"></b-input>
      </b-field>

      <b-field label="เดือนปีที่จบ" expanded>
        <b-input v-model="EduInfo.graduation" placeholder="เดือน-ปี ที่จบ"></b-input>
      </b-field>

    </b-field>
    
    <b-field grouped>
      <b-field label="สถานภาพทางการทหาร">
        <b-select v-model="EduInfo.armyActivities">
          <option>สำเร็จ ร.ด.</option>
          <option>ผ่านการเกณฑ์ทหารแล้ว</option>
          <option>ยังไม่ผ่านการเกณฑ์ทหาร</option>
        </b-select>
      </b-field>


    </b-field>









    <p>{{EduInfo}}</p>
  </section>
</template>


<script>
export default {
  data() {
    return {
      EduInfo: {
        eduCertificate: "",
        major: "",
        gpa: "",
        school: "",
        graduation: "",
        armyActivities:""
      },

      
    };
  },
  
};
</script>