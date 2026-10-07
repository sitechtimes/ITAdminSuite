<script lang="ts">
	interface Props {
		label: string;
		level: 1 | 2 | 3 | 4 | 5 | 6;
		color: 'primary' | 'secondary' | 'accent' | 'neutral';
	}

	let { label, level, color = 'primary' }: Props = $props();

	const sizes = {
		1: 'text-4xl md:text-5xl',
		2: 'text-3xl md:text-4xl',
		3: 'text-2xl md:text-3xl',
		4: 'text-xl md:text-2xl',
		5: 'text-lg md:text-xl',
		6: 'text-base md:text-lg'
	};

	const colors = {
		primary: 'text-primary-ink',
		secondary: 'text-secondary-ink',
		accent: 'text-accent-ink',
		neutral: 'text-neutral-ink',
	};
</script>

<svelte:element this={`h${level}`} class="{sizes[level]} {colors[color]} font-bold text-center">
	{label}
</svelte:element>
