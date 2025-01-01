<script>
import ContainerLayout from '@/components/ContainerLayout.vue';
import CtaSection from './components/CtaSection.vue';
import SectionTitle from '@/components/SectionTitle.vue';

const projects = [
{
        id: 1,
        name: "User Panel Dashboard",
        description: "This project is a web application featuring a robust authentication system to ensure secure user access. After logging in, users can manage five distinct types of ads, adding or editing them as needed. The dashboard provides a comprehensive overview of the ads' performance, showcasing detailed analytics and charts based on the collected data. These visualizations help users gain valuable insights into their ads' effectiveness, enabling informed decision-making to optimize their campaigns. The project emphasizes user-friendly interaction, efficient data management, and actionable analytics.",
        link: "https://www.github.com",
        picture: require('@/assets/images/businessshareslate.png'),
        deployedLink: "https://business.shareslate.com/",
        stack: ["MERN", "React.js", "AntD", "Css","Axios for Integration", "Node.js", "Express.js", "MongoDb", "AWS for Deployment"]
    },
    {
        id: 2,
        name: "Static Website",
        description: "The UI/UX Designer Landing Page is a visually captivating platform for creative professionals to showcase their talents and portfolio. Crafted with Vue.js, it provides a seamless and interactive user experience. The landing page is a canvas for designers to display their finest work, tell their design journey, and connect with potential clients. It's a portfolio that stands out, with beautiful animations and a minimalist design that emphasizes the beauty of UI and UX.",
        link: "https://www.github.com",
        picture: require('@/assets/images/nibnab.png'),
        deployedLink: "https://nibnab.vercel.app/",
        stack: ["Next.js", "Typescript", "TailwindCss",]
    },
    {
        id: 3,
        name: "Restaurant Landing Page",
        description: "The Restaurant Landing Page is a responsive and feature-rich web presence solution for eateries. It's built using React.js and stylized with Bootstrap to deliver an attractive online front for restaurants of all sizes. This landing page offers not just a glimpse of the restaurant's delicious offerings but also facilitates online reservations and takeout orders. With dynamic menus, eye-catching food photography, and a user-friendly interface, it's a gateway to the world of culinary delights.",
        link: "https://www.github.com",
        picture: require('@/assets/images/UiLanding.png'),
        stack: ["React.js", "Bootstrap"]
    }
];

export default {
    components: { ContainerLayout, CtaSection, SectionTitle },
    data() {
      return { projects }
    }
}
</script>

<template>
  <ContainerLayout>
    <section class="mainContainer">
      <SectionTitle>Here is what I've been working on</SectionTitle>
      <div class="projectsGrid">
        <div v-for="project in projects" :key="project.id" class="project">
          <div class="projectImage">
            <img :src="project.picture" alt="Project" loading="lazy" />
          </div>
          <div class="projectDetails">
            <div class="projectHeader">
              <h3 class="projectTitle">
                {{ project.name }}
              </h3>
              <a :href="project.link" target="_blank" class="projectLink">
                <img src="@/assets/icons/githubIcon.svg" alt="github" />
              </a>
              <a :href="project.deployedLink" target="_blank"  >View Live</a>
            </div>
            <p class="projectDesc">{{ project.description }}</p>
            <!-- <p><a :href="project.deployedLink" target="_blank" >{{ project.deployedLink }}</a></p> -->
            <p class="projectStack">
              <strong>Made with: </strong>
              {{ project.stack.join(', ') }}
            </p>
          </div>
        </div>
      </div>
    </section>
  </ContainerLayout>
  <CtaSection />
</template>

<style scoped src="./styles.css"></style>
