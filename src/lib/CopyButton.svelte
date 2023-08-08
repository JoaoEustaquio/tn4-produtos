<script lang="ts">
    import { createEventDispatcher } from "svelte";

    let disabled = false
    let className = ""

    const dispatch = createEventDispatcher<{ click: null }>()

    function handleClick() {
        disabled = true
        dispatch("click")

        setTimeout(() => disabled = false, 1000)
    }

    export { disabled, className as class }
</script>

<button disabled={disabled} on:click={handleClick} class={className + " button"}>
    {disabled && "✅" || "COPIAR"}
</button>