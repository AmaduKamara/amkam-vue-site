<template>
  <div>
    <NavBar />

    <!-- HERO SECTION -->
    <div class="relative heroSection h-screen">
      <div class="image">
        <img class="object-cover w-full pt-5" src="images/Amadu Kamara.png" alt="Amadu Kamara" />
      </div>
      <div class="absolute -mt-12 bg-gray-200 p-8 mx-4 rounded shadow-2xl text-white mb-8">
        <h4 class="text-center text-teal-500 text-xl">Hello!</h4>
        <h3 class="text-center text-teal-500 text-2xl leading-tight">I Am Amadu Kamara, aka Amkam.</h3>
        <p
          class="text-sm mt-2 text-center text-gray-500 leading-normal"
        >I am Web Designer, Developer, UI/UX Designer and A Web Instructor with 4 years experience.</p>
      </div>
    </div>

    <!-- SKILLS LINK SECTION -->
    <div class="my-6">
      <div class="card bg-white shadow-xl mx-4 rounded py-4 px-4 text-teal-500">
        <h4>
          <a href="#">
            <i class="fas fa-desktop"></i> Web Design
          </a>
        </h4>
      </div>
      <div class="card mt-4 bg-white shadow-xl mx-4 rounded py-4 px-4 text-teal-500">
        <a href="#">
          <h4>
            <i class="fas fa-laptop"></i> Frontend Development
          </h4>
        </a>
      </div>
      <div class="card mt-4 bg-white shadow-xl mx-4 rounded py-4 px-4 text-teal-500">
        <a href="#">
          <h4>
            <i class="fas fa-desktop"></i> UI/UX Design
          </h4>
        </a>
      </div>
      <div class="card mt-4 bg-white shadow-xl mx-4 rounded py-4 px-4 text-teal-500">
        <a href="#">
          <h4>
            <i class="fas fa-window-maximize"></i> Web Instructor
          </h4>
        </a>
      </div>
    </div>

    <!-- BRAND SECTION -->
    <div class="my-6">

      <div class="hidden">
        <img src="images/Photo In PC.png" alt="Amkam Website in computer">
      </div>
      <div class="px-8 bg-gray-200 mt-10 py-12">
        <h4 class="text-2xl leading-tight uppercase text-center mb-2 text-teal-500">I love to be part of a brands' growth</h4>
        <p class="text-gray-600 text-center">My mission is to help businesses grow by making their presence online possible. My joy is to see all businesses move their operations online and be counted a part of that mission.</p>

        <div class="text-center mt-6">
          <a class="bg-teal-500 py-2 px-6 rounded-full text-white mr-3" href="#">Hire Me</a>
          <a class="bg-transparent border border-teal-500 py-2 px-4 rounded-full " href="#">Download CV</a>
        </div>
      </div>

    </div>

    <!-- ABOUT MY SKILLS SECTION -->
    <div class="bg-gray-100 py-12 px-6">
      <!-- About Skills Text -->
      <div class="text-center px-4">
        <h3 class="text-2xl leading-tight uppercase text-center mb-2 text-teal-500">About My Skills</h3>
        <p class="text-gray-600 text-center">
          I have skills in four main areas so far from my experience as a programmer. My experty lies in the following: Web Design , Frontend Development, UI/UX Design and I also teach Web Development at my residence.
        </p>
      </div>

      <!-- Main Skills Cards -->
      <div>
        <!-- Cards -->
        <div v-for="skill in skills " :key="skill.title" class="by-gray-100 rounded overflow-hidden shadow-lg ">
          <div class="py-6 px-4 border mt-8 rounded">
            <div class="text-center mb-5">
              <i :class="skill.icon" class="text-6xl text-teal-500"></i>
            </div>
            <div>
              <h3 class="text-2xl leading-tight uppercase text-center mb-2 text-teal-500">{{ skill.title }}</h3>
              <p class="text-gray-600 text-center">
                {{ skill.content }}
              </p>
            </div>
          </div>
        </div>

      </div>

    </div>


    <!-- MY EXPERIENCE SECTION -->
    <div class="bg-gray-200 py-12 px-4">

      <!-- About Skills Text -->
      <div class="text-center px-4">
        <h3 class="text-2xl leading-tight uppercase text-center mb-2 text-teal-500">My Experience</h3>
        <p class="text-gray-600 text-center">
          I started learning programming at Limkokwing University of Creative Technology at my 3rd day on campus with C++ Programming Language. Below are the experience I've got since I started writing code in 2016.
        </p>
      </div>

      <!-- Experience Percentages -->
      <div class="mt-8 px-4">
        
        <h4 class="text-xl leading-tight mb-2 text-teal-500 uppercase">Web Design</h4>
        <div v-for="experience in webExperience" :key="experience.title" class="relative">
          <div class="flex mb-2 items-center justify-between">
            <div>
              <span class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full text-teal-700 bg-teal-300">
                {{ experience.title }}
              </span>
            </div>
            <div class="text-right">
              <span class="text-xs font-semibold inline-block text-teal-600">
                {{ experience.percent }}
              </span>
            </div>
          </div>
          <div class="overflow-hidden h-2 mb-4 text-xs flex rounded bg-teal-200">
            <div :style="{width: experience.percent}" class="shadow-none flex flex-col text-center whitespace-nowrap text-white justify-center bg-teal-600"></div>
          </div>
        </div>

      </div>

      <div class="mt-8 px-4">
        
        <h4 class="text-xl leading-tight mb-2 text-teal-500 uppercase">Frontend Development</h4>
        <div v-for="experience in frontExperience" :key="experience.title" class="relative">
          <div class="flex mb-2 items-center justify-between">
            <div>
              <span class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full text-teal-700 bg-teal-300">
                {{ experience.title }}
              </span>
            </div>
            <div class="text-right">
              <span class="text-xs font-semibold inline-block text-teal-600">
                {{ experience.percent }}
              </span>
            </div>
          </div>
          <div class="overflow-hidden h-2 mb-4 text-xs flex rounded bg-teal-200">
            <div :style="{width: experience.percent}" class="shadow-none flex flex-col text-center whitespace-nowrap text-white justify-center bg-teal-600"></div>
          </div>
        </div>

      </div>

      <div class="mt-8 px-4">
        
        <h4 class="text-xl leading-tight mb-2 text-teal-500 uppercase">UI/UX Design</h4>
        <div v-for="experience in designExperience" :key="experience.title" class="relative">
          <div class="flex mb-2 items-center justify-between">
            <div>
              <span class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full text-teal-700 bg-teal-300">
                {{ experience.title }}
              </span>
            </div>
            <div class="text-right">
              <span class="text-xs font-semibold inline-block text-teal-600">
                {{ experience.percent }}
              </span>
            </div>
          </div>
          <div class="overflow-hidden h-2 mb-4 text-xs flex rounded bg-teal-200">
            <div :style="{width: experience.percent}" class="shadow-none flex flex-col text-center whitespace-nowrap text-white justify-center bg-teal-600"></div>
          </div>
        </div>

      </div>

    </div>


    <!-- MY EXPERIENCE SECTION -->
    <div class="bg-gray-100 py-12 px-4">

      <!-- About Skills Text -->
      <div class="text-center px-4">
        <h3 class="text-2xl leading-tight uppercase text-center mb-2 text-teal-500">How I Do My Work</h3>
        <p class="text-gray-600 text-center">
          As a software developer or engineer, I strongly follow the principles of software development which deals with Software Development Life Cycle(SDLC).
        </p>
      </div>

      <!-- Work Process -->
       

    </div>

  <Footer />

  </div>
