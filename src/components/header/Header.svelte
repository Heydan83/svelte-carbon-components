<script>
  // Components
  import HamburgerMenu from "../sideNavBar/HamburgerMenu.svelte";
  import SideNavBar from "../sideNavBar/SideNavBar.svelte";
  import HeaderSearch from "./HeaderSearch.svelte";
  import HeaderNotification from "./HeaderNotification.svelte";
  import HeaderAppSwitcher from "./HeaderAppSwitcher.svelte";

  // Props
  export let isShown = false;
  export let firstTabIndexText = "";
  export let company = "";
  export let platform = "";
  export let platformShort = "";
  export let searchIcon = false;
  export let notificationIcon = false;
  export let appSwitcherIcon = false;

  // Reactivities
  $: winWidth = window.innerWidth;
</script>

<header aria-label="Header" class="bx--header" role="banner">
  <a class="bx--skip-to-content" href="#main-content" tabindex="0">
    {firstTabIndexText}
  </a>
  <HamburgerMenu bind:isShown />
  <a class="bx--header__name" href="google.com">
    <span class="bx--header__name--prefix">{company}</span>
    {#if winWidth >= 520}
      &nbsp;[{platform}]
    {:else}
       &nbsp;[{platformShort}]
    {/if}
  </a>
  <div class="bx--header__global">
    {#if searchIcon}
      <HeaderSearch />
    {/if}
    {#if notificationIcon}
      <HeaderNotification />
    {/if}
    {#if appSwitcherIcon}
      <HeaderAppSwitcher />
    {/if}
  </div>
  <SideNavBar isShown={isShown} winWidth={winWidth} />
</header>
