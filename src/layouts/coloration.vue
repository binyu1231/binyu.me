<template>
  <PageLayout
    cover="https://xinghe-blog-bucket.oss-cn-beijing.aliyuncs.com/img/blog-coloration-cover.jpg"
  >
    <div class="relative max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20">
        <!-- Section header -->
        <div class="max-w-3xl mx-auto text-center pb-6 pt-10 md:pb-10 md:pt-14" data-aos="fade-down">
          <h2 class="h2 font-red-hat-display">Coloration Code Document</h2>
        </div>

        <div
          class="max-w-xs sm:max-w-none mx-auto md:max-w-none lg:max-w-none grid gap-4 md:gap-6 sm:grid-cols-2 md:grid-cols-3"
          data-aos-id-rellinks
        >
          <a target="_blank" href="//coloration.github.io/#/kit">
            <FeatureCard
              title="Kit"
              desc="常用的工具函数和浏览器功能扩展, 简化日常前端开发工作量"
              class="bg-gradient-to-tr from-teal-500 to-teal-400 dark:to-teal-500"
              data-aos-delay="100"
            >
              <svg class="w-8 h-8 mb-3" viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg">
                <path
                  class="fill-current"
                  d="M11.586 23l-3-3L10 18.586 15.414 24 10 29.414 8.586 28l3-3H3v-8h2v6h6.586zm8.828-14l3 3L22 13.414 16.586 8 22 2.586 23.414 4l-3 3H29v8h-2V9h-6.586zM7 14A7 7 0 117 0a7 7 0 010 14zm0-2A5 5 0 107 2a5 5 0 000 10zm18 20a7 7 0 110-14 7 7 0 010 14zm0-2a5 5 0 100-10 5 5 0 000 10z"
                  fill="#FFF"
                  fill-rule="nonzero"
                />
              </svg>
            </FeatureCard>
          </a>

          <a target="_blank" href="//coloration.github.io/#/asker">
            <FeatureCard
              title="Asker"
              desc="功能齐全的客户端HTTP工具，代码量小功能齐全"
              class="bg-gradient-to-tr from-purple-500 to-purple-400 dark:to-purple-500"
              data-aos-delay="200"
            >
              <svg class="w-8 h-8 mb-3" viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg">
                <path
                  class="fill-current"
                  d="M25.324 21H22v-2h3.324a6 6 0 014.992 2.671l1.206 1.81-1.16.451-15.167 5.9a7 7 0 01-6.3-.619L0 23.55V13h3c2.994 0 5.922 1.078 7.5 3H15a6 6 0 016 6v1H8v-2h10.874A4.002 4.002 0 0015 18H9.466l-.297-.443C8.123 15.995 5.612 15 3 15H2v7.451l7.97 5.075a5 5 0 004.5.442l13.996-5.444A4 4 0 0025.324 21zM25.6 8.439L19 15.27l-.72-.744-5.884-6.092a5.046 5.046 0 010-6.968A4.74 4.74 0 0119 1.223a4.738 4.738 0 016.603.243A5.046 5.046 0 0125.6 8.44zm-1.442-1.385a3.045 3.045 0 00-.001-4.206 2.738 2.738 0 00-4.307.445l-.849 1.371-.85-1.37a2.74 2.74 0 00-4.309-.447 3.045 3.045 0 00-.004 4.202L19 12.392l5.158-5.338z"
                  fill="#FFF"
                  fill-rule="nonzero"
                />
              </svg>
            </FeatureCard>
          </a>

          <a target="_blank" href="//coloration.github.io/island" class="h-full">
            <FeatureCard
              title="island"
              desc="Vue UI component library with storybook"
              class="bg-gradient-to-tr h-full from-indigo-500 to-indigo-400 dark:to-indigo-500 sm:col-span-2 md:col-auto"
              data-aos-delay="300"
            >
              <clarity:vmw-app-line class="w-8 h-8 mb-3" />
            </FeatureCard>
          </a>

          <a target="_blank" href="//coloration.github.io" class="h-full">
            <FeatureCard
              title="Coming Soon!"
              desc="更多有趣工具正在路上, 前往 Coloration 主页"
              class="bg-gradient-to-tr h-full from-indigo-500 to-indigo-400 dark:to-indigo-500 sm:col-span-2 md:col-auto"
              data-aos-delay="300"
            >
              <svg class="w-8 h-8 mb-3" viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg">
                <path
                  class="fill-current"
                  d="M11.697 9.254l-4.3-4.3a14.14 14.14 0 00-2.443 2.442l4.3 4.3a8.03 8.03 0 012.443-2.442zm1.932-.896a8.036 8.036 0 014.742 0l4.538-4.538a14.027 14.027 0 00-13.818 0l4.538 4.538zm6.674.896a8.03 8.03 0 012.443 2.443l4.3-4.3a14.14 14.14 0 00-2.443-2.443l-4.3 4.3zm3.339 4.375a8.036 8.036 0 010 4.742l4.538 4.538a14.027 14.027 0 000-13.818l-4.538 4.538zm-.896 6.674a8.029 8.029 0 01-2.443 2.443l4.3 4.3a14.14 14.14 0 002.443-2.443l-4.3-4.3zm-4.375 3.34a8.036 8.036 0 01-4.742 0L9.091 28.18a14.027 14.027 0 0013.818 0l-4.538-4.538zm-6.674-.897a8.029 8.029 0 01-2.443-2.443l-4.3 4.3a14.14 14.14 0 002.443 2.443l4.3-4.3zm-3.34-4.375a8.036 8.036 0 010-4.742L3.82 9.09a14.027 14.027 0 000 13.818l4.538-4.538zm18.956 8.943c-6.248 6.248-16.378 6.248-22.627 0-6.248-6.249-6.248-16.38 0-22.628 6.249-6.248 16.38-6.248 22.627 0 6.249 6.249 6.249 16.38 0 22.628zm-7.07-7.071a6 6 0 10-8.486-8.486 6 6 0 008.485 8.486z"
                />
              </svg>
            </FeatureCard>
          </a>
        </div>
      </div>
    </div>

    <router-view />
  </PageLayout>
</template>
