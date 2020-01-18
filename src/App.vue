<template>
  <div id="app" class="antialiased text-gray-900">
    <div class="bg-white min-h-screen">
      <Navbar/>
      <Content/>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar'
import Content from './components/Content'
export default {
  name: 'app',
  components: {
    Navbar,
    Content
  },
}
</script>

<style src="./assets/tailwind.css"></style>
