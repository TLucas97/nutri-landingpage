<script lang="ts">
  export let theme: string = 'blue';
  export let size: string = 'md';

  $: bg = {
    blue: 'bg-blue-500',
    red: 'bg-red-500',
    green: 'bg-green-500',
    black: 'bg-black',
  }[theme];

  $: sz = {
    sm: 'px-4 py-2 text-sm',
    md: 'px-6 py-3 text-base',
    lg: 'px-8 py-4 text-lg',
  }[size];
</script>

<button
  class={`text-white font-bold transition-all border-radius-change ${bg} ${sz} hover:bg-green-500`}
>
  <slot />
</button>

<style>
  .border-radius-change {
    border-radius: 0px 15px 0px 15px;
  }

  .border-radius-change:hover {
    border-radius: 15px;
  }
</style>
