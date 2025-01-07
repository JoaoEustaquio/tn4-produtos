<script lang="ts">
    import CopyButton from "$lib/CopyButton.svelte"
    import IconCopy from "$lib/icons/copy.svelte"
    
    const monitors = [
        { title: "MONITOR SEMINOVO 19' POL. *SORTIDO* (LC0032) ", price: "R$390,00" },  
        { title: "BLUECASE 19' POL. 75Hz (LC0033)", price: "R$570,00" },    
        { title: "BLUECASE 19' BRANCO LED 75Hz (LC0036)", price: "R$600,00" },
        { title: "VXPRO 21,5' POL. 75Hz (LC0019)", price: "R$690,00" },
        { title: "3GREEN 24' POL. 75Hz (LC0014)", price: "R$890,00" },
        { title: "MONITOR OFFICE BRIGHT, 24' POL., FULL HD, 5MS (LC0077)", price: "R$890,00" },
        { title: "OFFICE BRIGHT, 27' POL., FULL HD, 5MS, IPS, (LC0077)", price: "R$1.090,00" },
        { title: "BLUECASE OPTIGAMER FHD 23.8', 100HZ, 5MS, CURVO (LC0066)", price: "R$1.090,00" },
        { title: "GRASEP LED 23.8', 180HZ, 1MS, (LC0022)", price: "R$1.390,00" },
        { title: "DUEX 32' POL., 75Hz, PLANO (LC0078)", price: "R$1.390,00" },
        { title: "DUEX BLACK 27'POL. LED, 165HZ, 2K (LC0091)", price: "R$1.690,00"},
        { title: "DUEX BLACK 27'POL. LED, 240HZ, 2K (LC0092)", price: "R$1.890,00"},
    ]

    const gpus = [
        { title: "GT 730 4GB REVENGER", price: "R$ 490,00" },
        { title: "RX 550 4GB BIOSTAR", price: "R$ 790,00" },
        { title: "GTX 1650 4GB MSI VENTUS", price: "R$ 1.290,00" },
        { title: "RX 580 8GB VX PRO", price: "R$ 1.290,00" },
        { title: "RTX 3050 8GB PNY VERTO", price: "R$ 1.990,00" },
        { title: "RTX 3060 12GB MSI VENTUS", price: "R$ 2.590,00" },
        { title: "RTX 4060 8GB INNO3D COMPACT", price: "R$ 2.890,00" },
        { title: "RTX 4060 8GB ZOTAC TWIN EDGE", price: "R$ 2.990,00" },
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
        var finalString = "🖥 MONITORES:\n\n"

        monitors.forEach((monitor, i) => { finalString += `*${monitor.title}* por *${monitor.price}*` + ((i + 1) < monitors.length ? "\n" : "") })
        navigator.clipboard.writeText(finalString)
    }
</script>

<svelte:head>
    <title>TN4-TECH PRODUTOS</title>
</svelte:head>

<div class="p-8">
    <div>
        <a href="/notebooks">💻 Notebooks</a>
        <span> | </span>
        <a href="/office">⚙Office⚙</a>
        <span> | </span>
        <a href="/amd">🔴AMD🔴</a>
        <span> | </span>
        <a href="/intel">🔹Intel🔹</a>
        <span> | </span>
        <a href="/setup">⌨🖱 Setup Completo</a>
        <span> | </span>
        <a href="/setupCustom">🖌 Setup Personalizado</a>
        <span> | </span>
        <a href="/pcCustom">🖌 PCs Personalizado</a>
        <span> | </span>
        <a href="/frete">🚚 Medidas Frete</a>
    </div>      

    <div class="grid grid-cols-2 gap-4 mb-8">
        <div>
            <div class="flex justify-between items-center mb-4">
                <h1 class="text-xl font-bold">🖥️ MONITORES</h1>
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
                            <CopyButton on:click={() => navigator.clipboard.writeText(`🖥 *MONITOR ${monitor.title}* por *${monitor.price}*`)} class="text-white bg-black rounded-sm p-1">
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
</div>
