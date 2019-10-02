<template>
  <div class="container">
    <div class="card">
      <div class="card-body jumbotron">
        <IdSection class="card-body"></IdSection>
      </div>

      <div class="card">
          <h1 class="display-4">ข้อมูลส่วนตัว</h1>
        <ProfileSection></ProfileSection>
      </div>

      <div class="card">
        <h1 class="display-4">สถานที่ที่ติดต่อได้สะดวก</h1>
        <ContactSection></ContactSection>
      </div>

      <div class="card">
        <h1 class="display-4">ประวัติการศึกษา</h1>
        <EducationAndActivities></EducationAndActivities>
      </div>

      <div class="card">
        <h1 class="display-4">ความสามารถ</h1>
        <SkillWork></SkillWork>
      </div>

      <div class="card">
        <h1 class="display-4">ประวัติการทำงาน</h1>
        <WorkExperience></WorkExperience>
      </div>

      <ConfirmSection></ConfirmSection>
    </div>
  </div>
</template>

<script>
import IdSection from "./IdSection.vue";
import ProfileSection from "./ProfileSection.vue";
import ContactSection from "./ContactSection.vue";
import EducationAndActivities from "./EducationAndActivities.vue";
import SkillWork from "./SkillWork.vue";
import WorkExperience from "./WorkExperience.vue";
import ConfirmSection from "./ConfirmSection.vue";

export default {
  components: {
    IdSection,
    ProfileSection,
    ContactSection,
    EducationAndActivities,
    SkillWork,
    WorkExperience,
    ConfirmSection
  }
};
</script>

<style>
body {
  background-color: lightblue;
}

h1 {
  color: rgb(139, 0, 0);
  font-size: 50px;
}

p {
  color: darkblue;
  font-size: 20px;
}
</style>


