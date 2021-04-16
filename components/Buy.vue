<template>
  <div class="section-wrapper">
    <section
      class="max-w-5xl mx-auto flex justify-center flex-wrap py-16"
      id="cta"
    >
      <h2 class="headline my-8 text-4xl text-center">How to buy</h2>
      <p class="mb-12">
        Hinge Fix is available in a kit and 3D printable files. If you have
        access to a 3Dprinter, buying the files is a great way to save on
        shipping.
      </p>

      <div class="flex flex-wrap">
        <div
          class="card max-w-sm p-6 border border-gray-400 rounded-lg text-center m-4"
          v-for="product in products"
          :key="product.title"
        >
          <img class="card__image" :src="product.image" alt="" />
          <h3 class="text-center text-lg font-semibold my-4">
            {{ product.title }}
          </h3>
          <p class="mb-2">
            {{ product.description }}
          </p>

          <a id="buy-now" class="button" :href="product.primaryLink">
            <HfButton class="my-4" :label="product.primaryLabel" />
          </a>
          <a
            class="button-link block text-blue-600 hover:text-blue-900"
            :href="product.secondaryLink"
          >
            {{ product.secondaryLabel }}
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    const products = [
      {
        image: require('@/assets/hinge_fix_kit.jpeg'),
        title: 'Hinge Repair Kit',
        description:
          'All the parts you need to repair two (2) hinges. The easiest way to repair your headphones. Requires a small phillips screwdriver.',
        primaryLink: 'https://gum.co/jFpnA',
        primaryLabel: 'Buy Now',
        secondaryLink: 'https://www.ebay.com/itm/283974047847',
        secondaryLabel: 'Also available on eBay',
      },
      {
        image: require('@/assets/hinge_fix_file.jpeg'),
        title: 'Hinge Repair File',
        description:
          '3D print the parts and supply your own screws. Perfect for those that have access to a 3D printer and want to save on shipping.',
        primaryLink: 'https://gum.co/hISlr?wanted=true',
        primaryLabel: 'Buy the file',
        secondaryLink:
          'https://pinshape.com/items/47023-3d-printed-ath-m50x-hinge-repair',
        secondaryLabel: 'Also available on Pinshape',
      },
    ]
    return { products }
  },
})
</script>