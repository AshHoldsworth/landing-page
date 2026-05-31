<script lang="ts">
  const links: { title: string; description: string; href: `https://${string}`; label?: string }[] =
    [
      {
        title: 'Meal Planner',
        description: 'Plan your meals and shopping list efficiently',
        href: 'https://mealplanner.ashholdsworth.co.uk/',
        label: 'Meal Planner →'
      },
      {
        title: 'Meal Planner Test',
        description:
          'Test environment for the meal planner app, showcasing new features and improvements',
        href: 'https://mealplanner.test.ashholdsworth.co.uk/',
        label: 'Test new Meal Planner features →'
      },
      {
        title: 'Home Assistant',
        description:
          'Control and automate your smart home with Home Assistant, a powerful open-source platform',
        href: 'https://homeassistant.ashholdsworth.co.uk/',
        label: 'Go to dashboard →'
      },
      {
        title: 'Jellyfin',
        description: 'Stream and manage your media with Jellyfin, a free software media system',
        href: 'https://media.ashholdsworth.co.uk/',
        label: 'Launch Jellyfin →'
      },
      {
        title: 'Manage your account',
        description: 'Manage your account settings and preferences',
        href: 'https://auth.ashholdsworth.co.uk/',
        label: 'Manage your account →'
      }
    ];
</script>

<section class="px-4 pt-8 sm:px-6 sm:pt-12">
  <div class="hero rounded-2xl border border-base-300 bg-base-100 shadow-sm">
    <div class="hero-content py-14 text-center">
      <div class="max-w-2xl">
        <h1 class="text-4xl font-bold leading-tight sm:text-6xl">
          Welcome to<br /><span class="text-primary">Ash Holdsworth</span>
        </h1>
        <p class="mt-5 text-base-content/70">
          Quick links to projects, experiments, and what is coming next.
        </p>
        <div class="mt-8 flex flex-wrap justify-center gap-3">
          <a
            href="https://github.com/AshHoldsworth"
            target="_blank"
            rel="noopener noreferrer"
            class="btn btn-neutral"
          >
            View on GitHub
          </a>
          <a href="/about" class="btn btn-outline">About this site</a>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="features" class="px-4 py-12 sm:px-6 sm:py-16">
  <div class="mx-auto max-w-6xl">
    <div class="mb-8 flex items-center justify-between gap-4">
      <h2 class="text-2xl font-bold sm:text-3xl">Explore</h2>
      <span class="badge badge-outline">{links.length} Links</span>
    </div>
    <div class="grid gap-4 sm:grid-cols-2 xl:grid-cols-4">
      {#each links as link (link.title)}
        <a
          href={link.href}
          target="_blank"
          rel="noopener noreferrer"
          class="card border border-base-300 bg-base-100 shadow-sm transition-all hover:-translate-y-1 hover:shadow-lg"
        >
          <div class="card-body gap-3">
            <h3 class="card-title text-lg">{link.title}</h3>
            <p class="text-sm text-base-content/70">{link.description}</p>
            {#if link.label}
              <div class="card-actions mt-2">
                <span class="btn btn-sm btn-soft btn-primary">{link.label}</span>
              </div>
            {/if}
          </div>
        </a>
      {/each}
    </div>
  </div>
</section>
