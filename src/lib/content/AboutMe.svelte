<script lang="ts">
  import WiWindy from 'svelte-icons/wi/WiWindy.svelte';
</script>

<main class="w-[1234px] h-[700px] m-auto">
  <div class="flex justify-center items-center space-x-10 w-full h-full">
    <div class="w-[50%]">
      <img
        src="https://media.self.com/photos/57d8a54346d0cb351c8c56cd/4:3/w_2560%2Cc_limit/healthy-cooking-8701.jpg"
        alt="asd"
        class="w-full special-radius shadow-xl"
      />
    </div>
    <div class="w-[50%] h-[400px] flex flex-col">
      <div class="w-[90px] h-[90px] text-green-600">
        <WiWindy />
      </div>
      <span class="text-[44px] font-medium">Sobre mim</span>
      <span class="font-thin tracking-widest text-base mt-2"
        >Como nutricionista, minha paixão é ajudar meus pacientes a alcançar
        seus objetivos de saúde e bem-estar através de uma dieta equilibrada e
        personalizada. Com meu conhecimento em nutrição e hábitos alimentares
        saudáveis, eu trabalho com meus pacientes para desenvolver planos
        alimentares individualizados que atendam às suas necessidades
        específicas. Eu acredito que uma alimentação saudável não precisa ser
        complicada e é minha missão ajudar meus pacientes a descobrir o prazer
        de comer bem enquanto atingem suas metas de saúde e qualidade de vida.</span
      >
    </div>
  </div>
</main>

<style>
  .special-radius {
    border-radius: 100% 100% 50% 0% / 100% 100% 0% 0%;
  }
</style>
