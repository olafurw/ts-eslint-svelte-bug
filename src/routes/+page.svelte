<script lang="ts">
  import Bug from "$lib/Bug.svelte";

  $: value = '';

  function updateValue(newValue: string) {
    value = newValue;
  }
</script>

<Bug someFunction={updateValue} />

{value}
