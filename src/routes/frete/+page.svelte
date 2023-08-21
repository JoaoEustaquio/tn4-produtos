<script lang="ts">
  import CopyButton from "$lib/CopyButton.svelte";
  import IconCopy from "$lib/icons/copy.svelte";

  const frete = [
    { title: "Altura", medida: "44" },
    { title: "Largura", medida: "18" },
    { title: "Comprimento", medida: "39" },
    { title: "Peso", medida: "5,5" },
  ];
</script>

<div class="p-8">
  <a href="/"> ⬅ Home</a>
  <div class="flex justify-between items-center mb-4">
    <h1 class="text-xl font-bold">🚚✉ MEDIDAS PARA FRETE</h1>
  </div>
  <table class="border border-neutral-300 w-full">
    {#each frete as frete}
      <tr class="group border border-neutral-300">
        <th class="text-left border border-neutral-300 p-2 bg-neutral-100"
          >{frete.title}</th
        >
        <td class="p-2 flex justify-between items-center">
          <span>{frete.medida}</span>
        </td>
      </tr>
    {/each}
  </table>
</div>
