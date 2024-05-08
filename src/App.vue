<script setup>
import { ref } from 'vue';

const name = ref('Paullaster Okoth');
const position = ref('Web Developer');
const experience = ref(
  [
    {
      employer: "Kinetics Technologies",
      position: "Web Developer",
      duration: "March 2023 - Present",
      location: "Nairobi, Kenya",
      roles: [
        {
          description: "Spearheaded redesign of Kinetics's membership platform, prioritizing user experience by developing intuitive UIs tailored to user needs and preferences, which generated 3 sales opportunity for the membership platform in Nairobi in Q1 2024 and achieved 18% increase in sales",

        },
        {
          description: "Played a pivotal role in development of Kinetics's Electronic Voting Systems with user centric design, significatly enhancing voting process and security. The voting ststem facilitated 46% increase in revenue in Q1 2024, gaining reputation among clients."
        },
        {
          description: "Championed a 40% Reduction in Client Support Resolution Time:  Led the development team in implementing strategic improvements to our software support infrastructure. This resulted in a remarkable 40% decrease in client support resolution time, significantly enhancing customer satisfaction and fostering trust within our client base. This achievement has also bolstered the company's reputation for providing exceptional customer service."

        },
        {
          description: "Led the development of Kinetics's research proposals' reveiew plaftform with intuitive UI, significantly ehnacing the research grants awards with a reduction from 6 months to 1 month  by hugely slashing review time by 80%, increasing revenue by 20% in Q3 2023"
        }
      ],

    },
    {
      employer: "Sama ",
      position: "Junior Developer",
      duration: "October 2020 - February 2023",
      location: "Nairobi, Kenya",
      roles: [
        {
          description: "Championed a User-Centric Redesign of SamaHub: Played a pivotal role in the redesign of SamaHub, our internal work platform. By prioritizing user experience (UX) and user interface (UI) improvements, we created a more intuitive and streamlined platform. This resulted in a significant increase in efficiency for over 2,000 employees, enabling them to complete daily tasks faster and with greater ease. This enhanced user experience has contributed to a more productive and engaged workforce.",

        },
        {
          description: "Empowered 2,000+ Learners: Collaborated on building a React.js dashboard for Sama Kenya's Learning Management System (LMS) that facilitated self-paced learning for employees, fostering a culture of continuous skills development."
        },
      ],

    },
    {
      employer: "Huawei, Kenya ",
      position: "HMTMP",
      duration: "July 2023 - November 2022",
      location: "Nairobi, Kenya",
      roles: [
        {
          description: "Championed a User-Centric Redesign of SamaHub: Played a pivotal role in the redesign of SamaHub, our internal work platform. By prioritizing user experience (UX) and user interface (UI) improvements, we created a more intuitive and streamlined platform. This resulted in a significant increase in efficiency for over 2,000 employees, enabling them to complete daily tasks faster and with greater ease. This enhanced user experience has contributed to a more productive and engaged workforce.",

        },
        {
          description: "Empowered 2,000+ Learners: Collaborated on building a React.js dashboard for Sama Kenya's Learning Management System (LMS) that facilitated self-paced learning for employees, fostering a culture of continuous skills development."
        },
      ],

    }
  ]
);

function dateFormatter(period) {
  const [start, end] = period.split('-');
  return `${start} - ${end}`;
}
</script>

<template>
  <header>
   <h1>{{ name }}</h1>
   <nav>
    <h3>{{ position }}</h3>
    <div>
      <p><RouterLink to="https://github.com/paullaster" >paullaster</RouterLink></p>
      <p><RouterLink to="" >paullasterokoth98@gmail.com</RouterLink></p>
      <p><RouterLink to="" >+254700258098</RouterLink></p>
    </div>
   </nav>
  </header>
  <main>
    <section class="main">
      <div class="experince">
        <h1 class="theme">Experience</h1>
       <div v-for="e in experience" :key="e.employer" class="card-experience">
        <h3 class="organization">
          <span> {{  e.employer }}</span>
          <span> {{ e.position}}</span>
        </h3>
        <p class="duration"> {{  dateFormatter(e.duration) }}, {{ e.location }} </p>
        <ul v-for="(role, index) in e.roles" :key="index">
          <li> {{ role.description }}</li>
        </ul>
       </div>
      </div>
      <div class="projects">
        <!-- <h1>Projects</h1> -->
        <div>

        </div>
      </div>
    </section>
    <aside class="sidebar">
      <div class="education">
        <h1 class="theme">Education</h1>
        <div>
          <h3 class="organization">Multimedia University of Kenya</h3>
          <h4>Bachelor of Science in Information Technology, Nairobi, Kenya</h4>
          <h5>Aug 2017 - Dec 2021, Second class Honors (Upper division)</h5>
        </div>
      </div>
      <div class="skills">
        <h1 class="theme">Skills</h1>
        <ul>
          <li>
            Debugging
          </li>
          <li>Developing intuitive UIs</li>
          <li>Developing Scalable RESTful APIs</li>
          <li>Developing Backend applications</li>
          <li>Cloud, Windows and Linux administration</li>
          <li>Blackbox and Headless Testing Frontend and Backend application</li>
          <li>Containerizing applications</li>
          <li>Version Control</li>
          <li>Unit Testing</li>
          <li>Database design</li>
        </ul>
      </div>
      <div class="tools">
        <h1 class="theme">Tools</h1>
        <ul>
          <li>HTML/CSS/JavaScript</li>
          <li>React.js/Vue.js</li>
          <li>Java, Node.js/Express.js</li>
          <li>PostgreSQL, MySQL, MongoDB</li>
          <li>Git</li>
          <li>Jest, Postman, Cypress</li>
          <li>Docker</li>
          <li>AWS, Microsoft Azure, Digital ocean cloud</li>
        </ul>
      </div>
    </aside>
  </main>
</template>

<style scoped>

header {
  margin-bottom: 2rem;

  h1 {
    font-size: 2.5rem;
    font-weight: 900;
  }
  nav {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;

    h3 {
      font-size: 1.5rem;
      font-weight: 700;
    }
    div {
      display: flex;
      flex-direction: row;
      margin-left: 4rem;

      /* p {
        margin-bottom: 0.5rem;
        font-size: 1rem;
        font-weight: 200;
        padding: .5rem;
      } */
    }
  }
}
main  {
  display: grid;
  grid-template-columns: 4fr 1fr;
  grid-template-rows: 1fr 1fr;
  grid-gap: 2rem;
  margin-bottom: 2rem;
}
.theme {
  font-size: 1.6rem;
  font-weight: 900;
}
.duration { 
  font-size: 1rem;
  font-weight: 200;
}
.organization {
  font-size: 1.2rem;
  font-weight: 900;
}
.card-experience{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 1rem;
}
</style>
