<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte"

  const products = [
    // R$3.440,00
    {
      title: "Nº1 - () SETUP GAMER PINK - RYZE 4600G",
      image: "Pink.png",
      text: "*Setup ideal para Jogos como:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 1FAN RGB\n*Fonte:* 500W\n+ 🖥️ Monitor de 21,5' Pol.\n+ Kit Gamer Rosa(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 3.890,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳Cartão - Débito á vista ou Crédito em até *10x SEM JUROS*\n❖ Pix á Vista\n❌*NÃO* é possível realizar pagamento via Boleto Bancário"
    },

    // R$4.190,00
    {
      title: "Nº2 - () SETUP KIDS - RYZEN 5600G",
      image: "BRANCOALA.png",
      text: "*Setup ideal para Jogos como:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE (GRÁFICOS Médio/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:*  VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 4FANS RGB\n*Fonte:* 500W\n+ 🖥️ Monitor de 21,5' Pol.\n+ Kit Gamer (Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 4.190,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳Cartão - Débito á vista ou Crédito em até *10x SEM JUROS*\n❖ Pix á Vista\n❌*NÃO* é possível realizar pagamento via Boleto Bancário"
    },
  ]

  function copyToClipboard(product: { text: string }) {
    navigator.clipboard.writeText(product.text)
  }
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <span> | </span>
  <a href="/intel">PC</a>
  <h1 class="text-xl font-bold mb-4">⚙️ MÁQUINAS PRONTAS (SETUP)</h1>
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
