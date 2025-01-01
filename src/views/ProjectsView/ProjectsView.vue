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
        description: "The Nibnab Static Website  is a visually captivating platform for creative professionals to showcase their talents and portfolio. Crafted with Next.js and Tailwindcss, it provides a seamless and interactive user experience. It's a portfolio that stands out, with beautiful animations and a minimalist design that emphasizes the beauty of UI and UX.",
        link: "https://www.github.com",
        picture: require('@/assets/images/nibnab.png'),
        deployedLink: "https://nibnab.vercel.app/",
        stack: ["Next.js", "Typescript", "TailwindCss",]
    },
    {
        id: 3,
        name: "Portfolio Website/Viking IT Solution",
        description: "This portfolio is a sleek and professional platform designed to showcase a company's expertise, projects, and achievements. Built with React.js and styled using Tailwind CSS, it offers a seamless and interactive user experience. The portfolio highlights the company’s services, innovative solutions, and success stories while fostering connections with potential clients and partners. Featuring a clean, minimalist design and engaging animations, it reflects the company’s commitment to excellence and modern web development practices. Additionally, internationalization has been seamlessly integrated into the portfolio, ensuring accessibility and relevance for a global audience.",
        link: "https://www.github.com",
        picture: require('@/assets/images/vikingit.png'),
        deployedLink: "https://dazzle-portfolio.vercel.app/en",
        stack: ["React.js", "Bootstrap"]
    },

    {
        id: 4,
        name: "Portfolio Website",
        description: "This portfolio is a sleek and professional platform designed to showcase a company's expertise, projects, and achievements. Built with React.js and styled using Tailwind CSS, it offers a seamless and interactive user experience. The portfolio highlights the company’s services, innovative solutions, and success stories while fostering connections with potential clients and partners. Featuring a clean, minimalist design and engaging animations, it reflects the company’s commitment to excellence and modern web development practices.",
        link: "https://www.github.com",
        picture: require('@/assets/images/rcweb.png'),
        deployedLink: "https://www.roughcopies.com/",
        stack: ["Next.js", "Tailwindcss"]
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
      <SectionTitle>Here is what I've been worked and working on </SectionTitle>
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
      <p style="margin-top:3rem; text-align: center;">Here are a few examples of my previous work. While I've accomplished much more, showcasing everything here isn't feasible.</p>
    </section>
  </ContainerLayout>
  <CtaSection />
</template>

<style scoped src="./styles.css"></style>
