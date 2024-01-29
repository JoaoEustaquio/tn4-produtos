<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte"

  const products = [
    {
      title: "Athlon 3000G",
      image: "Athlon3000G.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n\n*Placa Mãe:* A520\n*Processador:* Athlon 3000G\n*Memória RAM:* 2x8GB(16GB) DDR4 2666Htz\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 1.890,00* em até 10x sem juros!",
    },
    {
      title: "(PC0017) PC GAMER RYZEN 4600G",
      image: "Ryzen4600G.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE (GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4 2666Htz\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 3 FANS RGB RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 2.390,00* em até 10x sem juros!"
    },
    {
      title: "(PC0001)GAMER RYZEN 5600G",
      image: "Ryzen5600G.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 3 FANS RGB RGB FRONTAIS\n*Fonte:* 500W\n\nDE ~R$ 2.990,00~ POR APENAS *R$ 2.690,00* em até 10x sem juros!"
    },
    {
      title: "SETUP COMPLETO Ryzen Athlon 3000G",
      image: "KitAthlon+RX550.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n 🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* ATHLON 3000G\n*Memória RAM:* 8GB DDR4 2666Htz\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ MONITOR 17' POLEGADAS *NOVO*, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.690,00* em até 10x sem juros!",
    },
    {
      title: "(PC0014)🖥🖱SETUP GAMER RYZEN 5 5600G",
      image: "SetupRyzen5600.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 3 FANS RGB RGB FRONTAIS\n*Fonte:* 500W\n+ Monitor de 17'' POL. 75Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 3.290,00* em até 10x sem juros!"
    },
    {
      title: "RYZEN 4500 + GTX 1650",
      image: "3600.1650.new.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A320\n*Memória RAM:* 2x8GB DDR4\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD 512GB\n*Gabinete:* GAMER HAYOM C/3 FANS RGB\n*Fonte:* 500W\n\nPOR APENAS *R$ 3.590,00* em até 10x sem juros!"
    },
    {
      title: "RYZEN 4500 + 16GB 2666 + GTX 1650S",
      image: "3600.GTX1660S.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4 2666Hz\n*Placa de Vídeo:* GTX 1660 SUPER 6GB\n*Armazenamento:* SSD 512GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 4.390,00* em até 10x sem juros!"
    },
    {
      title: "RYZEN 5600 + GTX 1660 Super",
      image: "5600G.GTX1650S.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* GTX 1660 SUPER 6GB\n*Armazenamento:* SSD 512GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 4.890,00* em até 10x sem juros!"
    },
    {
      title: "RYZEN 4500 + GTX 1660 SUPER",
      image: "4500.1660S.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 4500\n*Placa Mãe:* B550M Biostar\n*Memória RAM:* 1x16GB DDR4\n*Placa de Vídeo:* GTX 1660 Super 6GB\n*Armazenamento:* NVME 256GB\n*Gabinete* GAMER AQUÁRIO C/ 3 FANS\n*Fonte:* 500W\n\nPOR APENAS *R$ 5.090,00* em até 10x sem juros!"
    },
    {
      title: "RYZEN 5600 + RTX 3050",
      image: "5600G.RTX3050.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* A520\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* RTX 3050 8GB\n*Armazenamento:* SSD 512GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 500W\n\nPOR APENAS *R$ 5.090,00* em até 10x sem juros!"
    },
    {
      title: "(PC0006) RYZEN 5 5600 + RTX 3050",
      image: "Ryzen5.3050.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600\n*Placa Mãe:* B550\n*Memória RAM:* 2x8GB (16GB) DDR4\n*Placa de Vídeo:* RTX 3050 8GB\n*Armazenamento:* NVME 500GB\n*Gabinete:* GAMER C/ 3 FANS RGB FRONTAIS\n*Fonte:* 700W 80 PLUS\n\nPOR APENAS *R$ 5.890,00* em até 10x sem juros!"
    },
  ]

  function copyToClipboard(product: { text: string }) {
    navigator.clipboard.writeText(product.text)
  }
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <h1 class="text-xl font-bold mb-4">⚙️ MÁQUINAS PRONTAS</h1>
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
