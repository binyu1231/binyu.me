<script lang="ts" setup>
const props = defineProps({
  next: {
    default: () => ({})
  },
  prev: {
    default: () => ({})
  }
})
</script>
<template>
  <aside>
    <div class="relative max-w-6xl mx-auto px-4 sm:px-6">
      <div class="pb-12 md:pb-20">
        <div class="max-w-3xl mx-auto">
          <h4 class="h4 font-red-hat-display mb-8">Related articles</h4>

          <!-- Articles container -->
          <div class="grid gap-4 sm:gap-6 sm:grid-cols-2" data-aos-id-relposts>

            <!-- 1st article -->
            <article v-if="prev" class="relative group p-6 text-white" data-aos="fade-down" data-aos-anchor="[data-aos-id-relposts]">
              <figure>
                <img 
                  class="absolute inset-0 w-full h-full object-cover opacity-50 group-hover:opacity-75 transition duration-700 ease-out" 
                  :src="props.prev.cover" 
                  width="372" 
                  height="182" 
                  alt="Related post 01" />
                <div class="absolute inset-0 bg-teal-500 opacity-75 group-hover:opacity-50 transition duration-700 ease-out" aria-hidden="true"></div>
              </figure>
              <div class="relative flex flex-col h-full">
                <header class="flex-grow">
                  <router-link class="hover:underline" :to="`/blog/${props.prev.file}`">
                    <h3 class="text-lg font-red-hat-display font-bold tracking-tight mb-2">
                      {{ props.prev.title }}
                    </h3>
                  </router-link>
                  <div class="text-sm opacity-80">{{ props.prev.desc }}</div>
                </header>
                <footer>
                  <!-- Author meta -->
                  <div class="flex items-center text-sm mt-5">
                    
                    <div>
                      <a class="font-medium hover:underline" href="#0">{{ props.prev.date }}</a>
                    </div>
                  </div>
                </footer>
              </div>
            </article>

            <!-- 2nd article -->
            <article 
              v-if="next" 
              class="relative group p-6 text-white" 
              data-aos="fade-down" 
              data-aos-anchor="[data-aos-id-relposts]" 
              data-aos-delay="200">
              <figure>
                <img 
                  class="absolute inset-0 w-full h-full object-cover opacity-50 group-hover:opacity-75 transition duration-700 ease-out" 
                  :src="props.next.cover" 
                  width="372" 
                  height="182" 
                  alt="Related post 02" />
                <div class="absolute inset-0 bg-purple-500 opacity-75 group-hover:opacity-50 transition duration-700 ease-out" aria-hidden="true"></div>
              </figure>
              <div class="relative flex flex-col h-full">
                <header class="flex-grow">
                  <router-link class="hover:underline" :to="`/blog/${props.next.file}`">
                    <h3 class="text-lg font-red-hat-display font-bold tracking-tight mb-2">
                      {{ props.next.title }}
                    </h3>
                  </router-link>
                  <div class="text-sm opacity-80">{{ props.next.desc }}</div>
                </header>
                <footer>
                  <!-- Author meta -->
                  <div class="flex items-center text-sm mt-5">
                    <!--
                    <a href="#0">
                      <img class="rounded-full flex-shrink-0 mr-3" src="../images/news-author-03.jpg" width="32" height="32" alt="Author 03" />
                    </a>
                     -->
                    <div>
                       <!--<span class="opacity-75">By </span> -->
                      <a class="font-medium hover:underline" href="#0">{{ props.next.date }}</a>
                    </div>
                  </div>
                </footer>
              </div>
            </article>

          </div>
        </div>
      </div>
    </div>
  </aside>
</template>