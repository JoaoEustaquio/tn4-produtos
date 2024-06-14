<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";

  const products = [
    // R$ 1.790,00
    {
      title: "Nº1 Athlon 3000G",
      image: "AMD-2390.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n\n*Placa Mãe:* A520\n*Processador:* Athlon 3000G\n*Placa de Vídeo* VEGA 3 (INTEGRADA)\n*Memória RAM:* 2x8GB DDR4\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 1.890,00* em até 10x sem juros!",
    },

    // R$ 2.390,00
    {
      title: "Nº2 (PC0017) PC GAMER RYZEN 4600G",
      image: "(AMD)PC0017.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE (GRÁFICOS Médios/Baixos)\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 4FANS RGB \n*Fonte:* 500W\n\nPOR APENAS *R$ 2.390,00* em até 10x sem juros!",
    },

    // R$ 2.690,00
    {
      title: "Nº3 - (PC0001) GAMER RYZEN 5600G",
      image: "(AMD)PC0001.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 4FANS RGB \n*Fonte:* 500W\n\nDE ~R$ 2.990,00~ POR APENAS *R$ 2.690,00* em até 10x sem juros!",
    },

    // R$ 4.390,00
    {
      title: "Nº4 - RYZEN 5500 + RX 580 8GB",
      image: "AMD-4790.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  💥 FREE FIRE\n🌎 ARK SURVIVE\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5500\n*Placa Mãe:* B450 Challenger\n*Memória RAM:* 2x8GB DDR4 MANCER BANSHEE 2666Mhz\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER PCYES SET BLACK VULCAN\n*Fonte:* 500W\n\nPOR APENAS *R$ 4.390,00* em até 10x sem juros!",
    },

    // R$ 3.490,00
    {
      title: "Nº5 - RYZEN 4500 + RX 560",
      image: "AMD-3790.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A520\n*Memória RAM:* 2x8GB 2666Mhz DDR4 (16GB)\n*Placa de Vídeo:* RX 560 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/3FANS RGB\n*Fonte:* 500W\n\nPOR APENAS *R$ 3.490,00* em até 10x sem juros!",
    },

    // R$ 3.890,00
    {
      title: "Nº6 - RYZEN 4500 + RX 580 8GB",
      image: "AMD-3490.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* 💥 FREE FIRE \n 🌎 MINECRAFT \n 🟥 ROBLOX \n 🚔 GTA RP \n 🔫 CSGO/VALORANT \n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A520\n*Memória RAM:* 2x8GB MANCER 2666Mhz DDR4\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/3FANS RGB\n*Fonte:* 500W\n\nPOR APENAS *R$ 3.890,00* em até 10x sem juros!",
    },

    // R$ 4.590,00
    {
      title: "Nº7 - RYZEN 4500 + RTX 3050 6GB",
      image: "AMD-4590.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4 2666Hz\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 4FANS RGB \n*Fonte:* 500W\n\nPOR APENAS *R$ 4.590,00* em até 10x sem juros!",
    },

    // R$ 5.190,00
    {
      title: "Nº8 - (PC0003)RYZEN 5600 + RTX 3050",
      image: "(AMD)PC0003.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 4FANS RGB \n*Fonte:* 500W\n\nPOR APENAS *R$ 5.190,00* em até 10x sem juros!",
    },

    // R$ 6.390,00
    {
      title: "Nº9 - FULL WHITE RTX 3050 6GB",
      image: "AMD-5690.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n  💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* B550 DUEX\n*Memória RAM:* 2x8GB(16GB) DDR4 3200Mhz *BRANCA*\n*Water Cooler* Rise Mode Aura ICE RGBC 240MM C/ VISOR DE TEMPERATURA*\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS Controláveis\n*Fonte:* 500W *BRANCA*\n\nPOR APENAS *R$ 6.390,00* em até 10x sem juros!",
    },

    // R$ 6.690,00
    {
      title: "Nº10 - RYZEN 5600 + RTX 3060 12GB",
      image: "AMD-6690.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n🪓 God Of War\n🔫 Resident Evil 4 Remake\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* Biostar B450MX\n*Memória RAM:* 1x16GB DDR4 Fury Beast RGB 320Mhz\n*AIR Cooler* RGB\n*Placa de Vídeo:* RTX 3060 12GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER TGT C/ 3 FANS Controláveis\n*Fonte:* 550W 80PLUS\n\nPOR APENAS *R$ 6.690,00* em até 10x sem juros!",
    },

    // R$ 7.590,00
    {
      title: "Nº11 - RYZEN 5500 + RTX 4060 8GB",
      image: "AMD-8190.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n🪓 God Of War\n🔫 Resident Evil 4 Remake\n\n*Processador:* RYZEN 5 5500\n*Placa Mãe:*  B450 ASUS - 4 BANCOS MEMORIA\n*Memória RAM:* 2x8GB DDR4 REDRAGON  3200Mhz\n*WATER COOLER 240MM*\n*Placa de Vídeo:* RTX 4060 8GB\n*Armazenamento:* NVME 512GB\n*Gabinete:* GAMER NZXT 2 FANS BLACK\n*Fonte:* 700W 80PLUS\n\nPOR APENAS *R$ 7.590,00* em até 10x sem juros!",
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
