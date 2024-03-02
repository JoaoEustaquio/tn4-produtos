<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";

  const products = [
    {
      title: "Nº1 - (PC0002)PC GAMER R$1.190,00",
      image: "i5-3.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB) DDR3\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 1.190,00* em até 10x sem juros!",
    },
    {
      title: "Nº2 - (PC0016)i5 3ª + RX 550 - R$1.790,00",
      image: "i5-3+RX550.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 FREE FIRE(Gráfico Baixo, SMART GAGA)\n🚔 GTA RP(Gráficos Baixos)\n🔫 CSGO/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I5 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 1.790,00* em até 10x sem juros!",
    },
    {
      title: "Nº3 - i7 de 3ª + RX 550  - R$2.190,00",
      image: "i7-3+RX550.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE(Gráficos Baixos)\n\n*Processador:* I7 de 3ª Geração\n*Placa Mãe:* H61 (LGA 1155)\n*Memória RAM:* 2x8GB(16GB)\n*Air Cooler* RGB\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER HAYOM C/ LED RGB\n*Fonte:* 500W\n\n*R$ 2.190,00* em até 10x sem juros!",
    },
    {
      title: "Nº4 - i3 de 8ª + GTX 1650 4GB",
      image: "i38.1650.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🚔 GTA RP(*Gráficos Médios)\n🔫 CSGO/VALORANT\n🦙 FORTNITE(*Gráficos Médios)\n\n*Processador:* I3 DE 8ªG\n*Placa Mãe:* H310 (LGA 1200)\n*Memória RAM:* 16GB DDR4 2666Htz\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD DE 512GB\n*Gabinete:* GAMER GAMER HAYOM C/3 FANS RGB + CONTROLADORA\n*Fonte:* 500W\n\n*R$ 3.330,00* em até 10x sem juros!",
    },
    {
      title: "Nº5 - i3 de 10ª + GTX 1650 4GB",
      image: "i312+1650.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I3 DE 10ªG\n*Placa Mãe:* H510PM (LGA 1200)\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* GTX 1650 4GB\n*Armazenamento:* SSD DE 480GB\n*Gabinete:* GAMER GAMER FORTREK C/3 FANS RGB\n*Fonte:* 500W\n\n*R$ 3.790,00* em até 10x sem juros!",
    },
    {
      title: "Nº6 - i5 de 12ª + RX 570 8GB",
      image: "I512+RX570.png",
      text: "💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🚔 GTA RP\n🔫 CSGO/VALORANT\n🦙 FORTNITE\n 🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Processador:* I5-12400F (12ª Geração)\n*Placa Mãe:* H610 (LGA 1700)\n*Memória RAM:* 16GB DDR4 3200Mhz FURY BEAST RGB\n*Placa de Vídeo:* RX 570 8GB\n*Armazenamento:* NVME 256GB\n*Gabinete:* GAMER HAYOM C/ 4 FANS RGB\n*Fonte:* 500W\n\n*R$ 4.790,00* em até 10x sem juros!",
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
