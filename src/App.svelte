<script>
  import Toggle from "./components/Toggle.svelte";
  import RandomNumber from "./components/RandomNumber.svelte";
  import UserInputs from "./components/UserInputs.svelte";

  let darkMode = true;
</script>

<style lang="postcss">
  a {
    @apply bg-pink-600 rounded text-white;
  }
  a:hover {
    @apply bg-pink-500;
  }
</style>

<main class="{darkMode ? 'dark' : ''}">
  <div class="w-full bg-pink-200 dark:bg-gray-800">
    <div class="container mx-auto text-center py-4">
      <h1 class="m-8 font-bold text-4xl dark:text-white">Welcome To The Guessing Game</h1>
      <div class="my-4">
        <a
          target="_blank"
          class="p-2 m-2"
          href="">
          Star Github
        </a>
      </div>
      <Toggle label="Dark Mode" bind:value="{darkMode}" />
      <div class="container flex">
        <div class="flex-auto bg-red-800 m-6 rounded-md">
          <RandomNumber />
        </div>
        <div class="flex-auto bg-blue-800 m-6 rounded-md">
          <UserInputs />
        </div>
      </div>
    </div>
  </div>
</main>
