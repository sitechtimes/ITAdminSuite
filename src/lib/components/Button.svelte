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

<button class="hover:cursor-pointer px-6 py-2 rounded-lg text-{size} {colors[color]}">
	{label}
</button>
