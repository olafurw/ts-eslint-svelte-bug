<script lang="ts">
    import SomeOtherComponent from "./SomeOtherComponent.svelte";

    export let someFunction: ((value: string) => void) | undefined = undefined;
    let value: string | null = null;

    $: {
        if (value !== null && someFunction) {
            someFunction(value);
        }
    }
</script>

<SomeOtherComponent
    bind:value
/>