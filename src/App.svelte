<script>
  import SourceGraph from "./components/sourcesGraph/sourceGraph.svelte";
  import SdgGraph from "./components/sdgGraph/sdgGraph.svelte";
  import ProductGraph from "./components/productGraph/productGraph.svelte";
</script>

<main>
  <SourceGraph/>
  <br><br>
  <SdgGraph/>
  <br><br>
  <ProductGraph/>
</main>

<style>
  :global(.graph-container){
    margin-bottom: 100px;
  }
</style>
