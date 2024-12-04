<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";

  const products = [
    // R$ 499,00
    {
      title: "Nº1 - (DT0006E)HP ELITEDESK 705",
      image: "DT0006E.png",
      text: "*Placa Mãe:* \n*Processador:* AMD A4\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 120GB\n*Fonte:* 200w 80Plus Gold\nDe ~R$790,00~ Por apenas *R$499,00*em até 10x sem juros!",
    },

    // R$ 970,00
    {
      title: "Nº2 - (DT0007)Lenovo Thinkcentre S510",
      image: "DT0007.png",
      text: "*Placa Mãe:* \n*Processador:* Intel i5 de 7ª Geração\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD 240GB\nPor apenas *R$1.190,00*em até 10x sem juros!",
    },

    // R$ 1.790,00
    {
      title: "Nº3 - (DT0087)Lenovo Thinkcentre M910",
      image: "DT0087.png",
      text: "*Placa Mãe:* \n*Processador:* Intel i7 de i6ª Geração\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD 240GB\n*Fonte:* 200w 80PLUS Platinum\n\nDe ~R$1.990,00~ Por apenas *R$1.690,00*em até 10x sem juros!",
    },
  ];

  function copyToClipboard(product: { text: string }) {
    navigator.clipboard.writeText(product.text);
  }
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <h1 class="text-xl font-bold mb-4">⚙️ Desktop Office</h1>
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
