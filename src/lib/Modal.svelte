<script>
  import { blur } from 'svelte/transition';
  import FaSpinner from 'svelte-icons/fa/FaSpinner.svelte';

  export let closeModal;
  let isLoading = true;
</script>

<div class="fixed z-10 inset-0 flex items-center justify-center bg-[#000000d7]">
  <div class="w-[1000px] h-[650px] bg-white" transition:blur>
    <div class="relative">
      <button
        class="absolute top-0 right-0 text-gray-400 hover:text-gray-500 focus:outline-none focus:text-gray-500"
        on:click={closeModal}
      >
        <svg class="h-8 w-8 bg-red-400" viewBox="0 0 24 24">
          <path
            d="M18 6L6 18M6 6l12 12"
            stroke="white"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </button>
    </div>
    <iframe
      class="w-full h-full"
      style={isLoading ? 'display:none' : 'display:block'}
      title="instagram-video"
      src="https://www.instagram.com/p/CS-K5eIAlRG/embed"
      frameborder="0"
      allowfullscreen
      on:load={() => (isLoading = false)}
    />
    {#if isLoading}
      <div class="flex justify-center items-center h-full">
        <div class="animate-spin -ml-1 mr-3 h-10 w-10 text-gray-700">
          <FaSpinner />
        </div>
      </div>
    {/if}
  </div>
</div>
