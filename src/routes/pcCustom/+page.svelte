<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";

  const products = [
    // R$ 4.990,00
    {
      title: "Nº1 - Ryzen 4500 + RX 580 ",
      image: "AMD-N7.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🚔 GTA 5/RP\n🔫 CSGO 2\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* B450MHP\n*Memória RAM:* 2x8GB (16GB) DDR4 Redragon Solar RGB 3200MHZ\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* BRX HAVOC\n*Fonte:* 500W 80Plus RGB\n\nPOR APENAS *R$ 4.990,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳Cartão - Débito á vista ou Crédito em até *10x SEM JUROS*\n❖ Pix á Vista\n❌*NÃO* é possível realizar pagamento via Boleto Bancário",
    },

    // R$5.790,00
    {
      title: "Nº2 - I5 DE 10ª + RTX 3050 + GABINETE STORM-Z",
      image: "SETUP - N10.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I5-10400F (10ª Geração)\n*Placa Mãe:* B560-PRO MSI (LGA 1200)\n*Memória RAM:* 2x8GB DDR4 FURY BEAST 3200MHZ (16GB)\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* STORM-Z SHARP\n*Fonte:* 500W PFV ATIVO\n\n*R$ 5.790,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳Cartão - Débito á vista ou Crédito em até *10x SEM JUROS*\n❖ Pix á Vista\n❌*NÃO* é possível realizar pagamento via Boleto Bancário",
    },

    // R$ 5.990,00
    {
      title: "Nº3 - RYZEN 3700X + RX 580",
      image: "AMD-5990.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n💥 GTA RP\n🌎 MINECRAFT\n🔫 VALORANT\n🔫 WARZONE\n🚔 GTA 5/RP\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 7 3700X\n*Placa Mãe:* DUEX B550ZG WHITE\n*Memória RAM:* 2x8GB 3200MHZ White RGB DDR4(16GB)\n*Placa de Vídeo:* RX 580 8GB\n*Water Cooler*: GAMDIAS AURA GL120 White\n*Armazenamento:* SSD M.2 512GB\n*Gabinete:* PCYES BOLTER WHITE GHOST\n*Fonte:* 500W *WHITE*\n\nPOR APENAS *R$ 5.990,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳Cartão - Débito á vista ou Crédito em até *10x SEM JUROS*\n❖ Pix á Vista\n❌*NÃO* é possível realizar pagamento via Boleto Bancário",
    },

    // R$ 8.490,00
    {
      title: "Nº4 - Ryzen 5700X + RTX 4060 ",
      image: "RYZEN5700X.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n🪓 God Of War\n🚔 GTA 5/RP\n🔫 Resident Evil 4 Remake\n\n*Processador:* RYZEN 7 5700X\n*Placa Mãe:*  B450M STEEL LEGEND\n*Memória RAM:* 2x8GB DDR4 3200Mhz\n*WATER COOLER GAMDIAS AURA 240MM*\n*Placa de Vídeo:* RTX 4060 8GB\n*Armazenamento:* NVME 512GB\n*Gabinete:* GAMER PCYES FORCEFIELD BLACK VULCAN *C/6 FANS*\n*Fonte:* 600W 80PLUS\n\nPOR APENAS *R$ 8.490,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳Cartão - Débito á vista ou Crédito em até *10x SEM JUROS*\n❖ Pix á Vista\n❌*NÃO* é possível realizar pagamento via Boleto Bancário",
    },

    // R$8.890,00
    {
      title: "Nº5 - (PC0006)i5 de 12ª + RTX 4060 8GB ",
      image: "PC0006.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🚘FORZA HORIZON\n🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I5-12400F (12ª Geração)\n*Placa Mãe:*ASROCK B660M PHANTOM GAMING (LGA 1700)\n*Memória RAM:* 1x16GB DDR4 3200Mhz FURY BEAST RGB\n*AIR COOLER* GAMDIAS BOREAS E1 RGB\n*Placa de Vídeo*: RTX 4060 GALAX 8GB 1-CLICK 2X\n*Armazenamento:* SSD 512GB REDRAGON\n*Gabinete:* GAMER AQUÁRIO C/ 4 FANS RGB\n*Fonte:* 700W\n\n*R$ 7.590,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳Cartão - Débito á vista ou Crédito em até *10x SEM JUROS*\n❖ Pix á Vista\n❌*NÃO* é possível realizar pagamento via Boleto Bancário",
    },
  ];

  function copyToClipboard(product: { text: string }) {
    navigator.clipboard.writeText(product.text);
  }
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <span> | </span>
  <a href="/intel">PC</a>
  <h1 class="text-xl font-bold mb-4">🖌 PCs Personalizados</h1>
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
