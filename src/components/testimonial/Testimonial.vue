<template>
  <v-row>
    <v-col cols="12">
      <!-- Start Tab Content  -->
      <div class="rn-testimonial-content">
        <v-tabs-items v-model="tab">
          <v-tab-item v-for="item in testimonialContent" :key="item.id">
            <v-card flat v-for="(item, i) in item.content" :key="i">
              <v-card-text>
                <div class="inner">
                  <p>
                    {{ item.description }}
                  </p>
                </div>
                <div class="author-info">
                  <h6>
                    <span>{{ item.name }}</span> -
                    {{ item.designation }}
                  </h6>
                </div>
              </v-card-text>
            </v-card>
          </v-tab-item>
        </v-tabs-items>
        <!-- End .v-tabs-items -->
        <v-tabs v-model="tab" centered hide-slider center-active>
          <v-tab v-for="item in tabItems" :key="item.id">
            <div class="thumb">
              <img :src="item.src" alt="testimonial image" />
            </div>
          </v-tab>
        </v-tabs>
        <!-- End .v-tabs -->
      </div>
      <!-- End .rn-testimonial-content -->
    </v-col>
  </v-row>
</template>

<script>
  export default {
    data() {
      return {
        tab: null,
        testimonialContent: [
          {
            id: 1,
            content: [
              {
                name: "Victoria Tran",
                description:
                  "Niko has a natural interest in learning new things and creative problem solving. He is open to new ideas, listens to feedback and continuously pushes for a more positive user experience.",
                designation: " Digital Media Marketer , International Data Group",
              },
            ],
          },
          {
            id: 2,
            content: [
              {
                name: "Nelson Lourenço",
                description:
                  "He is a level head, from discussing the rationale behind development standards to providing valued feedback on design prototypes.",
                designation: "User Interface Designer, TSD Rental",
              },
            ],
          },
          {
            id: 3,
            content: [
              {
                name: "Phillip Dunn",
                description:
                  "Niko opened our eyes to the creative possibilites and his up-to-date knowledge excited us. He delivered a great looking site and continually offers suggestions for better functionality. He knows his stuff and continues to learn.",
                designation: "Supervisor, Wise Construction",
              },
            ],
          },
          {
            id: 4,
            content: [
              {
                name: "Michael Bourne",
                description:
                  "He's a very organized, determined and intelligent guy who brings a growth mindset to every assignment, and rises to meet new challenges.",
                designation: "Vice President, Matter Communications",
              },
            ],
          },
          {
            id: 5,
            content: [
              {
                name: "Kwadwo Amo-Mensah",
                description:
                  "Niko works well independently as well as with a group. It's nice to work with someone who genuinely cares about what they're doing and the mark they're leaving behind.",
                designation: "Camp Director (Fairfield, CT), ID Tech Camps",
              },
            ],
          },
          {
            id: 6,
            content: [
            {
                name: "Greg Colker",
                description:
                  "We're glad we found Niko! He leveled-up our team by thoughtfully bringing his knowledge and skill in user experience and web development to bear on our project.",
                designation: "Director of Digital Services, CLB Network",
              },
            ],
          },
          {
            id: 7,
            content: [
              {
                name: "Greg Colker",
                description:
                  "With very minimal direction, and in an unfamiliar code base, Niko quickly got our project moving in the right direction and saw it through to the end with testing and revisions.",
                designation: "Director of Digital Services, CLB Network",
              },
            ],
          },
        ],

        tabItems: [
          {
            id: 1,
            src: require("../../assets/images/client/testimonial-1.jpg"),
          },
          {
            id: 2,
            src: require("../../assets/images/client/testimonial-2.jpg"),
          },
          {
            id: 3,
            src: require("../../assets/images/client/testimonial-3.jpg"),
          },
          {
            id: 4,
            src: require("../../assets/images/client/testimonial-4.jpg"),
          },
          {
            id: 5,
            src: require("../../assets/images/client/testimonial-5.jpg"),
          },
          {
            id: 6,
            src: require("../../assets/images/client/testimonial-6.jpg"),
          },
          {
            id: 7,
            src: require("../../assets/images/client/testimonial-7.jpg"),
          },
        ],
      };
    },
  };
</script>
