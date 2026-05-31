<script lang="ts">
  import './layout.css';
  import favicon from '$lib/assets/favicon.svg';

  let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<header class="navbar sticky top-0 z-20 bg-info-content text-base-100 shadow-sm">
  <div class="mx-auto flex w-full max-w-6xl items-center justify-between px-4 sm:px-6">
    <a href="/" class="btn btn-ghost text-xl normal-case">Ash Holdsworth</a>
    <nav class="menu menu-horizontal gap-1 px-0 text-sm">
      <a
        href="https://github.com/AshHoldsworth"
        target="_blank"
        rel="noopener noreferrer"
        class="btn btn-ghost btn-sm"
      >
        GitHub
      </a>
      <a href="/about" class="btn btn-ghost btn-sm">About</a>
    </nav>
  </div>
</header>

<main class="min-h-screen bg-neutral-content pb-10">
  {@render children()}
</main>

<footer class="footer footer-center bg-info-content p-6 text-base-100">
  <p class="text-sm opacity-90">
    Built with
    <a
      href="https://svelte.dev"
      target="_blank"
      rel="noopener noreferrer"
      class="link link-hover font-semibold"
      >SvelteKit</a
    >
    &amp;
    <a
      href="https://tailwindcss.com"
      target="_blank"
      rel="noopener noreferrer"
      class="link link-hover font-semibold"
      >Tailwind CSS</a
    >
  </p>
</footer>
