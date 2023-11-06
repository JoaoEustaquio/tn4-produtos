<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte"

  const products = [
    {
      title: "(PC0001)GAMER RYZEN 5 5600G",
      image: "maquina_ryzen_5.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 4 FANS RGB NA FRENTE\n*Fonte:* 500W\n\nDE ~R$ 2.990,00~ POR APENAS *R$ 2.690,00* em até 10x sem juros!"
    },
    {
      title: "(PC0002)PC GAMER R$1.190,00",
      image: "gabinete1690.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n\n*Processador:* I5-3550 3.20GHz\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER TGT C/DUAS FANS\n*Fonte:* 500W\n\n*R$ 1.190,00* em até 10x sem juros!",
    },
    // {
    //   title: "PC GAMER 1.190 (Gabinete Hayom)",
    //   image: "gabinete1990_v2.png",
    //   text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n\n*Processador:* I5-3550 3.20GHz\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER HAYOM com LED FRONTAL *CONTROLAVEL*\n*Fonte:* 500W\n\n*R$ 1.290,00* em até 10x sem juros!",
    // },
    {
      title: "🖥🖱SETUP GAMER RYZEN 5 5600G",
      image: "maquina_ryzen_5.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 WARZONE\n🦙 FORTNITE\n\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 4 FANS RGB NA FRENTE\n*Fonte:* 500W\n+ Monitor de 17'' POL. 75Htz\n+ Kit Gamer(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 3.290,00* em até 10x sem juros!"
    },
    {
      title: "I5 de 3ª + 16GB + RX 550",
      image: "gabinete1990.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🚔 GTA RP\n🔫 CSGO/VALORANT\n\n*Processador:* I5-3550 3.20GHz\n*Memória RAM:* 2x8GB(16GB) DDR3\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER TGT C/DUAS FANS\n*Fonte:* 500W\n\n*R$ 1.940,00* em até 10x sem juros!",
    },
    {
      title: "PC GAMER + RX 550 (1790)",
      image: "gabinete1990.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🚔 GTA RP\n🔫 CSGO/VALORANT\n\n*Processador:* I5-3550 3.20GHz\n*Memória RAM:* 8GB DDR3\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER TGT C/DUAS FANS\n*Fonte:* 500W\n\n*R$ 1.790,00* em até 10x sem juros!",
    },
    {
      title: "SETUP COMPLETO 1690",
      image: "kit1690.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n\n*Processador:* I5-3550 3.20GHz\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER TGT C/DUAS FANS\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ MONITOR SEMINOVO 19' POLEGADAS, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD 🎧 HEADSET\n\n*R$ 1.690,00* em até 10x sem juros!",
    },
    {
      title: "SETUP COMPLETO 1690 + RX 550",
      image: "kit1690.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n 🚔 GTA RP\n🔫 CSGO/VALORANT\n\n*Processador:* I5-3550 3.20GHz\n*Memória RAM:* 8GB DDR3\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER TGT C/DUAS FANS\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ MONITOR SEMINOVO 19' POLEGADAS, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.290,00* em até 10x sem juros!",
    },
    {
      title: "GAMER I7 3 GERAÇÃO",
      image: "gabinete1990.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🔫 VALORANT (50/70FPS)\n\n*Processador:* i7 3ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER TGT C/DUAS FANS\n*Fonte:* 500W\n\n*R$ 1.490,00* em até 10x sem juros!",
    },
    {
      title: "GAMER I7 3 GERAÇÃO + R5 230 2GB",
      image: "gabinete1990.png",
      text: "💥 LEAGUE OF LEGENDS\n🚔 GTA RP\n🌎 MINECRAFT\n🔫 VALORANT\n\n*Processador:* i7 3ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Placa de Vídeo:* R5 230 2GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER TGT C/DUAS FANS\n*Fonte:* 500W\n\n*R$ 1.990,00* em até 10x sem juros!",
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
