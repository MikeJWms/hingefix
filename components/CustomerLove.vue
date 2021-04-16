<template>
  <section
    id="testimony"
    class="section-wrapper max-w-7xl mx-auto flex justify-center flex-wrap py-16"
  >
    <section>
      <h2 class="headline my-8 text-4xl text-center">What our customers say</h2>
      <ul class="mv-2 flex flex-wrap">
        <li
          v-for="testimonial in customerTestimonials"
          :key="testimonial"
          class="text-lg w-6/12 p-4 italic"
        >
          {{ testimonial }}
        </li>
      </ul>
    </section>
    <Nuxt-Link to="walloflove" class="mt-8">
      <HfButton label="See more on our wall of love" />
    </Nuxt-Link>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    const customerTestimonials: string[] = [
      `"Perfect. Discreet. Works. Ended up *NOT* replacing the hinges, this
          just works."`,
      `"brought my dear headphones back to life. you're awesome, thanks so
          much!"`,
      `"Wanted to be objective in this review, but now i'm a fanboy!
          Fantastic product!"`,
      `"This saved me up to $30 for full hinge replacements and it's quicker
          to replace."`,
      `"Fantasticly designed piece. Easier than all the Jerry rigged
          suggestions online."`,
      `"Arrived fast, & fixed my headphones. I'm very pleased with the result
          :)"`,
    ]
    return {
      customerTestimonials,
    }
  },
})
</script>