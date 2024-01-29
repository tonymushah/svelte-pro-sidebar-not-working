<script lang="ts">
	export let className: string;
	export let rootStyles: string | null = null;
</script>

<span style={rootStyles} class={className}>
	<slot />
</span>

<style>
	span {
		flex-grow: 1;
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
	}
</style>
