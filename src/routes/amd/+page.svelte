<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";

  const products = [
    // R$ 1.790,00
    {
      title: "Nº1 Athlon 3000G",
      image: "Athlon3000G.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n\n*Placa Mãe:* A320\n*Processador:* Athlon 3000G\n*Placa de Vídeo* VEGA 3 (INTEGRADA)\n*Memória RAM:* 8GB DDR4\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 1.790,00* em até 10x sem juros!",
    },
    // R$ 2.390,00
    {
      title: "Nº2 (PC0017) PC GAMER RYZEN 4600G",
      image: "Ryzen5600G.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE (GRÁFICOS Médios/Baixos)\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 3 FANS RGB RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 2.390,00* em até 10x sem juros!",
    },
    // R$ 2.690,00
    {
      title: "Nº3 - (PC0001) GAMER RYZEN 5600G",
      image: "Ryzen5600G.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ LED Fronta RGB\n*Fonte:* 500W\n\nDE ~R$ 2.990,00~ POR APENAS *R$ 2.690,00* em até 10x sem juros!",
    },
    // R$ 3.590,00
    {
      title: "Nº4 - (PC0025) RYZEN 4500 + GTX 1650",
      image: "4500+1650.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A520\n*Memória RAM:* 2x8GB DDR4\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER RGB\n*Fonte:* 500W\n\nPOR APENAS *R$ 3.590,00* em até 10x sem juros!",
    },
    // R$ 4.190,00
    {
      title: "Nº5 - RYZEN 4500 + RX 580",
      image: "4500-RX580.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4 2666Hz\n*Placa de Vídeo:* RX 580 8GB ASROCK\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 4.190,00* em até 10x sem juros!",
    },
    // R$ 4.690,00
    {
      title: "Nº6 - RYZEN 5600 + RX 580",
      image: "5600G.GTX1650S.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 \n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 4.690,00* em até 10x sem juros!",
    },
    // R$ 5.090,00
    {
      title: "Nº7 - RYZEN 5600 + RTX 3050",
      image: "5600G.RTX3050.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 5.090,00* em até 10x sem juros!",
    },
    // R$ 5.290,00
    {
      title: "Nº8 - RYZEN 4500 + RTX 4060 8GB 2X",
      image: "4500.1660S.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* B550M Biostar\n*Memória RAM:* 1x16GB DDR4 Fury Beast Black\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* NVME 256GB\n*Gabinete* GAMER AQUÁRIO C/ 3 FANS\n*Fonte:* 500W\n\nPOR APENAS *R$ 5.290,00* em até 10x sem juros!",
    },
    // R$ 5.990,00
    {
      title: "Nº9 - RYZEN 4500 + RX 580 WHITE",  
      image: "4500+RX580.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* B550 DUEX\n*Memória RAM:* 2X8GB DDR4 RISE MODE 320Mhz\n*Water Cooler* Rise Mode Aura ICE RGB C/ VISOR LCD PERSONALIZAVEL*\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER Fortrek Cruiser C/ 3 FANS Controláveis\n*Fonte:* 500W *BRANCA*\n\nPOR APENAS *R$ 5.990,00* em até 10x sem juros!",
    },
  ];

  function copyToClipboard(product: { text: string }) {
    navigator.clipboard.writeText(product.text);
  }
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <h1 class="text-xl font-bold mb-4">⚙️ MÁQUINAS PRONTAS (PC)</h1>
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
