<template>
  <section
    id="experience-timeline"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        xs12
        md12
        deep-orange darken-4
        text-xs-center
        pa-5
        white--text
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateX(5%)"
        />
        <base-heading>
          Experience
        </base-heading>

        <base-text class="mb-5">
          <v-timeline>
            <v-timeline-item
              v-for="experience in experiences"
              :key="experience"
              color="red lighten-2"
              large
            >
              <template v-slot:opposite>
                <span>{{ experience.year }}</span>
              </template>
              <v-card class="elevation-2">
                <v-card-title primary-title>
                  <div>
                    <div class="headline">{{ experience.title }}</div>
                    <span class="grey--text">{{ experience.company}}</span>
                  </div>
                </v-card-title>
                <v-card-text>
                  {{ experience.description }}
                </v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </base-text>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        title: 'Freelance Remote Software Engineer',
        company: 'KUDO Inc.',
        year: 'July 2018 - Present',
        description: 'Develop rapid application features, stabilize and manage application codes independently.',
      },
      {
        title: 'Founder / Product Manager',
        company: 'BazaarFactory',
        year: 'July 2017 - Present',
        description: 'Create and implement effective solutions to e-commerce platforms’ pain-points.',
      },
      {
        title: 'Software Engineer',
        company: 'WhiteHat Engineering',
        year: 'July 2017 - Oct 2017',
        description: 'Maintain complete product flow in React based web application.',
      },
      {
        title: 'Associate Software Engineer',
        company: 'CloudFactory (Sprout Technologies)',
        year: 'July 2016 - July 2017',
        description: 'Maintain complete product flow in React based web application.',
      },
      {
        title: 'Junior Software Engineer',
        company: 'CloudFactory (Sprout Technologies)',
        year: 'June 2015 - July 2016',
        description: 'Maintain complete product flow in React based web application.',
      },
      {
        title: 'Software Engineer Trainee',
        company: 'CloudFactory (Sprout Technologies)',
        year: 'Jan 2015 - June 2016',
        description: 'Maintain complete product flow in React based web application.',
      }
    ]
  })
}
</script>
