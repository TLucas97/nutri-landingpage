<script lang="ts">
  import WiWindy from 'svelte-icons/wi/WiWindy.svelte';
  import { fly } from 'svelte/transition';
  import Button from '../Button.svelte';

  let scroll;
  let visible: boolean = false;

  $: if (scroll > 1000) {
    setTimeout(() => {
      visible = true;
    }, 300);
  } else {
    setTimeout(() => {
      visible = false;
    }, 300);
  }
</script>

<svelte:window bind:scrollY={scroll} />

<main class="w-full bg-[#ffacac23] py-5">
  <div class="w-[1234px] h-[700px] m-auto">
    {#if visible}
      <div
        class="flex justify-between items-center space-x-20"
        transition:fly={{ duration: 700, y: -100 }}
      >
        <div class="w-[50%] h-[450px] shadow-xl">
          <img
            src="./images/people-eating.jpg"
            alt="teste"
            class="w-full h-full object-cover"
          />
        </div>
        <div class="w-[50%] flex justify-start flex-col">
          <div class="w-[90px] h-[90px] text-green-600">
            <WiWindy />
          </div>
          <span class="text-[52px] font-medium"
            >Get the healthy life you always dreamed of</span
          >
          <div class="mt-10 flex items-center space-x-3">
            <img
              src="https://cdn-icons-png.flaticon.com/512/3061/3061427.png"
              alt="asd"
              class="w-[70px] h-[70px]"
            />
            <div class="flex flex-col space-y-2">
              <span class="font-bold text-xl"
                >Tailor-made plan for your own needs</span
              >
              <span
                >Dolor sit amet consectetur adipiscing elit sed do eius mod
                tempor incididunt ut labore et dolore.</span
              >
            </div>
          </div>
          <div class="mt-7 flex items-center space-x-3">
            <img
              src="https://cdn-icons-png.flaticon.com/512/3061/3061427.png"
              alt="asd"
              class="w-[70px] h-[70px]"
            />
            <div class="flex flex-col space-y-2">
              <span class="font-bold text-xl"
                >Tailor-made plan for your own needs</span
              >
              <span
                >Dolor sit amet consectetur adipiscing elit sed do eius mod
                tempor incididunt ut labore et dolore.</span
              >
            </div>
          </div>
          <div class="mt-10">
            <Button size="lg">Ver planos</Button>
          </div>
        </div>
      </div>
    {/if}
  </div>
</main>
