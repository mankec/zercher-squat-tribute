<script lang="ts">
  import "./layout.css";
  import Navbar from "$lib/components/Navbar.svelte";

  const { children } = $props();
</script>

<Navbar />

<div class="bg-red-500">
  {@render children()}
</div>
