<script>
  import OnEvent from "./components/OnEvents.svelte";
  import CustomEvent from "./components/CustomEvent.svelte";
  import FancyImage from "./components/FancyImage.svelte";

  function handleHover() {
    console.log("hovered");
  }
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <OnEvent />
  <CustomEvent
    on:eventName={(event, args) => {
      console.log(event, args);
    }} />
  <FancyImage on:mouseover={handleHover} />
</main>
