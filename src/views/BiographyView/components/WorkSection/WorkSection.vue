<script>
import SectionTitle from '@/components/SectionTitle.vue';
import TimelineLayout from '@/components/TimelineLayout.vue';

const career = [
  {
    date: '2022-04-01',
    dateString: 'Oct 2023 - Present',
    work: 'Rough Copies Pvt Ltd',
    text: 'Working as a Frontend developer(Reactjs/Nextjs/ReactNative) at Rough Copies.',
  },
  {
    date: '2020-04-01',
    dateString: 'Oct 2022',
    work: 'Tri Tech Solutions',
    text: 'Worked with different clients on React and Javascript based projects. Really helped me to learn new things, improve my skills and get a better understanding of the programming.',
  },
];

const education = [
  {
    date: '2016-03-02',
    dateString: 'September 2017 - December 2022',
    work: 'University of Engineering and Technology, Pehsawar',
    text: 'Bachelors in Computer Systems Engineering',
  },
  {
    date: '2023-04-01',
    dateString: '2015 - 2017',
    work: 'Islamia College Peshawar',
    text: 'Fsc Pre Engineering',
  },
];

export default {
  components: { SectionTitle, TimelineLayout },
  data() {
    return { career, education };
  },
};
</script>

<template>
  <div class="mainContainer">
    <div class="gridColumnLeft">
      <div class="careerSection">
        <SectionTitle>My Career</SectionTitle>
        <div v-for="(item, index) in career" :key="index">
          <TimelineLayout
            :date="item.date"
            :dateString="item.dateString"
            :work="item.work"
            :workDescription="item.text"
          />
        </div>
      </div>
      <div class="educationSection">
        <SectionTitle>My Education</SectionTitle>
        <div v-for="(item, index) in education" :key="index">
          <TimelineLayout
            :date="item.date"
            :dateString="item.dateString"
            :work="item.work"
            :workDescription="item.text"
          />
        </div>
      </div>
    </div>
    <div class="skillsSection">
      <img src="@/assets/icons/dots.svg" alt="Dots" class="dots" />
      <div class="skillsSectionContent">
        <SectionTitle>Skills</SectionTitle>
        <h3 class="skillTitle">Languages I've worked with:</h3>
        <ul>
          <li>Javascript</li>
          <li>C++</li>
          <!-- <li>Python</li> -->
        </ul>
        <h3 class="skillTitle">Libraries/Frameworks I've worked with:</h3>
        <ul>
          <li>Html5</li>
          <li>Css3 (Bootstrap, TailwindCss, AntD, MUI )</li>
          <li>Javascript</li>
          <li>Responsive Design</li>
          <li>Pixel Perfect UI</li>
          <li>React.js</li>
          <li>Typescript</li>
          <li>Flux,Redux, ReduxToolkit</li>
          <li>React Charts</li>
          <li>Next.js</li>
          <li>Vue.js</li>
          <li>React Native</li>
          <li>Firebase</li>
          <li>SQL</li>
          <li>MongoDb</li>
          <li>MERN</li>
        </ul>
        <!-- <h3 class="skillTitle">Tools I am comfortable with:</h3>
        <ul>
          <li>VsCode</li>
          <li>Sublime Text</li>
          <li>Android Studio</li>
        </ul> -->
      </div>
    </div>
  </div>
</template>

<style scoped src="./styles.css"></style>
