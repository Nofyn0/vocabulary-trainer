<script>
  import Button from './Button.svelte'
  import { SkeletonPlaceholder } from 'carbon-components-svelte'

  import { currentWord } from './stores'
  import 'carbon-components-svelte/css/g10.css'
  import 'carbon-components-svelte/css/all.css'

  $: {
    console.log($currentWord)
  }
</script>

<main>
  <h1>{$currentWord.source}</h1>
  <div class="placeholder">
    <SkeletonPlaceholder style="height: 8em;  width: 14rem;" />
  </div>

  <Button />
</main>

<style>
  h1 {
    text-transform: capitalize;
    font-weight: bold;
    font-size: 3rem;
  }

  .placeholder {
    margin: 0 auto;
    margin: 2rem 0;
    display: flex;
    justify-content: center;
  }

  main {
    padding: 1em;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>
