<template>
  <section class="section-wrapper w-full" id="problem">
    <section class="max-w-5xl mx-auto flex justify-center flex-wrap py-16">
      <div>
        <h2 class="headline m-8 text-4xl text-center">The problem...</h2>
        <div class="">
          <img
            class="w-80 rounded-full float-left mr-5"
            id="problem-image"
            src="@/assets/IMG_4350_crop_tiny.jpeg"
            alt=""
          />
          <div class="copy pt-6">
            <p class="my-4 text-lg leading-relaxed">
              We love our M50 headphones, but they have one major design flaw -
              the hinges. Over time, a part in the hinge breaks and prohibits
              the ear cup from hugging your ear.
            </p>
            <p class="my-4 text-lg leading-relaxed">
              This effects all versions of the M50: original ATH-M50 headphones
              with the attached cable, ATH-M50x with the interchangeable cable,
              and the new ATH-M50xBT Bluetooth headphones.
            </p>
            <p class="my-4 text-lg leading-relaxed">
              That's why we made HingeFix.
            </p>
          </div>
        </div>
      </div>
    </section>
  </section>
</template>

<style scoped>
#problem-image {
  shape-outside: circle(50%);
}
</style>