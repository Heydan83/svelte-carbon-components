<script>
  // Modules
  import { writable } from 'svelte/store';

  // Props
  export let modalName = "";
  export let buttonText= "";

  let labelName = `modal-${modalName}-label`;
  let headingName = `modal-${modalName}-heading`;
</script>

<button
  class="bx--btn bx--btn--primary"
  type="button"
  data-modal-target=#{modalName}>
  {buttonText}
</button>
