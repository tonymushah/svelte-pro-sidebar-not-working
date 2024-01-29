<script lang="ts">
	export let open: boolean = false;
	export let rtl: boolean = false;
	export let style: string | null = null;
	export let className: string;
</script>

<span class:rtl class={className} class:open {style}>
	<slot />
</span>

<style>
	span {
		display: inline-block;
		transition: transform 0.3s;
		width: 5px;
		height: 5px;
		transform: rotate('-45deg');
	}
	:not(.rtl) {
		border-right: 2px solid currentcolor;
		border-bottom: 2px solid currentcolor;
	}
	.rtl {
		border-left: 2px solid currentcolor;
		border-top: 2px solid currentcolor;
	}
	.open.rtl {
		transform: rotate('-135deg');
	}

	.open:not(.rtl) {
		transform: rotate('45deg');
	}
</style>
