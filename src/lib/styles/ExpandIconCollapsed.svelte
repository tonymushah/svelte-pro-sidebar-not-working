<script lang="ts">
	export let className: string;
</script>

<span class={className}>
	<slot />
</span>

<style>
	span {
		width: 5px;
		height: 5px;
		background-color: currentcolor;
		border-radius: 50%;
		display: inline-block;
	}
</style>
