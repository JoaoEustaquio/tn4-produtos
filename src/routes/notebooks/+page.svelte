<script lang="ts">
  import { page } from "$app/stores";
  import CopyButton from "$lib/CopyButton.svelte";
  import IconCopy from "$lib/icons/copy.svelte";

  const products = [
    // R$0.000,00
    // {
    //   title: "(CODE)NOTEBOOK ",
    //   image: ".png",
    //   text: "💻 NOTEBOOK ...\n\n*Processador:* \n*Memória RAM:* \n*Armazenamento:*\n(Acompanha Fonte)\n\n*POR APENAS R$0.000,00* em até 10x sem juros!",
    // },

    // R$1.190,00
    {
      title: "Nº1 - (NT0062)POSITIVO MASTER N190I",
      image: "POSITIVO-I33110M.png",
      text: "💻 NOTEBOOK POSITIVO MASTER N190I\n\n*Processador:* i3-3110M (3ª GERAÇÃO)\n*Memória RAM:* 8GB\n*Armazenamento:* SSD 120GB\n*ACOMPANHA FONTE*\n*BATERIA NOVA*\n\n*POR APENAS R$1.190,00* em até 10x sem juros!",
    },

    // R$1.490,00
    {
      title: "Nº2 - (NT0002)NOTEBOOK LENOVO THINKPAD",
      image: "LENOVO-thinkpad_i5-5.png",
      text: "💻 NOTEBOOK LENOVO THINKPAD\n\n*Processador:*i5 4ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Armazenamento:*SSD 240GB\n(Acompanha Fonte)\n\n*POR APENAS R$1.490,00* em até 10x sem juros!",
    },

    // R$1.590,00
    {
      title: "Nº3 - (NT0118)NOTEBOOK LENOVO B40-70",
      image: "LENOVO-B40-70_i5-4.png",
      text: "💻 NOTEBOOK LENOVO B40-70\n\n*Processador:*i5 5ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 240GB\n(Acompanha Fonte)\n\n*POR APENAS R$1.590,00* em até 10x sem juros!",
    },

    // R$1.890,00
    {
      title: "Nº4 - (NT0067)NOTEBOOK HP CORE 240 G6",
      image: "HP-CORE-240_I5-7.png",
      text: "💻 NOTEBOOK HP CORE 240 G6\n\n*Processador:* I5-7200U (7ª Geração)\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD de 240GB\n(Acompanha Fonte)\n\n*POR APENAS R$1.890,00* em até 10x sem juros!",
    },

    // R$2.590,00
    {
      title: "Nº5 - (NT0022)LENOVO I7-4",
      image: "i7_4_16.png",
      text: "💻 NOTEBOOK DELL\n\n*Processador:* i7 4ª GERAÇÃO\n*Memória RAM:* 8GB\n*Armazenamento:* SSD 256GB\n\nDE ~2.990,00~ *POR APENAS R$2.590,00* em até 10x sem juros!",
    },

    // R$2.890,00
    {
      title: "Nº6 - (NT0046)DELL I7-6 - 8GB - SSD256",
      image: "i7_8_256.png",
      text: "💻 NOTEBOOK DELL LATITUDE\n\n*Processador:* i7 6ª GERAÇÃO\n*Memória RAM:* 8GB\n*Armazenamento:* SSD 256GB\n\nDE ~R$3.390,00~ *POR APENAS R$2.890,00* em até 10x sem juros!",
    },

    // R$3.290,00
    {
      title: "Nº7 - (NT0064)NOTEBOOK LENOVO IDEAPAD ",
      image: "LENOVO-ideapad_I7-8.png",
      text: "💻 NOTEBOOK LENOVO IDEAPAD\n\n*Processador:* i7 8ª GERAÇÃO\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD 240GB\n(Acompanha Fonte)\n\n*POR APENAS R$3.290,00* em até 10x sem juros!",
    },

    // R$3.390,00
    {
      title: "Nº8 - (NT0068)NOTEBOOK THINKPAD E490",
      image: "THINKPAD-E490_i7-8.png",
      text: "💻 NOTEBOOK THINKPAD E490\n\n*Processador:* i7-8565U (8ª Geração)\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD 240GB\n*Placa de Vídeo*: RX 550X 2GB\n(Acompanha Fonte)\n\n*POR APENAS R$3.390,00* em até 10x sem juros!",
    },

    // R$3.490,00
    {
      title: "Nº9 - (NT0065)NOTEBOOK THINKPAD E14",
      image: "THINKPAD-E14_i5-10.png",
      text: "💻 NOTEBOOK THINKPAD E14\n\n*Processador:* I5-10210U (10ª Geração)\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD 240GB\n(Acompanha Fonte)\n\n*POR APENAS R$3.490,00* em até 10x sem juros!",
    },
  ];

  function copyToClipboard(product: { text: string }) {
    navigator.clipboard.writeText(product.text);
  }
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <h1 class="text-xl font-bold mb-4">💻 Notebooks</h1>
  <div class="grid grid-cols-4 gap-8">
    {#each products as product}
      <div class="space-y-4">
        <img
          src={product.image}
          class="rounded-md w-full h-64 object-contain border border-gray-200 bg-gray-50"
          alt={product.title}
        />
        <h1 class="font-bold text-xl truncate">{product.title}</h1>
        <code
          class="font-mono-emoji block w-full h-64 overflow-y-scroll whitespace-pre-line bg-gray-100 border border-gray-300 p-2 rounded"
        >
          {product.text}
        </code>

        <CopyButton
          class="w-full tracking-wider text-sm"
          on:click={() => copyToClipboard(product)}>COPIAR</CopyButton
        >
      </div>
    {/each}
  </div>
</div>
