<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import '../app.css';

	let { children } = $props();
</script>

<ParaglideJS {i18n}>
	<div class="app">
		<main>
			{@render children()}
		</main>

		<footer>
			<p>Live free, chase adventure, capture the world—play wild and frame every moment.</p>
		</footer>
	</div>
</ParaglideJS>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 667px;
		min-width: 375px;
		overflow: scroll;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		gap: 5rem;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
