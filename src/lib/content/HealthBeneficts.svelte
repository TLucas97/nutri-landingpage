<script lang="ts">
  import WiWindy from 'svelte-icons/wi/WiWindy.svelte';
  import InfoCard from '../InfoCard.svelte';
  import { fly } from 'svelte/transition';
  import Button from '../Button.svelte';

  const beneficts = [
    {
      image: 'https://cdn-icons-png.flaticon.com/512/415/415733.png',
      title: 'Aprenda a se alimentar de forma saudável',
      description:
        'Excepteur sint occaecat cupidatat nones proident sunt in culpa qui officia dese.',
    },
    {
      image: 'https://cdn-icons-png.flaticon.com/512/1535/1535019.png',
      title: 'Alcance seus objetivos',
      description:
        'Excepteur sint occaecat cupidatat nones proident sunt in culpa qui officia dese.',
    },
    {
      image: 'https://cdn-icons-png.flaticon.com/512/7346/7346053.png',
      title: 'Checkups periódicos',
      description:
        'Excepteur sint occaecat cupidatat nones proident sunt in culpa qui officia dese.',
    },
  ];

  let scroll;
  let visible: boolean = false;

  $: if (scroll > 370) {
    setTimeout(() => {
      visible = true;
    }, 300);
  } else if (scroll < 360){
    setTimeout(() => {
      visible = false;
    }, 300);
  }
</script>

<svelte:window bind:scrollY={scroll} />

<main class="w-[1234px] h-[800px] m-auto">
  <div class="w-full h-full flex items-center flex-col">
    <div class="w-[100px] h-[100px] text-green-600">
      <WiWindy />
    </div>
    <div class="flex items-center justify-center flex-col">
      <span class="text-[54px]">Oque você ganha?</span>
      <span class="w-[400px] text-center text-gray-500"
        >Dolor sit amet consectetur adipiscing elit sed do eius mod tempor
        incididunt ut labore et dolore.</span
      >
    </div>
    <div class="h-[300px] mt-5">
      {#if visible}
        <div
          class="flex justify-center items-center space-x-10 mt-10 w-full"
          transition:fly={{ duration: 700, y: -100 }}
        >
          {#each beneficts as benefict}
            <InfoCard>
              <div class="flex flex-col items-center justify-between h-full">
                <div class="flex flex-col space-y-6 items-center justify-center">
                  <img
                    src={benefict.image}
                    alt=""
                    class="w-[150px] h-[150px]"
                  />
                  <span class="text-xl font-medium text-center"
                    >{benefict.title}</span
                  >
                </div>
                <div
                  class="flex flex-col items-center justify-center space-y-4 mt-2"
                >
                  <span class="text-sm w-[300px] text-center text-gray-600"
                    >{benefict.description}</span
                  >
                </div>
              </div>
            </InfoCard>
          {/each}
        </div>
        <div class="flex justify-center items-center space-x-6 mt-14">
          <Button size="lg" theme="blue">Ver planos</Button>
          <Button size="lg" theme="black">Entrar em contato</Button>
        </div>
      {/if}
    </div>
  </div>
</main>
