<script lang="ts">
  import FaFacebook from 'svelte-icons/fa/FaFacebook.svelte';
  import FaWhatsapp from 'svelte-icons/fa/FaWhatsapp.svelte';
  import FaInstagram from 'svelte-icons/fa/FaInstagram.svelte';
  import IoMdMail from 'svelte-icons/io/IoMdMail.svelte';
  import Button from './Button.svelte';
</script>

<main class="w-full bg-[#97deff15]">
  <div class="w-[1234px] h-[550px] m-auto">
    <div class="flex justify-center items-center w-full h-full">
      <div class="w-[50%] h-full flex items-center justify-center flex-col">
        <div class="flex space-x-2 items-end">
          <img src="./images/apple.png" alt="asd" class="w-[44px] h-[44px]" />
          <span class="font-bold text-[24px]">Flavia Nutri</span>
        </div>
        <span class="w-[400px] text-center text-gray-600 mt-3"
          >Lorem ipsum dolor sit amet consectetur dolol drakgonil adipiscing
          elit aliquam mauris.</span
        >
        <span class="mt-10 font-bold text-xl">Redes sociais</span>
        <div class="mt-5 flex space-x-4">
          <button
            class="w-[35px] h-[35px] flex items-center justify-center hover:text-blue-600"
          >
            <FaFacebook />
          </button>
          <button
            class="w-[35px] h-[35px] flex items-center justify-center hover:text-green-600"
          >
            <FaWhatsapp />
          </button>
          <button
            class="w-[35px] h-[35px] flex items-center justify-center hover:text-red-600"
          >
            <FaInstagram />
          </button>
        </div>
      </div>
      <div class="w-[50%] h-full flex items-center justify-center flex-col">
        <div class="w-[50%] h-[85%] bg-red-100 rounded-lg flex flex-col">
          <div class="h-[50%] flex items-center justify-center">
            <div class="w-[90%] border h-[70%] px-4 flex flex-col">
              <div class="w-[45px]">
                <IoMdMail />
              </div>
              <span class="font-semibold text-lg mt-3">Contato por e-mail</span>
              <span class="font-normal text-start text-sm mt-2"
                >Me envie um email se quiser saber mais detalhes sobre os planos
                ou qualquer outra dúvida!</span
              >
            </div>
          </div>
          <div class="h-[50%] flex items-center justify-center">
            <div class="flex items-center justify-center flex-col space-y-3 w-[90%] max-h-[200px] px-4">
              <input
                type="text"
                placeholder="Seu email ou número"
                class="w-full p-3 focus:outline-none"
              />
              <textarea placeholder="Sua mensagem" class="w-full p-3 focus:outline-none" />
              <div>
                <Button>ENVIAR</Button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</main>
