<DarkMode>
  <template v-slot="{ mode }">
    <MyLightIcon v-show="mode === 'light'">
    <MyDarkIcon v-show="mode === 'dark'">
    <MySystemIcon v-show="mode === 'system'">
  </template>
</DarkMode>


<script>
// ...
</script>

<style>
:root {
  --bg: #fff;
  --color: #333333;
}

html.dark-mode {
  --bg: #232b32;
  --color: #ddd8ca;
}

body {
  background-color: var(--bg);
  color: var(--color);
}
</style>
