<template>
  <section>
    
    <b-field grouped>
      <b-field label="บ้านเลขที่" expanded> 
        <b-input v-model="contactInfo.housenumber"></b-input>
      </b-field>
      <b-field label="หมู่" expanded>
        <b-input v-model="contactInfo.moo"></b-input>
      </b-field>

      <b-field label="ซอย" expanded>
        <b-input v-model="contactInfo.soi"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
        <b-field label="ถนน" expanded>
        <b-input v-model="contactInfo.tambon"></b-input>
      </b-field>
        
      <b-field label="ตำบล/แขวง" expanded>
        <b-input v-model="contactInfo.tambon"></b-input>
      </b-field>
      <b-field label="อำเภอ/เขต" expanded>
        <b-input v-model="contactInfo.district"></b-input>
      </b-field>
    </b-field >

    <b-field grouped>
      <b-field label="จังหวัด">
        <b-select v-model="contactInfo.city" placeholder="โปรดเลือก">
          <option
            v-for="city in cityList "
            v-bind:key="city.id"
            v-bind:value="city.name"
          >{{ city.name }}</option>
        </b-select>
      </b-field>

        <b-field label="รหัสไปรษณีย์" expanded>
        <b-input v-model="contactInfo.zipcode"></b-input>
      </b-field>

      <b-field label="โทรศัพท์" type="is-danger" message="(ใส่เฉพาะตัวเลข 0-10 เท่านั้น)">
        <b-input v-model="contactInfo.phone"></b-input>
      </b-field>

    </b-field>

    <b-field grouped>
      <b-field label="โทรศัพท์มือถือ" type="is-danger" message="(ใส่เฉพาะตัวเลข 0-10 เท่านั้น)" expanded>
        <b-input v-model="contactInfo.cellphone"></b-input>
      </b-field>
      <b-field label="Email" expanded> 
        <b-input v-model="contactInfo.email"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ชื่อบิดา" expanded>
        <b-input v-model="contactInfo.fatherfirstName"></b-input>
      </b-field>

      <b-field label="อาชีพ" expanded>
        <b-input v-model="contactInfo.fatherJob"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="ชื่อมารดา" expanded>
        <b-input v-model="contactInfo.motherfirstName"></b-input>
      </b-field>

      <b-field label="อาชีพ" expanded>
        <b-input v-model="contactInfo.motherlastJob"></b-input>
      </b-field>
    </b-field>

    <b-field grouped>
      <b-field label="สถานภาพ" expanded>
        <b-radio v-model="contactInfo.status" native-value="โสด">โสด</b-radio>
        <b-radio v-model="contactInfo.status" native-value="แต่งงาน">แต่งงาน</b-radio>
        <b-radio v-model="contactInfo.status" native-value="หย่า">หย่า</b-radio>
        <b-radio v-model="contactInfo.status" native-value="แยกกันอยู่">แยกกันอยู่</b-radio>
        <b-radio v-model="contactInfo.status" native-value="หม้าย">หม้าย</b-radio>
        
      </b-field>
    </b-field>
    

    <p>{{contactInfo}}</p>
  </section>
</template>

<script>
export default {
  data() {
    return {
      contactInfo: {
        housenumber: "",
        moo: "",
        soi:"",
        road:"",
        tambon: "",
        district: "",
        city: "",
        zipcode: "",
        phone: "",
        cellphone: "",
        email: "",
        fatherName: "",
        fatherJob: "",
        motherName: "",
        motherJob: "",
        status: ""

      },

      cityList: [
        { id: 1, name: "กระบี่" },
        { id: 2, name: "กรุงเทพมหานคร" },
        { id: 3, name: "กาญจนบุรี" },
        { id: 4, name: "กาฬสินธุ์" },
        { id: 5, name: "กำแพงเพชร" },
        { id: 6, name: "ขอนแก่น" },
        { id: 7, name: "จันทบุรี" },
        { id: 8, name: "ฉะเชิงเทรา" },
        { id: 9, name: "ชลบุรี" },
        { id: 10, name: "ชัยนาท" },
        { id: 11, name: "ชัยภูมิ" },
        { id: 12, name: "ชุมพร" },
        { id: 13, name: "เชียงราย" },
        { id: 14, name: "เชียงใหม่" },
        { id: 15, name: "ตรัง" },
        { id: 16, name: "ตราด" },
        { id: 17, name: "ตาก" },
        { id: 18, name: "นครนายก" },
        { id: 19, name: "นครปฐม" },
        { id: 20, name: "นครพนม" },
        { id: 21, name: "นครราชสีมา" },
        { id: 22, name: "นครศรีธรรมราช" },
        { id: 23, name: "นครสวรรค์" },
        { id: 24, name: "นนทบุรี" },
        { id: 25, name: "นราธิวาส" },
        { id: 26, name: "น่าน" },
        { id: 27, name: "บึงกาฬ" },
        { id: 28, name: "บุรีรัมย์" },
        { id: 29, name: "ปทุมธานี" },
        { id: 30, name: "ประจวบคีรีขันธ์" },
        { id: 31, name: "ปราจีนบุรี" },
        { id: 32, name: "ปัตตานี" },
        { id: 33, name: "พะเยา" },
        { id: 34, name: "พังงา" },
        { id: 35, name: "พัทลุง" },
        { id: 36, name: "พิจิตร" },
        { id: 37, name: "พิษณุโลก" },
        { id: 38, name: "เพชรบุรี" },
        { id: 39, name: "เพชรบูรณ์" },
        { id: 40, name: "แพร่" },
        { id: 41, name: "ภูเก็ต" },
        { id: 42, name: "มหาสารคาม" },
        { id: 43, name: "มุกดาหาร" },
        { id: 44, name: "แม่ฮ่องสอน" },
        { id: 45, name: "ยโสธร" },
        { id: 46, name: "ยะลา" },
        { id: 47, name: "ร้อยเอ็ด" },
        { id: 48, name: "ระนอง" },
        { id: 49, name: "ระยอง" },
        { id: 50, name: "ราชบุรี" },
        { id: 51, name: "ลพบุรี" },
        { id: 52, name: "ลำปาง" },
        { id: 53, name: "ลำพูน" },
        { id: 54, name: "เลย" },
        { id: 55, name: "ศรีสะเกษ" },
        { id: 56, name: "สกลนคร" },
        { id: 57, name: "สงขลา" },
        { id: 58, name: "สตูล" },
        { id: 59, name: "สมุทรปราการ" },
        { id: 60, name: "สมุทรสงคราม" },
        { id: 61, name: "สมุทรสาคร" },
        { id: 62, name: "สระแก้ว" },
        { id: 63, name: "สระบุรี" },
        { id: 64, name: "สิงห์บุรี" },
        { id: 65, name: "สุโขทัย" },
        { id: 66, name: "สุพรรณบุรี" },
        { id: 67, name: "สุราษฎร์ธานี" },
        { id: 68, name: "สุรินทร์" },
        { id: 69, name: "หนองคาย" },
        { id: 70, name: "หนองบัวลำภู" },
        { id: 71, name: "อยุธยา" },
        { id: 72, name: "อ่างทอง" },
        { id: 73, name: "อำนาจเจริญ" },
        { id: 74, name: "อุดรธานี" },
        { id: 75, name: "อุตรดิตถ์" },
        { id: 76, name: "อุทัยธานี" },
        { id: 77, name: "อุบลราชธานี" }
      ]
    };
  }
};
</script>