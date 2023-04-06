<script lang="ts">
  import { fly } from 'svelte/transition';
  import { onMount } from 'svelte';
  import Button from './Button.svelte';

  let scroll;
  let heightView = false;
  let heightSize: string = 'h-[100px]';
  let currentOpacity: string = '';
  let currentTextSize: string = 'text-lg';
  let heightColor: string = '';

  $: {
    if (scroll > 80) {
      heightSize = 'h-[50px]';
      currentOpacity = 'opacity-80';
      currentTextSize = 'text-base';
      heightColor = 'bg-white';
    } else {
      heightSize = 'h-[100px]';
      currentOpacity = '';
      currentTextSize = 'text-lg';
      heightColor = '';
    }
  }

  onMount(() => {
    setTimeout(() => {
      heightView = true;
    }, 600);
  });
</script>

<svelte:window bind:scrollY={scroll} />

<main
  class={`w-full ${heightSize} ${currentOpacity} ${heightColor} fixed top-0 transition ease-in-out z-10`}
  on:mouseenter={() => (currentOpacity = 'opacity-100')}
  on:mouseleave={() => (currentOpacity = 'opacity-80')}
  class:shadow-xl={scroll > 80}
>
  {#if heightView}
    <div
      transition:fly={{ duration: 1000 }}
      class="w-[1234px] m-auto h-full flex justify-between items-center"
    >
      <div class="flex space-x-3 items-end">
        <img src="./images/apple.png" alt="img" class="w-[40px] h-[40px]" />
        <span class="text-2xl font-extrabold">FlaviaNutri</span>
      </div>
      <div class={`flex space-x-10 ${currentTextSize}`}>
        <button class="hover:text-green-600 hover:underline transition-all ease-in-out">Home</button>
        <button class="hover:text-green-600 hover:underline transition-all ease-in-out">Sobre mim</button>
        <button class="hover:text-green-600 hover:underline transition-all ease-in-out">Insta</button>
        <button class="hover:text-green-600 hover:underline transition-all ease-in-out">Contato</button>
        <Button size={scroll > 80 ? 'sm' : 'md'}>Planos</Button>
      </div>
    </div>
  {/if}
</main>
