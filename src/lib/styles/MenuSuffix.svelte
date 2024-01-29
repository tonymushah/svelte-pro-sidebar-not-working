<script lang="ts">
	export let className: string;
	export let collapsed = false;
	export let firstLevel = false;
	export let rootStyles: string | null = null;
	$: fc = firstLevel && collapsed;
</script>

<span style={rootStyles} class:fc class={className}>
	<slot />
</span>

<style>
	span {
		margin-right: 5px;
		margin-left: 5px;
		transition: opacity var(--transitionDuration);
	}
	.fc {
		opacity: 0;
	}
	:not(.fc) {
		opacity: 1;
	}
</style>
