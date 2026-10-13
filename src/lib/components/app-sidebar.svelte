<script lang="ts" module>
	const data = {
		title: 'IT Administration',
		pages: [
			{
				title: 'Dashboard',
				url: '/'
			},
			{
				title: 'Reports',
				url: 'reports'
			}
		]
	};
</script>

<script lang="ts">
	import * as Sidebar from '#lib/components/ui/sidebar/index.js';
	import SearchForm from './search-form.svelte';
	import VersionSwitcher from './version-switcher.svelte';
	import type { ComponentProps } from 'svelte';

	let { ref = $bindable(null), ...restProps }: ComponentProps<typeof Sidebar.Root> = $props();

	let selectedPageIdx = $state(0);
</script>

<Sidebar.Root {...restProps} bind:ref class="p-2">
	<Sidebar.Header>
		<h1 class="text-2xl font-bold">{data.title}</h1>
	</Sidebar.Header>
	<Sidebar.Content>
		<Sidebar.Menu>
			{#each data.pages as page, idx (page.title)}
				<Sidebar.MenuItem>
					<Sidebar.MenuButton
						isActive={data.pages[selectedPageIdx].title === page.title}
						onclick={() => (selectedPageIdx = idx)}
					>
						{#snippet child({ props })}
							<a href={page.url} {...props}>{page.title}</a>
						{/snippet}
					</Sidebar.MenuButton>
				</Sidebar.MenuItem>
			{/each}
		</Sidebar.Menu>
	</Sidebar.Content>
	<Sidebar.Rail />
</Sidebar.Root>
