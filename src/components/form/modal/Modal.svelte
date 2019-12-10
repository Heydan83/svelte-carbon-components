<script>
  // Props
  export let selectedOption = null;
  export let modalName = "";
  export let modalOptionalLabel= "";
  export let modalHeading= "";
  export let modalBody= "";
  export let primaryButton= "";
  export let scondaryButton= "";

  let labelName = `modal-${modalName}-label`;
  let headingName = `modal-${modalName}-heading`;
</script>

<div
  data-modal
  id={modalName}
  class="bx--modal "
  role="dialog"
  aria-modal="true"
  aria-labelledby={labelName}
  aria-describedby={headingName}
  tabindex="-1">
  <div class="bx--modal-container">
    <div class="bx--modal-header">
      <p
        class="bx--modal-header__label bx--type-delta"
        id={labelName}>
        {modalOptionalLabel}
      </p>
      <p
        class="bx--modal-header__heading bx--type-beta"
        id={headingName}>
        {modalHeading}
      </p>
      <button
        on:click={() => (selectedOption = '0')}
        class="bx--modal-close"
        type="button"
        data-modal-close
        aria-label="close modal">
        <svg
          focusable="false"
          preserveAspectRatio="xMidYMid meet"
          style="will-change: transform;"
          xmlns="http://www.w3.org/2000/svg"
          class="bx--modal-close__icon"
          width="16"
          height="16"
          viewBox="0 0 16 16"
          aria-hidden="true">
          <path
            d="M12 4.7L11.3 4 8 7.3 4.7 4 4 4.7 7.3 8 4 11.3 4.7 12 8 8.7 11.3
            12 12 11.3 8.7 8z" />
        </svg>
      </button>
    </div>
    <!-- Note: Modals with content that scrolls, at any viewport, requires `tabindex="0"` on the `bx--modal-content` element -->
    <div class="bx--modal-content">
      <p>
        {modalBody}
      </p>
    </div>
    <div class="bx--modal-footer">
      <button
        on:click={() => (selectedOption = '2')}
        class="bx--btn bx--btn--secondary"
        type="button"
        data-modal-close>
        {scondaryButton}
      </button>
      <button
        on:click={() => (selectedOption = '1')}
        class="bx--btn bx--btn--primary"
        type="button"
        data-modal-primary-focus
        data-modal-close>
        {primaryButton}
      </button> 
    </div>
  </div>
  <!-- Note: focusable span allows for focus wrap feature within Modals -->
  <span tabindex="0" />
</div>