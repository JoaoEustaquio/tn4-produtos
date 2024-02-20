<script lang="ts">
    import CopyButton from "$lib/CopyButton.svelte"
    import IconCopy from "$lib/icons/copy.svelte"
    
    const monitors = [
        { title: "(LC0042) 19' 75Hz Bluecase", price: "R$ 490,00" },
        { title: "(LC0071) 21,5' 75Hz", price: "R$ 650,00" },
        { title: "(LC0072) 23,5' 75Hz", price: "R$ 790,00" },
        { title: "(LC0049) 24' 75Hz HQ", price: "R$ 790,00" },
        { title: "(LC0041) 23,8' 100Hz", price: "R$ 990,00" },
        { title: "(LC0067) 24' 144Hz", price: "R$ 1.190,00" },
        { title: "(LC0064) 23.6' *CURVO* 180Hz", price: "R$ 1.390,00" },
        { title: "(LC0074) GAMER Bluecase 27' *CURVO* 165Hz", price: "R$ 1.590,00" },
        { title: "(LC0040) GAMER Bluecase 27' HIPERVIEW BRANCO *CURVO* 165Hz", price: "R$ R$1.690,00" },
        { title: "(LC0039) GAMER DUEX 27' *CURVO* 240Hz", price: "R$ R$1.790,00" },
        { title: "(LC0059) GAMER SUPERFRAME ELEGANCE SERIES WHITE 30' *CURVO, ULTRAWIDE*", price: "R$ R$2.290,00" },
    ]

    const gpus = [
        { title: "RX 550 4GB", price: "R$ 790,00" },
        { title: "GTX 1650 4GB VENTUS", price: "R$ 1.290,00" },
        { title: "RX 570 8GB", price: "R$ 1.390,00" },
        { title: "RX 580 8GB", price: "R$ 1.590,00" },
        { title: "RTX 3050 8GB", price: "R$ 1.990,00" },
        { title: "RTX 3060 8GB PEGASUS", price: "R$ 2.390,00" },
        { title: "RTX 4060 8GB", price: "R$ 2.790,00" },
        { title: "RTX 4060 TI", price: "R$ 3.990,00" },
        { title: "RTX 4070 MSI WHITE", price: "R$ 5.290,00" },
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
