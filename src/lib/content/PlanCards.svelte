<script lang="ts">
  import MdCheck from 'svelte-icons/md/MdCheck.svelte';
</script>

<div class="w-[300px] h-[500px] flex flex-col justify-between">
  <div
    class="h-[60%] bg-[url('https://www.fredhutch.org/content/dam/www/research/divisions/public-health-sciences/nutrition-assessment/nutrition-dietary-data-gfb-2.jpg')] p-10 flex items-center justify-center"
  >
    <div
      class="bg-green-100 w-full h-full shadow-lg opacity-80 flex items-center justify-center rounded-xl"
    >
      <span class="font-extrabold text-3xl text-center">PLANO BÁSICO</span>
    </div>
  </div>
  <div class="h-[40%] shadow-xl flex flex-col justify-center items-center">
    <div
      class="h-[30%] border-b w-full flex items-center justify-center font-medium text-lg"
    >
      Plano básico
    </div>
    <div class="h-[70%] w-full flex flex-col items-center justify-center">
      <div class="h-[40%] flex items-center justify-center">
        <span class="text-sm text-gray-600 text-center"
          >Ut enim ad minim veniam, quis ostrudes citation ullamco laboris nisi
          ut.</span
        >
      </div>
      <div class="h-[60%] w-full p-1 flex flex-col justify-between">
        <div class="h-full w-full flex justify-center items-center">
          <div class="w-[50%] flex justify-center items-center">
            <div class="flex space-x-2 items-center">
              <div class="w-[20px] h-[20px]">
                <MdCheck />
              </div>
              <span>Item 1</span>
            </div>
          </div>
          <div class="w-[50%] flex justify-center items-center">
            <div class="flex space-x-2 items-center">
              <div class="w-[20px] h-[20px]">
                <MdCheck />
              </div>
              <span>Item 1</span>
            </div>
          </div>
        </div>
        <div class="h-full w-full flex justify-center items-center">
          <div class="w-[50%] flex justify-center items-center">
            <div class="flex space-x-2 items-center">
              <div class="w-[20px] h-[20px]">
                <MdCheck />
              </div>
              <span>Item 1</span>
            </div>
          </div>
          <div class="w-[50%] flex justify-center items-center">
            <div class="flex space-x-2 items-center">
              <div class="w-[20px] h-[20px]">
                <MdCheck />
              </div>
              <span>Item 1</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
