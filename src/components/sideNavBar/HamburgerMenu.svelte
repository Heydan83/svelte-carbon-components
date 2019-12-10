<script>
  // Props
  export let isShown = false;

  // Functions
  function changeAndFocusBtn() {
    isShown = !isShown;
    setTimeout(() => {
      if (isShown) {
        document.getElementById("closeBtnElement").focus();
      } else {
        document.getElementById("openBtnElement").focus();
      }
    }, 0.00000001);
  }
</script>

{#if isShown}
  <button
    id="closeBtnElement"
    on:click={changeAndFocusBtn}
    aria-label="Open menu"
    class="bx--header__action bx--header__menu-trigger
    bx--header__action--active bx--header__menu-toggle"
    title="Open menu"
    type="button">
    <svg
      focusable="false"
      preserveAspectRatio="xMidYMid meet"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 32 32"
      aria-hidden="true"
      style="will-change: transform;">
      <path
        d="M24 9.4L22.6 8 16 14.6 9.4 8 8 9.4l6.6 6.6L8 22.6 9.4 24l6.6-6.6 6.6
        6.6 1.4-1.4-6.6-6.6L24 9.4z" />
    </svg>
  </button>
{:else}
  <button
    id="openBtnElement"
    on:click={changeAndFocusBtn}
    aria-label="Open menu"
    class="bx--header__action bx--header__menu-trigger bx--header__menu-toggle"
    title="Open menu"
    type="button">
    <svg
      focusable="false"
      preserveAspectRatio="xMidYMid meet"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20"
      aria-hidden="true"
      style="will-change: transform;">
      <path
        d="M2 14.8h16V16H2zm0-3.6h16v1.2H2zm0-3.6h16v1.2H2zM2 4h16v1.2H2z" />
    </svg>
  </button>
{/if}