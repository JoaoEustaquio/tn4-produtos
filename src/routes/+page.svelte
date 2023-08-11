<script lang="ts">
    import CopyButton from "$lib/CopyButton.svelte"
    import IconCopy from "$lib/icons/copy.svelte"
    
    const monitors = [
        { title: "15P", price: "R$ 259,00" },
        { title: "16P", price: "R$ 300,00" },
        { title: "17P", price: "R$ 340,00" },
        { title: "20P", price: "R$ 470,00" },
        { title: "22P", price: "R$ 590,00" },
        { title: "20P (LG)", price: "R$ 390,00" },
        { title: "19P (DELL)", price: "R$ 490,00" },
        { title: "20P (DELL)", price: "R$ 580,00" },
        { title: "22P (DELL)", price: "R$ 790,00" }
    ]

    const gpus = [
        { title: "GT 730 2GB", price: "R$ 450,00" },
        { title: "GT 1030 2GB", price: "R$ 790,00" },
        { title: "RX 550 4GB", price: "R$ 890,00" },
        { title: "GTX 1650 4GB", price: "R$ 1.290,00" },
        { title: "RX 580 8GB", price: "R$ 1.190,00" },
        { title: "RTX 3050 8GB", price: "R$ 2.190,00" },
        { title: "RTX 3060 12GB", price: "R$ 2.590,00" }
    ]

    const products = [
        {
            title: "GAMER 1190",
            image: "gabinete1690.png",
            text: "Computador GAMER de ENTRADA!\n\n💥 LEAGUE OF LEGENDS (30/40FPS)\n🌎 MINECRAFT (30/50FPS)\n🟥 ROBLOX (30/50FPS)\n\n*Processador:* i5 3ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 2 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n*R$ 1.190,00* em até 10x sem juros!",
        },
        {
            title: "PC GAMER 1990",
            image: "gabinete1990.png",
            text: "Computador GAMER de ENTRADA!\n\n💥 LEAGUE OF LEGENDS (60FPS)\n🌎 MINECRAFT (60/70FPS)\n🏎 ROCKET LEAGUE (60/70FPS)\n 🚔 GTA RP (40/80FPS)\n🔫 CSGO/VALORANT (60/90FPS)\n\n*Processador:* i5 3ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 2 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n*R$ 1.990,00* em até 10x sem juros!",
        },
        {
            title: "GAMER 1690",
            image: "kit1690.png",
            text: "Computador GAMER de ENTRADA!\n\n💥 LEAGUE OF LEGENDS (30/40FPS)\n🌎 MINECRAFT (30/50FPS)\n🟥 ROBLOX (30/50FPS)\n\n*Processador:* i5 3ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 2 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ MONITOR SEMINOVO 16 POLEGADAS, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD 🎧 HEADSET\n\n*R$ 1.690,00* em até 10x sem juros!",
        },
        {
            title: "GAMER 1690 + RX 550",
            image: "gabinete1990.png",
            text: "Computador GAMER de ENTRADA!\n\n💥 LEAGUE OF LEGENDS (60FPS)\n🌎 MINECRAFT (60/70FPS)\n🟥 ROBLOX (60/70FPS)\n 🚔 GTA RP (40/80FPS)\n🔫 CSGO/VALORANT (60/90FPS)\n\n*Processador:* i5 3ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Placa de Vídeo:* RX 550 4GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 2 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n +*KIT GAMER:* 🖥️ MONITOR SEMINOVO 16 POLEGADAS, ⌨️ TECLADO, 🖱️ MOUSE, MOUSEPAD E 🎧 HEADSET\n\n*R$ 2.590,00* em até 10x sem juros!",
        },
        {
            title: "GAMER RYZEN 5 5600G",
            image: "maquina_ryzen_5.png",
            text: "Computador GAMER!\n\n💥 LEAGUE OF LEGENDS (100FPS+)\n🚔 GTA RP (40/80FPS)\n🌎 MINECRAFT (150FPS+)\n🔫 WARZONE (40/65FPS)\n🦙 FORTNITE (60/120FPS)\n\n*Processador:* RYZEN 5 5600G\n*Memória RAM:* 16GB DDR4\n*Placa de Vídeo:* VEGA 7 (INTEGRADO)\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 4 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n*R$ 2990,00* em até 10x sem juros!",
        },
        {
            title: "GAMER I7 3 GERAÇÃO",
            image: "gabinete1690.png",
            text: "Computador GAMER!\n\n💥 LEAGUE OF LEGENDS (100FPS+)\n🚔 GTA RP (40/80FPS)\n🌎 MINECRAFT (150FPS+)\n🔫 WARZONE (40/65FPS)\n🦙 FORTNITE (60/120FPS)\n\n*Processador:* i7 3ª GERAÇÃO\n*Memória RAM:* 8GB DDR3\n*Placa de Vídeo:* RX 580 8GB\n*Armazenamento:* SSD 256GB\n*Gabinete:* GAMER 2 FANS RGB NA FRENTE\n*Fonte:* 500W\n\n*R$ 2.690,00* em até 10x sem juros!",
        },
    ]

    function copyToClipboard(product: { text: string }) {
        navigator.clipboard.writeText(product.text)
    }

    function allGPUs() {
        var finalString = "🎮 PLACAS DE VÍDEO:\n\n"
        gpus.forEach((gpu, i) => { finalString += `*${gpu.title}* por *${gpu.price}*` + ((i + 1) < gpus.length ? "\n" : "") })

        navigator.clipboard.writeText(finalString)

    }

    function allMonitors() {
        var finalString = "🖥 MONITORES SEMINOVOS:\n\n"

        monitors.forEach((monitor, i) => { finalString += `*${monitor.title}* por *${monitor.price}*` + ((i + 1) < monitors.length ? "\n" : "") })
        navigator.clipboard.writeText(finalString)
    }
