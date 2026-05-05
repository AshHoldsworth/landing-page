<script lang="ts">
  import './layout.css';
  import favicon from '$lib/assets/favicon.svg';

  let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<!-- Nav -->
<header class="sticky top-0 z-10 border-b border-gray-200 bg-white/80 backdrop-blur">
  <div class="mx-auto flex max-w-5xl items-center justify-between px-6 py-4">
    <a href="/" class="text-lg font-semibold tracking-tight text-gray-900">Ash Holdsworth</a>
    <nav class="flex gap-6 text-sm text-gray-600">
      <a
        href="https://github.com/AshHoldsworth"
        target="_blank"
        rel="noopener noreferrer"
        class="transition-colors hover:text-gray-900"
      >
        GitHub
      </a>
      <a href="/about" class="transition-colors hover:text-gray-900"> About </a>
    </nav>
  </div>
</header>

<main>
  {@render children()}
</main>

<!-- Footer -->
<footer class="border-t border-gray-200 px-6 py-8 text-center text-sm text-gray-400">
  <p>
    Built with <a
      href="https://svelte.dev"
      target="_blank"
      rel="noopener noreferrer"
      class="text-indigo-500 hover:underline">SvelteKit</a
    >
    &amp;
    <a
      href="https://tailwindcss.com"
      target="_blank"
      rel="noopener noreferrer"
      class="text-indigo-500 hover:underline">Tailwind CSS</a
    >
  </p>
</footer>
