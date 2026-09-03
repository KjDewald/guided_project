<script>
  import Instruction from "./Instruction.svelte";
  import CoachVideo from "./CoachVideo.svelte";
    import Thanks from "./Thanks.svelte";


  let navigationPageCount = $state(0); 

  function handleToMovies(){
    navigationPageCount = 1;
  }

  function handleNextVideo(){
    navigationPageCount = navigationPageCount + 1;
  }

  function handlePreviousVideo(){
    navigationPageCount = navigationPageCount - 1;
  }

</script>


{#if navigationPageCount == 0}
  <Instruction onToMovies={handleToMovies} />

{:else if navigationPageCount == 7}
  <Thanks />

{:else}
  <section id="center">
    <CoachVideo page={navigationPageCount} />

    <section id="videoNav">
      {#if navigationPageCount > 1 && navigationPageCount < 6}
        <p onclick={handlePreviousVideo} style="cursor:pointer">&lt; Letztes Video</p>
        <p onclick={handleNextVideo} style="cursor:pointer">Nächstes Video &gt;</p>
      {:else if navigationPageCount == 1}
        <p onclick={handleNextVideo} style="cursor:pointer">Nächstes Video &gt;</p>
      {:else if navigationPageCount == 6}
        <p onclick={handlePreviousVideo} style="cursor:pointer">&lt; Letztes Video</p>
        <p onclick={handleNextVideo} style="cursor:pointer">Zum Umfragelink &gt;</p>
      {/if}
    </section>
  </section>
{/if}