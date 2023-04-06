<script lang="ts">
  import Button from '../Button.svelte';
  import WiWindy from 'svelte-icons/wi/WiWindy.svelte';
  import { fly } from 'svelte/transition';
  import PlanCards from './PlanCards.svelte';
</script>

<main class="w-[1234x] h-[700px] m-auto">
  <div class="flex items-center justify-center flex-col w-full h-full">
    <span class="text-[44px] font-medium">Planos disponíveis</span>
    <span class="w-[600px] text-center text-gray-600 tracking-widest mt-2"
      >Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
      ut aliquip ex ea commodo consequat aute irure dolor in reprehenderit.</span
    >
    <div class="mt-10 flex justify-center space-x-5 w-full">
      <PlanCards />
      <PlanCards />
      <PlanCards />
    </div>
  </div>
</main>
