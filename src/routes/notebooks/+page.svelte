<script lang="ts">
  import { page } from "$app/stores";
  import CopyButton from "$lib/CopyButton.svelte";
  import IconCopy from "$lib/icons/copy.svelte";

  const products = [
    {
      title: "(NT0022)LENOVO I7-4 - 8GB - SSD256",
      image: "i7_4_16.png",
      text: "💻 NOTEBOOK DELL\n\n*Processador:* i7 4ª GERAÇÃO\n*Memória RAM:* 8GB\n*Armazenamento:* SSD 256GB\n\nDE ~2.990,00~ *POR APENAS R$2.590,00* em até 10x sem juros!",
    },
    {
      title: "(NT0046)DELL I7-6 - 8GB - SSD256",
      image: "i7_8_256.png",
      text: "💻 NOTEBOOK DELL LATITUDE\n\n*Processador:* i7 6ª GERAÇÃO\n*Memória RAM:* 8GB\n*Armazenamento:* SSD 256GB\n\nDE ~R$3.390,00~ *POR APENAS R$2.890,00* em até 10x sem juros!",
    },
    {
      title: "(NT0039)LENOVO I7-8 - 8GB - NVME - 512GB",
      image: "i7_8_512.png",
      text: "💻 NOTEBOOK LENOVO THINKPAD\n\n*Processador:* i7 8ª GERAÇÃO\n*Memória RAM:* 8GB\n*Armazenamento:* NVME 512GB\n\nDE ~R$3.690,00~ *POR APENAS R$3.190,00* em até 10x sem juros!",
    },
    {
      title: "(NT0039) NOTEBOOK HP ZBOOK - XEON E-2176",
      image: "HPZBOOK.png",
      text: "💻 NOTEBOOK HP ZBOOK\n\n*Processador:* XEON E-2176\n*Memória RAM:* 16GB (DDR4)\n*Armazenamento:*SSD 256GB\n*Placa de Vídeo:* NVIDIA QUADRO P600 \n\nDE ~R$5.490,00~ *POR APENAS R$4.990,00* em até 10x sem juros!",
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
