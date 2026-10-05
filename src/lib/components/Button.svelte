<script lang="ts">
	interface Props {
		label: string;
		size: 'xs' | 'sm' | 'md' | 'lg' | 'xl' | '2xl' | '3xl' | '4xl';
		color: 'primary' | 'secondary' | 'accent' | 'neutral';
	}

	let { label, size = 'lg', color = 'primary' }: Props = $props();

	const colors = {
		primary: 'bg-primary text-primary-ink hover:bg-primary-hover',
		secondary: 'bg-secondary text-secondary-ink',
		accent: 'bg-accent text-accent-ink',
		neutral: 'bg-neutral text-neutral-ink'
	};
</script>

<a href="/random"
	><button class="rounded-lg px-6 py-2 hover:cursor-pointer text-{size} {colors[color]}">
		{label}
	</button></a
>
