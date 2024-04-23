<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte"

  const products = [
    // R$1.690,00
    {
      title: "Nº1 - (PC0013)i5 3ªSETUP COMPLETO R$1.690,00",
      image: "PC0013.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD 🎧 HEADSET\n\n*R$ 1.690,00* em até 10x sem juros!",
    },

    // R$2.290,00
    {
      title: "Nº2 - (PC0010)SETUP i5 3ª + RX 550 - R$2.290,00",
      image: "PC0010.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n 🚔 GTA RP(Gráficos Baixos)\n🔫 CSGO/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.290,00* em até 10x sem juros!",
    },

    // R$2.290,00
    {
      title: "Nº3 - (PC0010)SETUP i5 3ª + RX 550 - R$2.290,00",
      image: "PC0010.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n 🚔 GTA RP(Gráficos Baixos)\n🔫 CSGO/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.290,00* em até 10x sem juros!",
    },

    // R$2.390,00
    {
      title: "Nº4 - SETUP Athlon 3000G + Monitor 20 + KIT GAMER - R$2.390,00",
      image: "N4-SETUP.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 CSGO/VALORANT\n\n*Processador:* Athlon 3000G\n*Placa Mãe:* A320\n*Placa de Vídeo*: VEGA 3 (INTEGRADA)\n*Memória RAM:* 2x8GB DDR4 (16GB)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.390,00* em até 10x sem juros!",
    },
    
    // R$2.590,00
    {
      title: "Nº5 - (PC0010)SETUP i7 3ª + RX 550 - R$2.590,00",
      image: "PC0010.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n\n*Processador:* I7 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.690,00* em até 10x sem juros!",
    },

    // R$2.990,00
    {
      title: "Nº6 - (PC0014)🖥🖱SETUP GAMER RYZEN 5 4600G",
      image: "PC0014.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ LED RGB FRONTAIS\n*Fonte:* 500W\n+ Monitor de 17' POL. 60Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 2.990,00* em até 10x sem juros!"
    },

    // R$3.290,00
    {
      title: "Nº7 - (PC0014)🖥🖱SETUP GAMER RYZEN 5 5600G",
      image: "PC0014.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ LED RGB FRONTAIS\n*Fonte:* 500W\n+ Monitor de 17' POL. 60Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 3.290,00* em até 10x sem juros!"
    },

    // R$4.260,00
    {
      title: "Nº8 - (PC0004)🖱SETUP GAMER RYZEN 5 4500",
      image: "N8-SETUP.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4500\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB RGB FRONTAIS\n*Fonte:* 500W\n+ Monitor de 17' POL. *NOVO*\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 4.260,00* em até 10x sem juros!"
    },

    // R$7.390,00
    {
      title: "Nº9 - 🖱SETUP GAMER RYZEN 5 5600",
      image: "N9-SETUP.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* B450MX\n*Memória RAM:* 1x16GB DDR4 Fury Beast RGB\n*Placa de Vídeo:* RTX 3060 12GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 550W 80PLUS\n+ Monitor de 19' Pol. 75Htz\n+ + Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 7.390,00* em até 10x sem juros!",
    },

    // R$8.190,00
    {
      title: "Nº10 - 🖱SETUP GAMER RYZEN 5 4500",
      image: "N10-SETUP.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE\n🦙 FORTNITE\n\n*Placa Mãe:* Duex B550\n*Processador:* RYZEN 5 4500\n*Memória RAM:* 2x8GB(16GB) DDR4 RISE MODE 3200Mhz\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER Fortrek C/ 3 FANS RGB FRONTAIS Controláveis\n*Fonte:* 500W Branca\n+ Monitor de 27' POL. 165Gtz *BRANCO*\n+ Kit Gamer(Teclado, Mouse e Headset)\n\nPOR APENAS *R$ 8.190,00* em até 10x sem juros!"
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
