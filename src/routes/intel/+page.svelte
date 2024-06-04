<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";

  const products = [
    // R$1.190,00
    {
      title: "Nº1 - (PC0002)PC GAMER R$1.190,00",
      image: "PC0002.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 1x8GB(8GB) DDR3\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 1.190,00* em até 10x sem juros!",
    },

    // R$1.790,00
    {
      title: "Nº2 - (PC0016)i5 3ª + RX 550 - R$1.790,00",
      image: "PC0016.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n🚔 GTA RP(Gráficos Baixos)\n🚚 Euro Truck Simulator 2(Gráficos Baixos)\n🔫 CSGO(Gráfico Médio)/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 1x8GB(8GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 1.790,00* em até 10x sem juros!",
    },

    // R$2.190,00
    {
      title: "Nº3 - i7 de 3ª + RX 550  - R$2.190,00",
      image: "N3-Intel.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🚔 GTA RP\n🔫 CSGO(Gráfico Médio)/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I7 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 1x8GB(8GB)\n*Air Cooler* RGB\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 2.190,00* em até 10x sem juros!",
    },

    // R$4.590,00
    {
      title: "Nº4 - i5 de 12ª + RX 580 8GB",
      image: "N5-Intel.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I5-12400F (12ª Geração)\n*Placa Mãe:* H610 (LGA 1700)\n*Memória RAM:* 16GB DDR4 3200Mhz FURY BEAST RGB\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* NVME 256GB\n*Gabinete:* GAMER C/ 4 FANS RGB\n*Fonte:* 500W\n\n*R$ 4.590,00* em até 10x sem juros!",
    },

    // R$4.690,00
    {
      title: "Nº5 - i5 de 10ª + RX 580",
      image: "INTEL-4690.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I5-10400F (10ª Geração)\n*Placa Mãe:* B560-PRO MSI (LGA 1200)\n*Memória RAM:* 2x8GB DDR4 (16GB)\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER MANCER HEXER C/ 3FANS RGB\n*Fonte:* 500W\n\n*R$ 4.690,00* em até 10x sem juros!",
    },
    
    // R$4.990,00
    {
      title: "Nº6 - i3 de 13ª + RTX 3050 6GB",
      image: "N4-INTEL.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I3-13100F (13ª Geração)\n*Placa Mãe:* H610 (LGA 1700)\n*Memória RAM:* 2x8GB DDR4\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER PCYES BOLTER WHITE GHOST C/3 FANS\n*Fonte:* 500W\n\n*R$ 4.990,00* em até 10x sem juros!",
    },

    // R$8.890,00
    {
      title: "(PC0006)Nº7 - i5 de 12ª + RTX 4060 8GB ",
      image: "PC0006.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🚘FORZA HORIZON\n🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I5-12400F (12ª Geração)\n*Placa Mãe:*ASROCK B660M PHANTOM GAMING (LGA 1700)\n*Memória RAM:* 1x16GB DDR4 3200Mhz FURY BEAST RGB\n*WATER COOLER* PCYES VISION C/ DISPLAY LED PERSONALIZAVEL RGB\n*Placa de Vídeo*: RTX 4060 GALAX 8GB 1-CLICK 2X\n*Armazenamento:* SSD 512GB REDRAGON\n*Gabinete:* GAMER AQUÁRIO C/ 4 FANS RGB\n*Fonte:* 700W\n\n*R$ 8.890,00* em até 10x sem juros!",
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
