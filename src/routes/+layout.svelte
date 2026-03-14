<script lang="ts">
  import "./layout.css";
  import Navbar from "$lib/components/Navbar.svelte";

  const { children } = $props();
</script>

<Navbar />

{@render children()}
