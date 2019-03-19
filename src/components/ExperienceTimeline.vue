<template>
  <v-container
    grid-list-xl
    mt-4
  >
    <h1 class="mb-5 display-2 text-xs-center font-weight-bold text-uppercase teal--text">
      Experience
    </h1>
    <v-timeline>
      <v-timeline-item
        v-for="(experience, i) in experiences"
        :key="i"
        :color="experience.color"
        small
      >
        <template v-slot:opposite>
          <span
            :class="`headline font-weight-bold ${experience.color}--text`"
            v-text="experience.year"
          />
        </template>
        <div class="py-3">
          <h2 :class="`headline font-weight-light mb-3 ${experience.color}--text`">
            {{ experience.title }}
          </h2>
          <h3 :class="`sub-heading font-weight-bold mb-3 ${experience.color}--text`">
            {{ experience.company }}
          </h3>
          <div>
            {{ experience.description }}
          </div>
        </div>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        title: 'Freelance Remote Software Engineer',
        company: 'KUDO Inc.',
        year: 'July 2018 - Present',
        color: 'cyan',
        description: 'Develop rapid application features, stabilize and manage application codes independently.'
      },
      {
        title: 'Founder / Product Manager',
        company: 'BazaarFactory',
        year: 'July 2017 - Present',
        color: 'green',
        description: 'Create and implement effective solutions to e-commerce platforms’ pain-points.'
      },
      {
        title: 'Software Engineer',
        company: 'WhiteHat Engineering',
        year: 'July 2017 - Oct 2017',
        color: 'orange',
        description: 'Maintain complete product flow in React based web application.'
      },
      {
        title: 'Associate Software Engineer',
        company: 'CloudFactory (Sprout Technologies)',
        year: 'July 2016 - July 2017',
        color: 'pink',
        description: 'Maintain complete product flow in React based web application.'
      },
      {
        title: 'Junior Software Engineer',
        company: 'CloudFactory (Sprout Technologies)',
        year: 'June 2015 - July 2016',
        color: 'pink',
        description: 'Maintain complete product flow in React based web application.'
      },
      {
        title: 'Software Engineer Trainee',
        company: 'CloudFactory (Sprout Technologies)',
        year: 'Jan 2015 - June 2016',
        color: 'pink',
        description: 'Maintain complete product flow in React based web application.'
      }
    ]
  })
}
</script>
