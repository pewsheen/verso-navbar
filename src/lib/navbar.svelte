<script>
	import { Button, Input } from 'flowbite-svelte';
	import PrevPageIcon from '../assets/images/angle-left.png';
	import NextPageIcon from '../assets/images/angle-right.png';
	import RefreshIcon from '../assets/images/refresh.png';
	import CloseIcon from '../assets/images/close.png';

	function onClickPrev() {
		console.log('click prev');
		window.prompt('PREV');
	}
	function onClickForward() {
		console.log('click forward');
		window.prompt('FORWARD');
	}
	function onClickRefresh() {
		console.log('click refresh');
		window.prompt('REFRESH');
	}
	function onClickClose() {
		console.log('close');
		window.close();
	}
</script>

<div class="navbar box-border w-full">
	<div class="inline-block w-full">
		<div class="inline-block w-1/4">
			<Button on:click={onClickPrev} class="btn ml-2 h-7 w-7 !p-2"
				><img alt="left angle" src={PrevPageIcon} /></Button
			>
			<Button on:click={onClickForward} class="btn h-7 w-7 !p-2"
				><img alt="left angle" src={NextPageIcon} /></Button
			>
			<Button on:click={onClickRefresh} class="btn h-7 w-7 !p-2"
				><img alt="left angle" src={RefreshIcon} /></Button
			>
		</div>
		<div class="inline-block w-1/2">
			<Input class="h-7" type="text" placeholder="Search or enter website name" />
		</div>
		<div class="float-right inline-block">
			<Button on:click={onClickClose} class="btn h-7 w-7 !p-2"
				><img alt="left angle" src={CloseIcon} /></Button
			>
		</div>
	</div>
</div>

<style lang="scss">
	:global(.btn) {
		background-color: #fafafa;
		&:hover {
			background-color: #f0f0f0;
		}
	}
	.navbar {
		background-color: #fafafa;
		height: 38px;
		padding-top: 6px;
		padding-left: 80px;
		padding-right: 10px;
	}
</style>