</script>

<svelte:head>
    <title>TN4-TECH PRODUTOS</title>
</svelte:head>

<div class="p-8">

    <div>
        <CopyButton on:click={() => allMonitors()} class="space-x-2">
            <IconCopy />
            <span class="text-sm tracking-wider">NOTEBOOKS</span>
        </CopyButton>
    </div>


    <div class="grid grid-cols-2 gap-4 mb-8">
        <div>
            <div class="flex justify-between items-center mb-4">
                <h1 class="text-xl font-bold">🖥️ MONITORES SEMINOVOS</h1>
                <CopyButton on:click={() => allMonitors()} class="space-x-2">
                    <IconCopy />
                    <span class="text-sm tracking-wider">COPIAR TODOS</span>
                </CopyButton>
            </div>
            <table class="border border-neutral-300 w-full">
                {#each monitors as monitor}
                    <tr class="group border border-neutral-300">
                        <th class="text-left border border-neutral-300 p-2 bg-neutral-100">{monitor.title}</th>
                        <td class="p-2 flex justify-between items-center">
                            <span>{monitor.price}</span>
                            <CopyButton on:click={() => navigator.clipboard.writeText(`🖥 *MONITOR SEMINOVO ${monitor.title}* por *${monitor.price}*`)} class="text-white bg-black rounded-sm p-1">
                                <IconCopy />
                            </CopyButton>
                        </td>
                    </tr>
                {/each}
            </table>
        </div>

        <div>
            <div class="flex justify-between items-center mb-4">
                <h1 class="text-xl font-bold">🎮 PLACAS DE VÍDEO</h1>
                <CopyButton on:click={() => allGPUs()} class="space-x-2">
                    <IconCopy />
                    <span class="text-sm tracking-wider">COPIAR TODOS</span>
                </CopyButton>
            </div>
            <table class="border border-neutral-300 w-full">
                {#each gpus as gpu}
                    <tr class="border border-neutral-300">
                        <th class="text-left border border-neutral-300 p-2 bg-neutral-100">{gpu.title}</th>
                        <td class="p-2 flex justify-between items-center">
                            <span>{gpu.price}</span>
                            <CopyButton on:click={() => navigator.clipboard.writeText(`🎮 *${gpu.title}* por *${gpu.price}*`)} class="text-white bg-black rounded-sm p-1">
                                <IconCopy />
                            </CopyButton>
                        </td>
                    </tr>
                {/each}
            </table>
        </div>
    </div>


    <h1 class="text-xl font-bold mb-4">⚙️ MÁQUINAS PRONTAS</h1>
    <div class="grid grid-cols-4 gap-8">
        {#each products as product}
            <div class="space-y-4">
                <img src={product.image} class="rounded-md w-full h-64 object-contain border border-gray-200 bg-gray-50" alt={product.title}>
                <h1 class="font-bold text-xl truncate">{product.title}</h1>
                <code class="font-mono-emoji block w-full h-64 overflow-y-scroll whitespace-pre-line bg-gray-100 border border-gray-300 p-2 rounded">
                    {product.text}
                </code>

                <CopyButton class="w-full tracking-wider text-sm" on:click={() => copyToClipboard(product)}>COPIAR</CopyButton>
            </div>
        {/each}
    </div>
</div>
