<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  // trigger event and send object
  function sayHello() {
    dispatch("eventName", {
      text: "nice event"
    });
  }
</script>

<button on:click={sayHello}>Click for your custom event</button>
