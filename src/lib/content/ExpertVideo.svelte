<script lang="ts">
  import WiWindy from 'svelte-icons/wi/WiWindy.svelte';
  import FaPlay from 'svelte-icons/fa/FaPlay.svelte';
  import Modal from '../Modal.svelte';

  let isHovering: boolean = false;
  let oneHundredValue: number = 0;
  let fourHundredValue: number = 0;
  let twentyFiveHundredValue: number = 0;
  let hasCounted: boolean = false;
  let modalView: boolean = false;
  let scroll;

  const increaseCountNumber = () => {
    if (hasCounted) {
      return;
    }

    hasCounted = true;

    const oneHundredInterval = setInterval(() => {
      if (oneHundredValue >= 100) {
        clearInterval(oneHundredInterval);
      } else {
        oneHundredValue += 1;
      }
    }, 10);

    const fourHundredInterval = setInterval(() => {
      if (fourHundredValue >= 400) {
        clearInterval(fourHundredInterval);
      } else {
        fourHundredValue += 4;
      }
    }, 5 * (400 / 100));

    const twentyFiveHundredInterval = setInterval(() => {
      if (twentyFiveHundredValue >= 2500) {
        clearInterval(twentyFiveHundredInterval);
      } else {
        twentyFiveHundredValue += 25;
      }
    }, 1 * (2500 / 90));
  };

  const closeModal = () => {
    modalView = false;
  };

  $: {
    if (scroll > 2500) {
      increaseCountNumber();
    }
  }
</script>

<svelte:window bind:scrollY={scroll} />

<main class="w-[1234px] h-[950px] m-auto">
  <div class="flex items-center flex-col justify-center w-full h-full">
    <div class="w-[100px] h-[100px] text-green-600">
      <WiWindy />
    </div>
    <span class="text-[40px] font-medium w-[600px] text-center"
      >Receba as melhores dicas de nutrição para o dia-a-dia</span
    >
    <div
      class="w-full h-[550px] overflow-scroll overflow-y-hidden overflow-x-hidden mt-5 relative"
    >
      <img
        src="https://www.hcbh.org/media/rdynpnx4/nutrition.png"
        alt=""
        class="w-full h-full object-cover opacity-70 transition-all"
        class:scale-125={isHovering}
        class:opacity-forced={isHovering}
      />
      <div class="absolute inset-0 flex items-center justify-center">
        <button
          class="w-[100px] h-[100px] text-red-400 opacity-forced"
          on:mouseenter={() => (isHovering = true)}
          on:mouseleave={() => (isHovering = false)}
          on:click={() => (modalView = true)}
        >
          <FaPlay />
        </button>
      </div>
    </div>
    <div class="flex space-x-4 justify-center items-center mt-10">
      <div
        class="w-[290px] h-[210px] shadow-xl flex items-center justify-center flex-col"
      >
        <span class="text-5xl font-bold letter">{oneHundredValue}+</span>
        <span class="mt-4 font-medium text-lg">Anos de experiência</span>
      </div>
      <div
        class="w-[290px] h-[210px] shadow-xl flex items-center justify-center flex-col"
      >
        <span class="text-5xl font-bold letter">{twentyFiveHundredValue}+</span>
        <span class="mt-4 font-medium text-lg">Clientes felizes</span>
      </div>
      <div
        class="w-[290px] h-[210px] shadow-xl flex items-center justify-center flex-col"
      >
        <span class="text-5xl font-bold letter">{oneHundredValue}%</span>
        <span class="mt-4 font-medium text-lg">Satisfação</span>
      </div>
      <div
        class="w-[290px] h-[210px] shadow-xl flex items-center justify-center flex-col"
      >
        <span class="text-5xl font-bold letter">{fourHundredValue}+</span>
        <span class="mt-4 font-medium text-lg">Receitas saudáveis</span>
      </div>
    </div>
  </div>
</main>

{#if modalView}
  <Modal {closeModal} />
{/if}

<style>
  .opacity-forced {
    opacity: 100 !important;
  }
</style>
