<script>
	import { page } from '$app/stores';

	let { children } = $props();
</script>

<nav
	class:has-color={!!$page.data.color}
	style:background={$page.data.color ?? 'var(--bg-2)'}
>
	<a href="/">home</a>
	<a href="/red">red</a>
	<a href="/green">green</a>
	<a href="/blue">blue</a>
</nav>

{@render children()}

<style>
	nav.has-color,
	nav.has-color a {
		color: white;
	}
</style>