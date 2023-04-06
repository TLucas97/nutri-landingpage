<script lang="ts">
  import Button from '../Button.svelte';
  import WiWindy from 'svelte-icons/wi/WiWindy.svelte';
  import { fly } from 'svelte/transition';
  import { onMount } from 'svelte';

  let visible: boolean = false;

  onMount(() => {
    setTimeout(() => {
      visible = true;
    }, 300);
  });
</script>

<main class="w-full h-[700px] bg-[#e1ffb128] flex items-center justify-center">
  <div class="w-[1234px] m-auto flex items-center justify-center">
    {#if visible}
      <div class="w-[900px]" transition:fly={{ duration: 500, y: 200 }}>
        <div class="w-[70px] h-[70px] text-green-600">
          <WiWindy />
        </div>
        <div class="flex flex-col text-[60px] font-medium w-full">
          <span>Transforme sua saúde</span>
          <span>através da alimentação</span>
        </div>
        <div class="mt-5">
          <span
            >Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
            nisi ut aliquip ex ea commodo consequat aute irure dolor in
            reprehenderit.</span
          >
        </div>
        <div class="mt-10 flex space-x-5">
          <Button theme="blue" size="lg">Planos</Button>
          <Button theme="black" size="lg">Contato</Button>
        </div>
      </div>
      <div class="ml-[10em] w-[500px] h-[600px] shadow-xl rounded-full" transition:fly={{ duration: 500, y: 200 }}>
        <img
          src="./images/nutri-example.png"
          alt="asd"
          class="w-full h-full object-cover rounded-full"
        />
      </div>
    {/if}
  </div>
</main>
