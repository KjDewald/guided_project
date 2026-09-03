<script>
  import Contribution from './lib/Contribution.svelte';
  import Demo from './lib/Demo.svelte';
  import Default from './lib/Default.svelte';

  let showDemo = $state(false);
  let showContribution = $state(false);
  

  function handleShowDemo(){
    showDemo = true;
    showContribution = false;
  }

  function handleShowContribution(){
    showContribution = true;
    showDemo = false;
  }
</script>

{#if !showDemo && !showContribution}
  <Default onShowDemo={handleShowDemo} onShowContribution={handleShowContribution}/>
{:else if showDemo && !showContribution}
  <section id="navigation">
    <div class="navItem active"id="navDemo">DEMO</div>
    <div class="navItem" id ="navContribute" onclick={handleShowContribution}>UMFRAGE</div>
  </section>
  <Demo/>
{:else}
  <section id="navigation">
    <div class="navItem"id="navDemo" onclick={handleShowDemo}>DEMO</div>
    <div class="navItem active" id ="navContribute">UMFRAGE</div>
  </section>
  <Contribution/>
{/if}

