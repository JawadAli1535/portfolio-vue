<script>
import ButtonLayout from '@/components/ButtonLayout.vue';

export default {
  components: { ButtonLayout },
};
</script>

<template>
  <section class="heroContainer">
    <div class="leftColumnContent">
      <h1 class="personName">Hey there, I'm Jawad<br />Frontend Developer</h1>
      <p class="personDescription">
        I have extensive expertise in building modern web applications using
        modern stacks. Additionally, I have a keen eye for designing and
        implementing smooth, intuitive user interfaces and I am a quick learner,
        continuously eager to adapt to new technologies and industry best
        practices.
      </p>
      <router-link to="/contact">
        <ButtonLayout :class="'letsTalkButton'">
          <div class="letsTalkContent">
            <p class="letsTalkText">Let's Talk</p>
            <img
              svg-inline
              src="../../../../assets/icons/rightArrowFilled.svg"
              alt="Right Arrow"
            />
          </div>
        </ButtonLayout>
      </router-link>
    </div>
    <div class="rightColumnContent">
      <img
        class="personImage"
        src="../../../../assets/images/jawadprofile.jpeg"
        alt="Person Pic"
      />
    </div>
  </section>
</template>
<style scoped src="./styles.css"></style>
