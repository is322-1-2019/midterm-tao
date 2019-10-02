<template>
  <section>
    <b-field grouped>
      <b-field label="เลขที่ประกาศตำแหน่ง" expanded>
        <b-input v-model="profileInfo.announcementId" placeholder="4/4562-2 เจ้าหน้าที่บริหารทั่วไปปฎิบัตรการ ศูนย์ให้คำปรึกษา"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ผลประกาศ" expanded>
        <b-radio v-model="profileInfo.passornot" native-value="ผ่าน">ผ่าน</b-radio>
        <b-radio v-model="profileInfo.passornot" native-value="ไม่ผ่าน">ไม่ผ่าน</b-radio>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="คำนำหน้า" expanded>
        <b-radio v-model="profileInfo.prefix" native-value="นาย">นาย</b-radio>
        <b-radio v-model="profileInfo.prefix" native-value="นาง">นาง</b-radio>
        <b-radio v-model="profileInfo.prefix" native-value="นาง">นางสาว</b-radio>
        <b-radio v-model="profileInfo.prefix" native-value="นาง">อื่นๆ</b-radio>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ชื่อ" expanded>
        <b-input v-model="profileInfo.firstName"></b-input>
      </b-field>

      <b-field label="นามสกุล" expanded>
        <b-input v-model="profileInfo.lastName"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
        <b-field label="เชื้อชาติ" expanded>
        <b-input v-model="profileInfo.ethnicity"></b-input>
      </b-field>

        <b-field label="สัญชาติ" expanded>
        <b-input v-model="profileInfo.nationality"></b-input>
      </b-field>

    </b-field>

    <b-field grouped>
        <b-field label="ศาสนา" expanded>
        <b-input v-model="profileInfo.religious" ></b-input>
      </b-field>

        <b-field label="ส่วนสูง" expanded>
        <b-input v-model="profileInfo.height" placeholder="เซนติเมตร"></b-input>
      </b-field>

      <b-field label="น้ำหนัก" expanded>
        <b-input v-model="profileInfo.weight" placeholder="กิโลกรัม" ></b-input>
      </b-field>

    </b-field>


    <b-field grouped>
      <b-field label="วัน/เดือน/ปีเกิด">
        <b-datepicker
          v-model="profileInfo.birthday"
          placeholder="คลิกเลือก"
          icon="calendar-today"
          editable
        ></b-datepicker>
      </b-field>

    </b-field>


    <p>{{profileInfo}}</p>
  </section>
</template>

<script>
export default {
  data() {
    return {
      profileInfo: {
        announcementId: "",
        passornot: "",
        prefix: "",
        firstName: "",
        lastName: "",
        ethnicity: "",
        nationality: "",
        religious: "",
        height:"",
        weight:"",
        birthday: "",
        
        
      },

    };
  }
};
</script>