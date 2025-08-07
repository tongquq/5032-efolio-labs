<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import MyName from './components/MyName.vue'
</script>

<template>
  <!-- Header section: logo on the left, greetings on the right -->
  <header class="app-header">
    <!-- Vue logo -->
    <img
      src="./assets/logo.svg"
      alt="Vue logo"
      class="logo"
      width="125"
      height="125"
    />

    <!-- Text container: success message and personal greeting -->
    <div class="text-block">
      <!-- Built-in HelloWorld component -->
      <div class="greeting">
        <HelloWorld msg="You did it!" />
      </div>
      <!-- Custom MyName component -->
      <div class="your-name">
        <MyName />
      </div>
    </div>
  </header>

  <!-- Main content: the original welcome timeline component -->
  <main class="app-main">
    <TheWelcome />
  </main>
</template>

<style scoped>
/* Layout: two columns, center-aligned, with a gap */
.app-header {
  display: grid;
  grid-template-columns: auto 1fr;
  align-items: center;
  gap: 2rem;
  padding: 2rem 1rem;
}

/* Logo alignment: stick to the right of its grid cell */
.logo {
  justify-self: end;
}

/* Text block: stack messages vertically with spacing */
.text-block {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.5rem;
}

/* Personal greeting: larger font, bold, with top/bottom margin */
.your-name h2.my-name {
  font-size: 2rem;
  font-weight: 700;
  margin: 1rem 0;
  color: #42b883; /* Vue brand green */
}

/* Main section padding for consistency */
.app-main {
  padding: 1rem;
}
</style>
