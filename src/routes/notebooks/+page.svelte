<script lang="ts">
  import { page } from "$app/stores";
  import CopyButton from "$lib/CopyButton.svelte";
  import IconCopy from "$lib/icons/copy.svelte";

  const products = [
    {
      title:
        "(NT0055)LENOVO L450 | CORE I5-5300U - 8GB DDR4 - SSD 240GB - TELA 15",
      image: "i5_5300U.png",
      text: "💻 LENOVO L450 \n\n*Processador:* i5-5300U (5ª Geração)\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 240GB\n BATERIA *NOVA*\nAcompanha Fonte e Adaptador Mini DP P/ HDMI\n\nPOR APENAS *R$1.690,00* em até 10x sem juros!",
    },
    {
      title: "(NT0009)Dell Inspiron 15 - 8GB - SSD 256GB",
      image: "Inspiron15.png",
      text: "💻 NOTEBOOK DELL INSPIRON 15\n\n*Processador:* Intel I5-7200U (7ª Geração)\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD 256GB\n\n*POR APENAS R$2.490,00* em até 10x sem juros!",
    },
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
      title: "(NT0040)ACER NITRO RYZEN 5 - 8GB DDR5 - NVME 512GB - RTX 3050",
      image: "AcerNitro.png",
      text: "💻 Notebook Gamer Acer Nitro 5 (Novo na caixa)\n\n*Processador:* AMD Ryzen 5 7535HS 6 núcleos (12 threads)\n*Memória RAM:* 8GB DDR5 - Expansível até 32GB DDR5 de até 4800 MHz\n*Armazenamento:* NVME 512GB PCIe 4.0 x4 M.2 2280\n*Placa de Vídeo:*NVIDIA® GeForce® RTX 3050 com 4 GB de memória dedicada GDDR6 (TGP de 60W)\n🔈2x alto-falantes estéreo - DTS® X:Ultra Áudio e Acer TrueHarmony™\n⌨️ Teclado retro iluminado na cor vermelha\n\n*POR APENAS R$7.490,00* em até 10x sem juros!",
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
