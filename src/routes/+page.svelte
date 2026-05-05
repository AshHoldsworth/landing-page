<script lang="ts">
  const links: { title: string; description: string; href: `https://${string}`; label?: string }[] =
    [
      {
        title: 'Meal Planner',
        description: 'Plan your meals and shopping list efficiently',
        href: 'https://mealplanner.ashholdsworth.co.uk/',
        label: 'Go to app →'
      },
      {
        title: 'Coming Soon...',
        description: 'More projects and resources coming soon!',
        href: 'https://ashholdsworth.co.uk/',
        label: undefined
      },
      {
        title: 'Also Coming Soon...',
        description: 'More projects and resources coming soon!',
        href: 'https://ashholdsworth.co.uk/',
        label: undefined
      },
      {
        title: 'Coming Soon aswell...',
        description: 'More projects and resources coming soon!',
        href: 'https://ashholdsworth.co.uk/',
        label: undefined
      }
    ];
</script>

<!-- Hero -->
<section class="bg-linear-to-b from-indigo-50 to-white px-6 py-24 text-center">
  <div class="mx-auto max-w-2xl">
    <h1 class="text-5xl font-extrabold tracking-tight text-gray-900 sm:text-6xl">
      Welcome to<br /><span class="text-indigo-600">Ash Holdsworth</span>
    </h1>
    <div class="mt-10 flex flex-wrap justify-center gap-4">
      <a
        href="https://github.com/AshHoldsworth"
        target="_blank"
        rel="noopener noreferrer"
        class="rounded-xl border border-gray-300 bg-white px-6 py-3 text-sm font-semibold text-gray-700 shadow-sm transition-colors hover:bg-gray-50"
      >
        View on GitHub
      </a>
    </div>
  </div>
</section>

<!-- Feature cards -->
<section id="features" class="px-6 py-20">
  <div class="mx-auto max-w-5xl">
    <h2 class="mb-12 text-center text-3xl font-bold text-gray-900">Explore...</h2>
    <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-4">
      {#each links as link (link.title)}
        <a
          href={link.href}
          target="_blank"
          rel="noopener noreferrer"
          class="group flex flex-col rounded-2xl border border-gray-200 bg-white p-6 shadow-sm transition hover:border-indigo-300 hover:shadow-md"
        >
          <h3
            class="mb-2 font-semibold text-gray-900 transition-colors group-hover:text-indigo-600"
          >
            {link.title}
          </h3>
          <p class="flex-1 text-sm leading-relaxed text-gray-500">{link.description}</p>
          <span class="mt-4 text-sm font-medium text-indigo-600">{link.label}</span>
        </a>
      {/each}
    </div>
  </div>
</section>
