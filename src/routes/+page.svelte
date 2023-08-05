<script lang="ts">
    const products = [
        {
            title: "GAMER 1690",
            image: "gabinete1690.jpg",
            text: "Computador GAMER de ENTRADA!\n\n💥 LEAGUE OF LEGENDS (30/40FPS)\n🌎 MINECRAFT (50FPS)\n🟥 ROBLOX (50FPS)\n\n*Processador:* i5 2ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 2 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ MONITOR 16 POLEGADAS, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD 🎧 HEADSET\n\n*R$ 1690,00* em até 10x sem juros!"
        },
        {
            title: "GAMER 1690 + RX 550",
            image: "gabinete1690.jpg",
            text: "Computador GAMER de ENTRADA!\n\n💥 LEAGUE OF LEGENDS (60FPS)\n🌎 MINECRAFT (60/70FPS)\n🟥 ROBLOX (60/70FPS)\n\n*Processador:* i5 2ª GERAÇÃO\n*Memória RAM:* 2x8GB DDR3\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 2 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ MONITOR 16 POLEGADAS, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.690,00* em até 10x sem juros!"
        },
        {
            title: "GAMER RYZEN 5 5600G",
            image: "maquina_ryzen_5.jpg",
            text: "Computador GAMER!\n\n💥 LEAGUE OF LEGENDS (100FPS+)\n🔫 GTA V (40/60FPS)\n🌎 MINECRAFT (150FPS+)\n🔫 WARZONE (40/65FPS)\n🦙 FORTNITE (60/120FPS)\n\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 4 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n*R$ 2990,00* em até 10x sem juros!"
        },
        {
            title: "GAMER I7",
            image: "gabinete1690.jpg",
            text: "Computador GAMER!\n\n💥 LEAGUE OF LEGENDS (100FPS+)\n🔫 GTA V (40/60FPS)\n🌎 MINECRAFT (150FPS+)\n🔫 WARZONE (40/65FPS)\n🦙 FORTNITE (60/120FPS)\n\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 4 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n*R$ 2990,00* em até 10x sem juros!"
        }
    ]

    function copyToClipboard(index: number) {
        navigator.clipboard.writeText(products[index].text)
    }
</script>

<div class="p-8">
    <div class="grid grid-cols-4 gap-8">
        {#each products as product, i}
            <div class="space-y-4">
                <img src={product.image} class="rounded-md w-full h-96 object-cover" alt={product.title}>
                <h1 class="font-bold text-xl truncate">{product.title}</h1>
                <code class="block w-full h-64 overflow-y-scroll whitespace-pre-line bg-gray-100 border border-gray-300 p-2 rounded">
                    {product.text}
                </code>
                <button on:click={() => copyToClipboard(i)} class="w-full bg-black hover:bg-neutral-800 active:bg-neutral-900 text-white px-3 py-2 rounded font-bold">Copiar</button>
            </div>
        {/each}
    </div>
</div>