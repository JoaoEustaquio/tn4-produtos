<script>
  const cpus = [
    {
      code: "PO0002",
      title: "PROCESSADOR I5 3ª GERAÇÃO",
      price: 230,
    },
  ]
  const gpus = []
  const motherboards = []
  const memories = []
  const storages = []
  const cases = []

  const today = new Date()
  const year = today.getFullYear()
  const month = today.getMonth()
  const day = today.getDate()

  let monthString = month.toString()
  let dayString = day.toString()

  if (day < 10) dayString =  "0" + dayString
  if (month < 10) monthString = "0" + monthString
</script>

<div>

<table>
  <tr>
    <th>PEDIDO: ________</th>
    <th colspan="2">DATA: {`${dayString}/${monthString}/${year}`}</th>
    <th>VENDEDOR: ________</th>
  </tr>
  <div class="h-8"></div>
  <tr>
    <th>COMPONENTE</th>
    <th class="text-center">QT.</th>
    <th class="text-center">CÓDIGO</th>
    <th>DESCRIÇÃO</th>
  </tr>
  <tr>
    <th>KIT</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>PROCESSADOR</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>PLACA MÃE</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>MEMÓRIA RAM</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>SSD / NVME</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>FONTE</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>GABINETE</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>COOLER FAN</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>COOLER PROCESSADOR</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>PLACA DE VÍDEO</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>TECLADO</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>MOUSE</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
  <tr>
    <th>HEADSET</th>
    <td>0</td>
    <td>NT0001</td>
    <td>Hello World</td>
  </tr>
</table>
</div>

<button on:click={() => print()} class="print:hidden">
  print
</button>

<style lang="postcss">
  tr {
    @apply odd:bg-neutral-100 text-left;
  }

  td:nth-child(2), td:nth-child(3) {
    @apply text-center;
  }

  th {
    @apply whitespace-nowrap;
  }

  td:nth-child(4) {
    @apply w-full;
  }

  th, td {
    @apply border border-neutral-200 p-2;
  }
</style>