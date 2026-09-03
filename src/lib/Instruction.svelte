<script>
    let { onToMovies } = $props();
</script>


<section id="center">
  <p id="welcomeParagraph">Wir freuen uns, dass du an Interesse an unserer Befragung hast! Wir erklären dir kurz was du für die Umfrage machen musst:</p>
  <div id="instructionParagraph">
        <p>Wir wollen testen, welcher der unterschiedlichen Versionen des Coaches am besten bei dir ankommt</p>
        <p>Jede Version des Coaches wird dabei in den exakt gleichen Trainingskontexten gezeigt, das einzige was sich ändern ist die Art wie der Coach den Trainierenden anspricht</p>
        <p>Wir zeigen jede Version des Coaches zuerst in einem Ausdauerkontext. Danach zeigen wir jede Version des Coaches in einem Krafttrainingskontext</p>
        <p>Die Coaches sollen dabei kontinuierlich sein, also in Kraft wie in Ausdauer das Training ähnlich anleiten.</p>
        <p>Die Videos werden in dieser Reihenfolge gezeigt:</p>
    <p class="orderTitle" style="padding-top:5px">AUSDAUER</p>
    <ol id="order">
        <li>Coach A</li>
        <li>Coach B</li>
        <li>Coach C</li>
    </ol>
    <p class="orderTitle" style="padding-top:5px">KRAFT</p>
    <ol id="order">
        <li>Coach A</li>
        <li>Coach B</li>
        <li>Coach C</li>
    </ol>
    <ul style="padding-top:10px">
        <li>Nach den Videos würden wir gerne...
            <br/>
                ...wissen, welchen Coach du am Besten fandest.
            <br/>
                ...dich bitten, einen kurzen, anonymen Persönlichkeitstest auszufüllen.
        </li>
    </ul>
</div>
<div onclick={onToMovies} style="align-self: end; padding-right:10px; cursor:pointer; text-decoration: underline 2px;">ZU DEN VIDEOS ></div>
</section>