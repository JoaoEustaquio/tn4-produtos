<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte"

  const products = [
    // R$1.690,00
    {
      title: "Nº1 - (PC0013)i5 3ªSETUP COMPLETO R$1.690,00",
      image: "PC0013.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 1x8GB(8GB)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 17' POL. , ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD 🎧 HEADSET\n\n*R$ 1.690,00* em até 10x sem juros!",
    },

    // R$2.290,00
    {
      title: "Nº2 - (PC0010)SETUP i5 3ª + RX 550 - R$2.290,00",
      image: "PC0010.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n 🚔 GTA RP(Gráficos Baixos)\n🔫 CSGO/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 1x8GB(8GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 17' POL. , ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.290,00* em até 10x sem juros!",
    },

    // R$2.390,00
    {
      title: "Nº3 - SETUP Athlon 3000G + Monitor 20 + KIT GAMER - R$2.390,00",
      image: "SETUP-2390.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 CSGO/VALORANT\n\n*Processador:* Athlon 3000G\n*Placa Mãe:* A320\n*Placa de Vídeo*: VEGA 3 (INTEGRADA)\n*Memória RAM:* 2x8GB DDR4 (16GB)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 17' POL. , ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.390,00* em até 10x sem juros!",
    },
    
    // R$2.590,00
    {
      title: "Nº4 - ()SETUP i7 3ª + RX 550 - R$2.590,00",
      image: "PC0010.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n\n*Processador:* I7 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 1x8GB(8GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 17' POL. , ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.690,00* em até 10x sem juros!",
    },

    // R$2.990,00
    {
      title: "Nº5 - (PC0031)🖥🖱SETUP GAMER RYZEN 5 4600G",
      image: "PC0031.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ LED RGB FRONTAIS\n*Fonte:* 500W\n+ 🖥️ Monitor de 17' POL. 60Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 2.990,00* em até 10x sem juros!"
    },

    // R$3.290,00
    {
      title: "Nº6 - (PC0014)🖥🖱SETUP GAMER RYZEN 5 5600G",
      image: "PC0014.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ LED RGB FRONTAIS\n*Fonte:* 500W\n+ 🖥️ Monitor de 17' POL. 60Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 3.290,00* em até 10x sem juros!"
    },

    // R$4.260,00
    {
      title: "Nº7 - (PC0004)🖱SETUP GAMER RYZEN 5 4500",
      image: "SETUP-4260.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4500\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB RGB FRONTAIS\n*Fonte:* 500W\n+ 🖥️ Monitor de 17' POL. *NOVO*\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 4.260,00* em até 10x sem juros!"
    },

    // R$ 5.290,00 Restore
    {
      title: "Nº8 - SETUP RYZEN 4500 + RTX 3050 6GB",
      image: "SETUP-5290.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4 2666Hz\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 500W\n +🖥 MONITOR (LC0042) 19' 75Hz Bluecase\n + KIT Gamer Completo(Teclado, Headset, Mouse e Mousepad)\n\nPOR APENAS *R$ 5.290,00* em até 10x sem juros!",
    },

    // R$7.990,00
    {
      title: "Nº8 - 🖱SETUP GAMER RYZEN 5 5600",
      image: "SETUP-7990.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🔫 CSGO 2\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* B450MX\n*Memória RAM:* 1x16GB DDR4 Fury Beast RGB\n*Placa de Vídeo:* RTX 3060 12GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 550W 80PLUS\n+ 🖥️ Monitor de 19' Pol. 75Htz\n+ + Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 7.990,00* em até 10x sem juros!",
    },

    // R$11.190,00
    {
      title: "Nº9 - 🖱SETUP GAMER RYZEN 5 4500",
      image: "SETUP-11190.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n 💥 FREE FIRE\n🌎 ARK SURVIVE\n🔫 GTA RP\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE\n🦙 FORTNITE\n\n*Placa Mãe:* Duex B550\n*Prcessador:* RYZEN 5 4500\n*Memória RAM:* 2x8GB(16GB) DDR4 RISE MODE 3200Mhz\n*Placa de Vídeo:* RTX 3050 6GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER Fortrek C/ 3 FANS RGB FRONTAIS Controláveis\n*Fonte:* 500W Branca\n+ 🖥️ Monitor de 27' POL. REDRAGON 180Gtz *BRANCO* PLANO & MONITOR 23,6'' BLUECASE CURVO 100Htz(Acompanha SUPORTE P/2 MONITOR EVOLUT)\n+ Kit Gamer(Teclado, Mouse e Headset)\nSUPORTE MESA C/LED HUB USB 3.0\n\nPOR APENAS *R$ 11.190,00* em até 10x sem juros!"
    },

    // R$11.490,00
    {
      title: "Nº10 - SETUP GAMER RYZEN 5 5500 COMPLETO",
      image: "SETUP-11490.png",
      text: "*UMA BASE DO QUE RODARIA NO COMPUTADOR:* \n🪓 God Of War\n🌎 ARK SURVIVE\n🟥 GTA RP\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5500\n*Placa Mãe:*  B450 ASUS - 4 BANCOS MEMORIA\n*Memória RAM:* 2x8GB DDR4 REDRAGON  3200Mhz\n*WATER COOLER 240MM*\n*Placa de Vídeo:* RTX 4060Ti 8GB INNO3D\n*Armazenamento:* NVME 512GB\n*Gabinete* GAMER NZXT 2 FANS BLACK\n*Fonte:* 700W 80PLUS\n\n+ 🖥️ Monitor REDRAGON 27' POL 165hz CURVO\n\n+*KIT GAMER:*\n- TECLADO REDRAGON FIZZ PRO 60% (COM KEYCAPS VERMELHAS)\n- MOUSE GAMER AOC AGM700\n- HEADSET REDRAGON MINOS BLACK\n- MICROFONE REDRAGON BLAZAR\n- MOUSEPAD FORTREK COURO\n\nPOR APENAS R$ 11.490,00 em até 10x sem juros!"
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
