<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";
  import IconCopy from "$lib/icons/copy.svelte";

  const fretePC = [
    { title: "Altura", medida: "44" },
    { title: "Largura", medida: "18" },
    { title: "Comprimento", medida: "39" },
    { title: "Peso", medida: "5,5" },
  ];

  const freteNOTE = [
    { title: "Altura", medida: "3" },
    { title: "Largura", medida: "24" },
    { title: "Comprimento", medida: "34" },
    { title: "Peso", medida: "2,5" },
  ];
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <div class="flex justify-between items-center mb-4">
    <h1 class="text-xl font-bold">🚚✉ FRETE PC GAMER</h1>
  </div>
  <table class="border border-neutral-300 w-full">
    {#each fretePC as fretePC}
      <tr class="group border border-neutral-300">
        <th class="text-left border border-neutral-300 p-2 bg-neutral-100"
          >{fretePC.title}</th
        >
        <td class="p-2 flex justify-between items-center">
          <span>{fretePC.medida}</span>
        </td>
      </tr>
    {/each}
  </table>
</div>

<div class="p-8">
  <div class="flex justify-between items-center mb-4">
    <h1 class="text-xl font-bold">🚚✉ FRETE NOTEBOOK</h1>
  </div>
  <table class="border border-neutral-300 w-full">
    {#each freteNOTE as freteNOTE}
      <tr class="group border border-neutral-300">
        <th class="text-left border border-neutral-300 p-2 bg-neutral-100"
          >{freteNOTE.title}</th
        >
        <td class="p-2 flex justify-between items-center">
          <span>{freteNOTE.medida}</span>
        </td>
      </tr>
    {/each}
  </table>
</div>
