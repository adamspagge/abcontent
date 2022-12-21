<script setup>
const { site } = useAppConfig()
useHead({
  titleTemplate: '%s | ' + site.title,
  link: [
    { rel: 'apple-touch-icon', sizes: '180x180', href: '/apple-touch-icon.png' },
    { rel: 'icon', type: 'image/png', sizes: '32x32', href: '/favicon-32x32.png' },
    { rel: 'icon', type: 'image/png', sizes: '16x16', href: '/favicon-16x16.png' },
    { rel: 'manifest', href: '/site.webmanifest' },
    { rel: 'mask-icon', href: '/safari-pinned-tab.svg', color: '#5bbad5' },
    { rel: 'icon', type: 'image/x-icon', href: '/favicon.png' }
  ],
  bodyAttrs: {
    class: ''
  }
})
</script>
<template>
  <div min-h-screen flex flex-col>
    <TheHeader p-4 mb-8 />
    <main p-4 lg:p-0 max-w-prose m-auto flex-grow>
      <NuxtPage />
    </main>
    <TheFooter p-4 min-h-30 />
  </div>
</template>
<style lang="sass">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,800;1,300;1,400;1,800&display=swap')
*
  font-family: 'Open Sans', sans-serif
  box-sizing: border-box
html, body
  width: 100vw
  overflow-x: hidden
body
  margin-left: 0
  margin-right: 0
  margin-bottom: 0
  
</style>