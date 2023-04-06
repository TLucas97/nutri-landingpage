<script lang="ts">
  import WiWindy from 'svelte-icons/wi/WiWindy.svelte';
  import Button from '../Button.svelte';
</script>

<main class="w-[1234px] m-auto h-[900px]">
  <div class="flex justify-center items-center flex-col">
    <div class="w-[90px] h-[90px] text-green-600">
      <WiWindy />
    </div>
    <span class="text-[44px] font-medium">Me siga no Instagram!</span>
    <div class="w-full h-[600px] mt-5 flex space-x-8">
      <button class="w-[50%]">
        <img
          src="https://blog.unicep.edu.br/wp-content/uploads/2022/09/nutricionista-alimentacao-1647291298693_v2_1258x833.jpg"
          alt="asd"
          class="w-full h-full object-cover border-4 border-transparent hover:border-gray-300 transition ease-in-out"
        />
      </button>
      <div class="w-[50%] flex flex-col space-y-8">
        <div class="flex w-full h-[50%] space-x-8">
          <button class="w-[50%] h-full">
            <img
              src="https://blog.unicep.edu.br/wp-content/uploads/2022/09/nutricionista-alimentacao-1647291298693_v2_1258x833.jpg"
              alt="aaa"
              class="w-full h-full object-cover border-4 border-transparent hover:border-gray-300 transition ease-in-out"
            />
          </button>
          <button class="w-[50%] h-full">
            <img
              src="https://blog.unicep.edu.br/wp-content/uploads/2022/09/nutricionista-alimentacao-1647291298693_v2_1258x833.jpg"
              alt="aaa"
              class="w-full h-full object-cover border-4 border-transparent hover:border-gray-300 transition ease-in-out"
            />
          </button>
        </div>
        <div class="flex w-full h-[50%] space-x-8">
          <button class="w-[50%] h-full">
            <img
              src="https://blog.unicep.edu.br/wp-content/uploads/2022/09/nutricionista-alimentacao-1647291298693_v2_1258x833.jpg"
              alt="aaa"
              class="w-full h-full object-cover border-4 border-transparent hover:border-gray-300 transition ease-in-out"
            />
          </button>
          <button class="w-[50%] h-full">
            <img
              src="https://blog.unicep.edu.br/wp-content/uploads/2022/09/nutricionista-alimentacao-1647291298693_v2_1258x833.jpg"
              alt="aaa"
              class="w-full h-full object-cover border-4 border-transparent hover:border-gray-300 transition ease-in-out"
            />
          </button>
        </div>
      </div>
    </div>
    <div class="mt-10">
      <Button size="lg" theme="red">
        @nutriplus
      </Button>
    </div>
  </div>
</main>
