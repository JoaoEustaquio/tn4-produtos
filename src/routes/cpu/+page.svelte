<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";
  import IconCopy from "$lib/icons/copy.svelte";

  const intel = [
    { code: "PO0002", title: "Intel Core I5-3470 (3ªGEN)", price: "R$220,00" },
    { code: "PO0133", title: "Intel Core I7-3770 (3ªGEN)", price: "R$570,00" },
];

  const amd = [
    { code: "PO0040", title: "ATHLON 3000G", price: "R$600,00" },
    { code: "PO0035", title: "AMD Ryzen 5 4500", price: "R$890,00" },
  ];

  function copyToClipboard(product: { text: string }) {
    navigator.clipboard.writeText(product.text);
  }

  function allAmd() {
    var finalString = "Processadores AMD:\n\n";
    amd.forEach((Amd, i) => {
      finalString +=
        `*${Amd.title}* por *${Amd.price}*` + (i + 1 < amd.length ? "\n" : "");
    });

    navigator.clipboard.writeText(finalString);
  }

  function allIntel() {
    var finalString = "Processadores Intel:\n\n";

    intel.forEach((Intel, i) => {
      finalString +=
        `*${Intel.title}* por *${Intel.price}*` +
        (i + 1 < intel.length ? "\n" : "");
    });
    navigator.clipboard.writeText(finalString);
  }
</script>

<svelte:head>
  <title>TN4-TECH PRODUTOS</title>
</svelte:head>

<div class="p-8">
  <div>
    <a href="/"> ⬅ Home</a>
    <span> | </span>
  </div>

  <div class="grid grid-cols-2 gap-4 mb-8">
    <div>
      <div class="flex justify-between items-center mb-4">
        <h1 class="text-xl font-bold">🟦INTEL</h1>
        <CopyButton on:click={() => allIntel()} class="space-x-2">
          <IconCopy />
          <span class="text-sm tracking-wider">COPIAR TODOS</span>
        </CopyButton>
      </div>
      <table class="border border-neutral-300 w-full">
        {#each intel as Intel}
          <tr class="group border border-neutral-300">
            <th class="text-left border border-neutral-300 p-2 bg-neutral-100"
              >{Intel.code} | {Intel.title}</th
            >
            <td class="p-2 flex justify-between items-center">
              <span>{Intel.price}</span>
              <CopyButton
                on:click={() =>
                  navigator.clipboard.writeText(
                    `🖥 *PROCESSADOR ${Intel.title}* por *${Intel.price}*`
                  )}
                class="text-white bg-black rounded-sm p-1"
              >
                <IconCopy />
              </CopyButton>
            </td>
          </tr>
        {/each}
      </table>
    </div>

    <div>
      <div class="flex justify-between items-center mb-4">
        <h1 class="text-xl font-bold">🟥AMD</h1>
        <CopyButton on:click={() => allAmd()} class="space-x-2">
          <IconCopy />
          <span class="text-sm tracking-wider">COPIAR TODOS</span>
        </CopyButton>
      </div>
      <table class="border border-neutral-300 w-full">
        {#each amd as Amd}
          <tr class="border border-neutral-300">
            <th class="text-left border border-neutral-300 p-2 bg-neutral-100"
              >{Amd.code} | {Amd.title}</th
            >
            <td class="p-2 flex justify-between items-center">
              <span>{Amd.price}</span>
              <CopyButton
                on:click={() =>
                  navigator.clipboard.writeText(
                    `🎮 *${Amd.title}* por *${Amd.price}*`
                  )}
                class="text-white bg-black rounded-sm p-1"
              >
                <IconCopy />
              </CopyButton>
            </td>
          </tr>
        {/each}
      </table>
    </div>
  </div>
</div>
