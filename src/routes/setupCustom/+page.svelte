<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte"

  const products = [
    // R$3.890,00
    {
      title: "Nº1 - () SETUP GAMER PINK - RYZE 4600G",
      image: "Pink.png",
      text: "*Setup ideal para Jogos como:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE(GRÁFICOS Médios/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 4600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 1FAN RGB\n*Fonte:* 500W\n+ 🖥️ Monitor de 21,5' Pol.\n+ Kit Gamer Rosa(Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 3.890,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳 Cartão - Débito à vista ou Crédito em até 10x *SEM JUROS*\n❖ Pix á Vista\n❌ NÃO aceitamos pagamento via boleto bancário\n❌ NÃO geramos link de pagamento \n\n🔥 Não perca essa chance de melhorar seu setup e jogar com qualidade! 🔥\n\n"
    },

    // R$4.190,00
    {
      title: "Nº2 - () SETUP KIDS - RYZEN 5600G",
      image: "BRANCOALA.png",
      text: "*Setup ideal para Jogos como:* \n 💥 LEAGUE OF LEGENDS\n🌎 MINECRAFT\n🟥 ROBLOX\n🔫 VALORANT\n🔫 CSGO 2\n🔫 WARZONE (GRÁFICOS Médio/Baixos)\n🦙 FORTNITE\n\n*Placa Mãe:* A520\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 2x8GB(16GB) DDR4\n*Placa de Vídeo:*  VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 240GB\n*Gabinete:* GAMER C/ 4FANS RGB\n*Fonte:* 500W\n+ 🖥️ Monitor de 21,5' Pol.\n+ Kit Gamer (Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 4.190,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳 Cartão - Débito à vista ou Crédito em até 10x *SEM JUROS*\n❖ Pix á Vista\n❌ NÃO aceitamos pagamento via boleto bancário\n❌ NÃO geramos link de pagamento \n\n🔥 Não perca essa chance de melhorar seu setup e jogar com qualidade! 🔥\n\n"
    },

    // R$8.090,00
    {
      title: "Nº3 - (PC0047) SETUP WHITE Ryzen 5600 + RTX 3050 GALAX 6GB",
      image: "WHITE.png",
      text: "*Setup ideal para Jogos como:*\n🚘FORZA HORIZON\n🚔 GTA 5/RP\n🔫 WARZONE/BLACK OPS 6\n🦙 FORTNITE\n🐎Red Dead Redemption 2\n\n*Placa Mãe:* DUEX B550ZGS\n*Processador:* RYZEN 5 5600\n*Memória RAM:* 2x8GB DDR4 3200Mhz PCYES UDIMM BRANCA\n*Placa de Vídeo:* RTX 3050 GALAX 6GB\n*Armazenamento:* SSD 240GB\n *Water Cooler:* PCYES SANGE FRIO3 BRANCO 120mm\n*Gabinete:* PCYES FORCEFIELD WHITE GHOST C/ 8FANS RGB\n*Fonte:* 500W BRANCA\n+ 🖥️ Monitor de 19' Pol. BRANCO\n+ Kit Gamer (Teclado, Mouse, Mousepad e Headset)\n\nPOR APENAS *R$ 8.090,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳 Cartão - Débito à vista ou Crédito em até 10x *SEM JUROS*\n❖ Pix á Vista\n❌ NÃO aceitamos pagamento via boleto bancário\n❌ NÃO geramos link de pagamento \n\n🔥 Não perca essa chance de melhorar seu setup e jogar com qualidade! 🔥\n\n"
    },

    // R$8.390,00
    {
      title: "Nº4 - () SETUP i5 de 10º(10400F) + RTX 3050 E GABINETE STORM-Z",
      image: ".png",
      text: "*Setup ideal para Jogos como:*\n🚔 GTA 5/RP\n\n🔫 CSGO 2\VALORANT\n🦙 FORTNITE\n🐎Red Dead Redemption 2\n🗡Elden Ring\n\n*Placa Mãe:* B560-PRO MSI(LGA 1200)\n*Processador:* I5-10400F(10º GERAÇÃO)\n*Memória RAM:* 2x8GB DDR4 FURY BEAST 3200MHZ *(16GB)*\n*Placa de Vídeo:* RTX 3050 GALAX 6GB\n*Armazenamento:* SSD 480GB\n *AIR Cooler:* REVENGE DUAL FAN RGB \n*Gabinete:* STORM-Z SHARP\n*Fonte:* 500W PFV ATIVO\n+ 🖥️ Monitor  Duex 32' 75hz PLANO Borda Infinita\n+ Kit Mecânico Knup (Teclado Mecânico Switch Azul, Mouse 4800DPI, Headset KP-359, Mousepad XL)\n\nPOR APENAS *R$ 8.390,00* em até 10x sem juros!\n\n*Formas de Pagamento:*\n💳 Cartão - Débito à vista ou Crédito em até 10x *SEM JUROS*\n❖ Pix á Vista\n❌ NÃO aceitamos pagamento via boleto bancário\n❌ NÃO geramos link de pagamento \n\n🔥 Não perca essa chance de melhorar seu setup e jogar com qualidade! 🔥\n\n"
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
