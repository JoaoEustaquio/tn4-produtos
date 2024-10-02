<script lang="ts">
    import CopyButton from "$lib/CopyButton.svelte"
    import IconCopy from "$lib/icons/copy.svelte"
    
    const monitors = [
        { title: "BLUECASE 19' POL. 75Hz (LC0020)", price: "R$ R$590,00" },
        { title: "VXPRO 21,5' POL. 75Hz (LC0019)", price: "R$ R$690,00" },
        { title: "3GREEN 24' POL. 75Hz (LC0014)", price: "R$ R$890,00" },
        { title: "GRASEP LED 23.8', 100HZ, 1MS, (LC0021)", price: "R$ R$1.050,00" },
        { title: "GAMER BLUECASE 23,8' POL. 100Hz CURVO OPTIGAMER *BRANCO* (LC0066B)", price: "R$ R$1.190,00" },
        { title: "GAMER DUEX CURVO 31,5 POL. 75HZ (LC0017)", price: "R$ R$1.190,00" },
        { title: "GRASEP LED 23.8', 180HZ, 1MS, (LC0022)", price: "R$ R$1.390,00" },
        { title: "GAMER MANCER VALAK 32' CURVO 165HZ (LC0051M) ", price: "R$ R$2.190,00" },
    ]

    const gpus = [
        { title: "RX 550 4GB", price: "R$ 790,00" },
        { title: "RADEON RX 560 4GB GDDR5 128 BITS - PCWINMAX", price: "R$ 1,090,99" },
        { title: "RX 580 BRX 8GB", price: "R$ 1.290,00" },
        { title: "GTX 1650 4GB VENTUS", price: "R$ 1.290,00" },
        { title: "RTX 3050 6GB", price: "R$ 1.990,00" },
        { title: "RTX 3060 12GB", price: "R$ 2.490,00" },
        { title: "RTX 4060 8GB", price: "R$ 2.790,00" },
        { title: "RTX 3060 TI PLUS 8GB GALAX, GDDR6X, 256BITS ", price: "R$3.390,00" },
        { title: "RTX 4070 12GB", price: "R$ 5.890,00" },
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
        <a href="/setup">Setup Completo</a>
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
