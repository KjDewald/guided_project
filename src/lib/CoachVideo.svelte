<script>
    import coachA1 from '../assets/CoachA1.mp4';
    import coachB1 from '../assets/CoachB1.mp4';
    import coachC1 from '../assets/CoachC1.mp4';
    import coachA2 from '../assets/CoachA2.mov';
    import coachB2 from '../assets/CoachB2.mov';
    import CoachC2 from '../assets/CoachC2.mov';

    let { page } = $props();

    let coachPaths = [ coachA1, coachB1, coachC1, coachA2, coachB2, CoachC2 ];
    let coachNumber = [ "Coach A - Ausdauer", "Coach B - Ausdauer", "Coach C - Ausdauer",
                        "Coach A - Kraft", "Coach B - Kraft", "Coach C - Kraft"]

    let header = $derived(coachNumber[page - 1])

    let videoPath = $derived(coachPaths[page - 1])

</script>

  <h2>{header}</h2>
  <video src={videoPath} controls></video>


<style>
  video {
    width: 100%;
    height: 100%;
    object-fit: block;
  }
</style>