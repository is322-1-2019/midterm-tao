<template>
  <section>
    <b-field grouped>
      <b-field label="ชื่อสถานที่ทำงาน">
        <b-input v-model="WorkExperienceInfo.officeName"></b-input>
      </b-field>
      <b-field label="ตำแหน่ง">
        <b-input v-model="WorkExperienceInfo.position"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="วันที่เริ่ม">
        <b-datepicker
          v-model="WorkExperienceInfo.startdate"
          placeholder="คลิกเลือก"
          icon="calendar-today"
          editable
        ></b-datepicker>
      </b-field>
      <b-field label="วันที่ออก">
        <b-datepicker
          v-model="WorkExperienceInfo.enddate"
          placeholder="คลิกเลือก"
          icon="calendar-today"
          editable
        ></b-datepicker>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ลักษณะของงาน">
        <b-input v-model="WorkExperienceInfo.workstyle"></b-input>
      </b-field>
      <b-field label="เงินเดือน">
        <b-input v-model="WorkExperienceInfo.salary"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="เหตุที่ออก">
        <b-input v-model="WorkExperienceInfo.reason"></b-input>
      </b-field>
    </b-field>
    <p>{{WorkExperienceInfo}}</p>
  </section>
</template>


<script>
export default {
  data() {
    return {
      WorkExperienceInfo: {
        officeName: "",
        position: "",
        startdate: "",
        enddate: "",
        workstyle: "",
        salary: "",

        reason: ""
      }
    };
  }
};
</script>