</template>

<script>
import NavBar from "./NavBar"
import Footer from "./Footer"

export default {
  name: "Home",
  components: {
    NavBar,
    Footer
  },
  data(){
    return {
      skills: [
        {title: 'Web Design', content: 'I do Web Design with different tools and technologies, from HTML and CSS, JavaScript, Bootstrap, TailwindCSS, Wordpress, Webflow and Wix.', icon: 'fas fa-desktop'},
        {title: 'Frontend Development', content: 'I do Frontend Development with different modern tools and technologies, from HTML and CSS, JavaScript, Bootstrap, TailwindCSS, Vue JS, React JS and Laravel - web application framework with expressive, elegant syntax.', icon: 'fas fa-laptop'},
        {title: 'UI/UX Design', content: 'I Design professional User Interfaces(UI) and User Experience(UX) with modern tools and technologies, from A4 paper with sketches and wireframing, Adobe XD, Figma for Mobile applications and Web applications.', icon: 'fas fa-desktop'},
        {title: 'Web Instructor', content: 'I faced lots of challenges when I started programming and things get easier as I go along. I realized I should help interested and dedicated students like I was in teaching them Web Development from scratch, to UI/UX and real development with modern technologies.', icon: 'fas fa-window-maximize'}
      ],
      webExperience:[
        {title: 'HTML & CSS', percent: '90%'},
        {title: 'Bootstrap', percent: '90%'},
        {title: 'TailwindCSS', percent: '80%'},
        {title: 'Wordpress', percent: '85%'},
        {title: 'Webflow', percent: '85%'},
      ],
      frontExperience:[
        {title: 'JavaScript', percent: '85%'},
        {title: 'Vue JS', percent: '85%'},
        {title: 'React JS', percent: '85%'},
        {title: 'Laravel', percent: '85%'},
        {title: 'Ruby on Rails', percent: '80%'},
      ],
      designExperience:[
        {title: 'Adobe XD', percent: '90%'},
        {title: 'Photoshop', percent: '90%'},
        {title: 'Figma', percent: '85%'},
        {title: 'Sketch App', percent: '85%'},
      ],
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.heroSection {
  height: 600px;
}
</style>
