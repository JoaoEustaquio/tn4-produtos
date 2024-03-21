<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte"

  const products = [
    {
      title: "(PC0013)i5 3ªSETUP COMPLETO R$1.690,00",
      image: "kit1690.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD 🎧 HEADSET\n\n*R$ 1.690,00* em até 10x sem juros!",
    },
    {
      title: "(PC0010)SETUP i5 3ª + RX 550 - R$2.290,00",
      image: "kit1690+RX550.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n 🚔 GTA RP(Gráficos Baixos)\n🔫 CSGO/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.290,00* em até 10x sem juros!",
    },
    {
      title: "(PC0010)SETUP i7 3ª + RX 550 - R$2.590,00",
      image: "kit1690+RX550.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n\n*Processador:* I7 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ Monitor 20' POL. *SEMINOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.690,00* em até 10x sem juros!",
    },
    {
      title: "(PC0014)🖥🖱SETUP GAMER RYZEN 5 4600G",
      image: "SetupRyzen5600.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ LED RGB FRONTAIS\n*Fonte:* 500W\n+ Monitor de 17' POL. 60Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 2.990,00* em até 10x sem juros!"
    },
    {
      title: "(PC0014)🖥🖱SETUP GAMER RYZEN 5 5600G",
      image: "SetupRyzen5600.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ LED RGB FRONTAIS\n*Fonte:* 500W\n+ Monitor de 17' POL. 60Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 3.290,00* em até 10x sem juros!"
    },
    {
      title: "🖱SETUP GAMER RYZEN 5 4500",
      image: "SetupRyzen5600.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4500\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER C/ 3 FANS RGB RGB FRONTAIS\n*Fonte:* 500W\n+ Monitor de 17' POL. *NOVO*\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 4.160,00* em até 10x sem juros!"
    },
    {
      title: "🖱SETUP GAMER RYZEN 5 4500",
      image: "4500.RX580.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE\n🦙 FORTNITE\n\n*Placa Mãe:* Duex B550\n*Processador:* RYZEN 5 4500\n*Memória RAM:* 2x8GB(16GB) DDR4 RISE MODE 3200Mhz\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 480GB\n*Gabinete:* GAMER Fortrek C/ 3 FANS RGB FRONTAIS Controláveis\n*Fonte:* 500W Branca\n+ Monitor de 27' POL. 165Gtz *BRANCO*\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 8.490,00* em até 10x sem juros!"
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
