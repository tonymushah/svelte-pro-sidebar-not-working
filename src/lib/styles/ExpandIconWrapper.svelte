<script lang="ts">
	export let rootStyles: string | null = null;
	export let collasped = false;
	export let level: number | undefined = undefined;
	export let rtl = false;
	export let className: string;
</script>

<span style={rootStyles} class={className} class:collapsed={collasped && level === 0} class:rtl>
	<slot />
</span>

<style>
	.collapsed {
		position: absolute;
		top: 50%;
		transform: translateY(-50%);
	}
	.collapsed.rtl {
		left: 10px;
	}
	.collapsed:not(.rtl) {
		right: 10px;
	}
</style>
