<template>
  <section>
    <b-field grouped>
      <b-field label="พิมพ์ดีดไทย" expanded>
        <b-input v-model="SkillWorkInfo.thai_typewriter" placeholder="คำ/นาที"></b-input>
      </b-field>

      <b-field label="พิมพ์ดีดอังกฤษ" expanded>
        <b-input v-model="SkillWorkInfo.english_typewriter" placeholder="คำ/นาที"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ภาษาอังกฤษ" expanded>
        <b-select v-model="SkillWorkInfo.englishskill">
          <option>พื้นฐาน</option>
          <option>พอใช้</option>
          <option>ดี</option>
          <option>ดีมาก</option>
          
        </b-select>
      </b-field>

      <b-field label="ภาษาอื่นๆ" expanded>
        <b-select v-model="SkillWorkInfo.otherlanguageskill">
          <option>พื้นฐาน</option>
          <option>พอใช้</option>
          <option>ดี</option>
          <option>ดีมาก</option>
          
        </b-select>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="โปรแกรมคอมพิวเตอร์" expanded>
        <b-input v-model="SkillWorkInfo.computerprogram"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ออกต่างจังหวัด" expanded>
        <b-radio v-model="SkillWorkInfo.countryside" native-value="ได้">ได้</b-radio>
        <b-radio v-model="SkillWorkInfo.countryside" native-value="ไม่ได้">ไม่ได้</b-radio>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ฉุกเฉินเร่งด่วนสามารถติดต่อ" expanded>
        <b-input v-model="SkillWorkInfo.emergencyContact"></b-input>
      </b-field>

      <b-field label="โทรศัพท์" expanded>
        <b-input v-model="SkillWorkInfo.emergencyPhone"></b-input>
      </b-field>

      <b-field label="ความสัมพันธ์" expanded>
        <b-input v-model="SkillWorkInfo.emergencyRelation"></b-input>
      </b-field>

    </b-field>


    <p>{{SkillWorkInfo}}</p>
  </section>
</template>


<script>
export default {
  data() {
    return {
      SkillWorkInfo: {
        thai_typewriter: "",
        english_typewriter: "",
        englishskill:"",
        otherlanguageskill: "",
        computerprogram: "",
        countryside: "",
        emergencyContact:"",
        emergencyPhone: "",
        emergencyRelation: ""
      }
    };
  }
};
</script>