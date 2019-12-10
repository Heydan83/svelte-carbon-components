<script>
  // Modules
  import { fly } from "svelte/transition";
  import { quintOut } from "svelte/easing";

  // Props
  export let isShown = false;
  export let winWidth = "";

  // Variables
  let title;

  // Reactivities
  $: setTitle = isShown ? "Open" : "Close"
</script>

{#if isShown || winWidth >= 1056}
  <nav
    transition:fly={{ x: -200, delay: 100, duration: 300, easing: quintOut }}
    class="bx--side-nav__navigation bx--side-nav bx--side-nav--ux"
    class:bx--side-nav--expanded={isShown}
    aria-label="Side navigation">
    <ul class="bx--side-nav__items">
      <li class="bx--side-nav__item bx--side-nav__item--icon">
        <button
          aria-haspopup="true"
          aria-expanded="false"
          class="bx--side-nav__submenu"
          type="button">
          <div class="bx--side-nav__icon">
            <svg
              width="16"
              height="16"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 32 32"
              aria-hidden="true">
              <path
                d="M8.24 25.14L7 26.67a14 14 0 0 0 4.18 2.44l.68-1.88a12 12 0 0
                1-3.62-2.09zm-4.05-7.07l-2 .35A13.89 13.89 0 0 0 3.86
                23l1.73-1a11.9 11.9 0 0 1-1.4-3.93zm7.63-13.31l-.68-1.88A14 14 0
                0 0 7 5.33l1.24 1.53a12 12 0 0 1 3.58-2.1zM5.59 10L3.86 9a13.89
                13.89 0 0 0-1.64 4.54l2 .35A11.9 11.9 0 0 1 5.59 10zM16 2v2a12
                12 0 0 1 0 24v2a14 14 0 0 0 0-28z" />
            </svg>
          </div>
          <span class="bx--side-nav__submenu-title">Category title</span>
          <div
            class="bx--side-nav__icon bx--side-nav__icon--small
            bx--side-nav__submenu-chevron">
            <svg
              focusable="false"
              preserveAspectRatio="xMidYMid meet"
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 32 32"
              aria-hidden="true"
              style="will-change: transform;">
              <path d="M16 22L6 12l1.4-1.4 8.6 8.6 8.6-8.6L26 12z" />
            </svg>
          </div>
        </button>
        <ul class="bx--side-nav__menu" role="menu">
          <li class="bx--side-nav__menu-item" role="none">
            <a
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
          <li class="bx--side-nav__menu-item" role="none">
            <a
              aria-current="page"
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
          <li class="bx--side-nav__menu-item" role="none">
            <a
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
        </ul>
      </li>
      <li class="bx--side-nav__item bx--side-nav__item--icon">
        <button
          aria-haspopup="true"
          aria-expanded="false"
          class="bx--side-nav__submenu"
          type="button">
          <div class="bx--side-nav__icon">
            <svg
              width="16"
              height="16"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 32 32"
              aria-hidden="true">
              <path
                d="M8.24 25.14L7 26.67a14 14 0 0 0 4.18 2.44l.68-1.88a12 12 0 0
                1-3.62-2.09zm-4.05-7.07l-2 .35A13.89 13.89 0 0 0 3.86
                23l1.73-1a11.9 11.9 0 0 1-1.4-3.93zm7.63-13.31l-.68-1.88A14 14 0
                0 0 7 5.33l1.24 1.53a12 12 0 0 1 3.58-2.1zM5.59 10L3.86 9a13.89
                13.89 0 0 0-1.64 4.54l2 .35A11.9 11.9 0 0 1 5.59 10zM16 2v2a12
                12 0 0 1 0 24v2a14 14 0 0 0 0-28z" />
            </svg>
          </div>
          <span class="bx--side-nav__submenu-title">Category title</span>
          <div
            class="bx--side-nav__icon bx--side-nav__icon--small
            bx--side-nav__submenu-chevron">
            <svg
              focusable="false"
              preserveAspectRatio="xMidYMid meet"
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 32 32"
              aria-hidden="true"
              style="will-change: transform;">
              <path d="M16 22L6 12l1.4-1.4 8.6 8.6 8.6-8.6L26 12z" />
            </svg>
          </div>
        </button>
        <ul class="bx--side-nav__menu" role="menu">
          <li class="bx--side-nav__menu-item" role="none">
            <a
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
          <li class="bx--side-nav__menu-item" role="none">
            <a
              aria-current="page"
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
          <li class="bx--side-nav__menu-item" role="none">
            <a
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
        </ul>
      </li>
      <li class="bx--side-nav__item bx--side-nav__item--icon">
        <button
          aria-haspopup="true"
          aria-expanded="false"
          class="bx--side-nav__submenu"
          type="button">
          <div class="bx--side-nav__icon">
            <svg
              width="16"
              height="16"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 32 32"
              aria-hidden="true">
              <path
                d="M8.24 25.14L7 26.67a14 14 0 0 0 4.18 2.44l.68-1.88a12 12 0 0
                1-3.62-2.09zm-4.05-7.07l-2 .35A13.89 13.89 0 0 0 3.86
                23l1.73-1a11.9 11.9 0 0 1-1.4-3.93zm7.63-13.31l-.68-1.88A14 14 0
                0 0 7 5.33l1.24 1.53a12 12 0 0 1 3.58-2.1zM5.59 10L3.86 9a13.89
                13.89 0 0 0-1.64 4.54l2 .35A11.9 11.9 0 0 1 5.59 10zM16 2v2a12
                12 0 0 1 0 24v2a14 14 0 0 0 0-28z" />
            </svg>
          </div>
          <span class="bx--side-nav__submenu-title">Category title</span>
          <div
            class="bx--side-nav__icon bx--side-nav__icon--small
            bx--side-nav__submenu-chevron">
            <svg
              focusable="false"
              preserveAspectRatio="xMidYMid meet"
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 32 32"
              aria-hidden="true"
              style="will-change: transform;">
              <path d="M16 22L6 12l1.4-1.4 8.6 8.6 8.6-8.6L26 12z" />
            </svg>
          </div>
        </button>
        <ul class="bx--side-nav__menu" role="menu">
          <li class="bx--side-nav__menu-item" role="none">
            <a
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
          <li class="bx--side-nav__menu-item" role="none">
            <a
              aria-current="page"
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
          <li class="bx--side-nav__menu-item" role="none">
            <a
              href="javascript:void(0)"
              class="bx--side-nav__link"
              role="menuitem">
              <span class="bx--side-nav__link-text">Link</span>
            </a>
          </li>
        </ul>
      </li>
      <li class="bx--side-nav__item">
        <a href="javascript:void(0)" class="bx--side-nav__link">
          <div class="bx--side-nav__icon bx--side-nav__icon--small">
            <svg
              width="16"
              height="16"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 32 32"
              aria-hidden="true">
              <path
                d="M8.24 25.14L7 26.67a14 14 0 0 0 4.18 2.44l.68-1.88a12 12 0 0
                1-3.62-2.09zm-4.05-7.07l-2 .35A13.89 13.89 0 0 0 3.86
                23l1.73-1a11.9 11.9 0 0 1-1.4-3.93zm7.63-13.31l-.68-1.88A14 14 0
                0 0 7 5.33l1.24 1.53a12 12 0 0 1 3.58-2.1zM5.59 10L3.86 9a13.89
                13.89 0 0 0-1.64 4.54l2 .35A11.9 11.9 0 0 1 5.59 10zM16 2v2a12
                12 0 0 1 0 24v2a14 14 0 0 0 0-28z" />
            </svg>
          </div>
          <span class="bx--side-nav__link-text">Link</span>
        </a>
      </li>
      <li class="bx--side-nav__item">
        <a href="javascript:void(0)" class="bx--side-nav__link">
          <div class="bx--side-nav__icon bx--side-nav__icon--small">
            <svg
              width="16"
              height="16"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 32 32"
              aria-hidden="true">
              <path
                d="M8.24 25.14L7 26.67a14 14 0 0 0 4.18 2.44l.68-1.88a12 12 0 0
                1-3.62-2.09zm-4.05-7.07l-2 .35A13.89 13.89 0 0 0 3.86
                23l1.73-1a11.9 11.9 0 0 1-1.4-3.93zm7.63-13.31l-.68-1.88A14 14 0
                0 0 7 5.33l1.24 1.53a12 12 0 0 1 3.58-2.1zM5.59 10L3.86 9a13.89
                13.89 0 0 0-1.64 4.54l2 .35A11.9 11.9 0 0 1 5.59 10zM16 2v2a12
                12 0 0 1 0 24v2a14 14 0 0 0 0-28z" />
            </svg>
          </div>
          <span class="bx--side-nav__link-text">Link</span>
        </a>
      </li>
    </ul>
    <footer class="bx--side-nav__footer">
      <button class="bx--side-nav__toggle" type="button" title={setTitle}>
        <div class="bx--side-nav__icon">
          <svg
            focusable="false"
            preserveAspectRatio="xMidYMid meet"
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 32 32"
            aria-hidden="true"
            style="will-change: transform;">
            {#if isShown}
              <path
                d="M24 9.4L22.6 8 16 14.6 9.4 8 8 9.4l6.6 6.6L8 22.6 9.4
                24l6.6-6.6 6.6 6.6 1.4-1.4-6.6-6.6L24 9.4z" />
            {:else}
              <path d="M22 16L12 26l-1.4-1.4 8.6-8.6-8.6-8.6L12 6z" />
            {/if}
          </svg>
        </div>
        <span class="bx--assistive-text">{setTitle}</span>
      </button>
    </footer>
  </nav>
{/if}
