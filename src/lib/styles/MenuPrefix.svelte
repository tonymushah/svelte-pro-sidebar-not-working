<script lang="ts">
	export let firstLevel = false;
	export let collapsed = false;
	export let rtl = false;
	export let rootStyles: string | null = null;
</script>

<span style={rootStyles} class:transition={true} class:fc={firstLevel && collapsed} class:rtl>
	<slot />
</span>

<style>
	.rtl {
		margin-left: 5px;
	}
	:not(.rtl) {
		margin-right: 5px;
	}
	.fc {
		opacity: 0;
	}
	:not(.fc) {
		opacity: 1;
	}
	.transition {
		opacity: opacity var(--transitionDuration);
	}
</style>
