<template>
  <section class="container grid">
    <h2>Work</h2>
    <section>
      <p
        class="description"
      >From design to production, I work with creative minds to build awesome, responsive and accessible web projects, here are some of my personal projects</p>
      <div class="work-grid animation-reveal-bottom">
        <div class="grid-item" style="position: relative" v-for="work in works" :key="work.no">
          <!-- <big>{{ work.no }}</big> -->
          <article>
            <div class="work">
              <h5 class="work__title">
                <b>{{ work.title }}</b>
              </h5>
              <p class="work__description">{{ work.description }}</p>
              <span class="work__link" v-if="work.link">
                <a :href="work.link.live" v-if="work.link.live">website</a>
                <a :href="work.link.repository" v-if="work.link.repository">repository</a>
              </span>
              <a href="#" class="work__link" title="Work In Progress" v-else>WIP</a>
              <div class="work__tech">
                <span class="work__tech--circle" v-for="(tech, index)  in work.tech" :key="index">
                  <img
                    src="../../assets/images/vuejs.svg"
                    height="25"
                    width="25"
                    v-if="tech === 'V'"
                    alt="Vue Js"
                  />
                  <img
                    src="../../assets/images/react.svg"
                    height="25"
                    width="25"
                    v-else-if="tech === 'R'"
                    alt="React Js"
                  />
                  <img
                    src="../../assets/images/html-5.svg"
                    height="25"
                    width="25"
                    v-if="tech === 'H'"
                    alt="HTML"
                  />
                  <img
                    src="../../assets/images/css3.svg"
                    height="25"
                    width="25"
                    v-else-if="tech === 'C'"
                    alt="CSS"
                  />
                </span>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
export default {
  data() {
    return {
      works: [
        {
          no: "01",
          title: "Daily Sketches",
          description:
            "I take time out of my schedule to convert at least one dribbble or figma design using CSS",
          link: {
            live: "https://seyidayo.github.io/Daily-Sketches/",
            repository: "https://github.com/Seyidayo/Figma-Sketches"
          },
          tech: ["H", "C"]
        },
        {
          no: "02",
          title: "Fuudzie.com",
          description: "An Ecommerce site to carry out operations",

          link: {
            live: "https://fuudzie.com"
          },
          tech: ["R"]
        },
        {
          no: "03",
          title: "Github Repository",
          description: "Finding time to learn more technologies and projects",
          link: { live: "https://github.com/seyidayo" }
        }
        // ,{
        //   no: "03",
        //   title: "Sportage shoes",
        //   description:
        //     "A minimal shoe store done to take a stab at this MERN stack every one is buzzing about",

        //   link: {
        //     live: "https://sportage.herokuapp.com",
        //     repository:
        //       "https://bitbucket.org/FaithIdowu/sportage-fe/src/master/"
        //   },
        //   tech: ["R"]
        // },
        // {
        //   no: "03",
        //   title: "Zoropay",
        //   description:
        //     "Zoropay helps students pay their school fees by offering a fair loan and payback system",
        //   link: { live: "https://zoropay.ng" },
        //   tech: ["R"]
        // },
        // {
        //   no: "05",
        //   title: "Breaking Bad",
        //   description:
        //     "Zoropay helps students pay their school fees by offering a fair loan and payback system",

        //   tech: ["V"]
        // }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.container {
  min-block-size: 100%;
}

.work {
  position: relative;
  block-size: 100%;
  inline-size: 100%;
}

.work__title {
  block-size: 20%;
  font-size: 1.4rem;
}

.work__description {
  block-size: 50%;
  font-size: 1.2rem;
  line-height: 165%;
}

.work__link {
  position: absolute;
  bottom: 0;
  right: 0;
  text-align: end;
  a {
    display: block;
  }
}

.work__tech {
  position: absolute;
  block-size: 50px;
  top: -2.5rem;
  right: -2.5rem;
  display: flex;
  flex-direction: row;

  .work__tech--circle {
    inline-size: 35px;
    block-size: 35px;
    background-color: var(--bg-color);
    border: var(--border-size) var(--bg-alt-color) solid;
    border-radius: 50%;
    font-size: 1.3em;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-inline-start: 0.25em;
  }
}
</style>
