<script lang="ts">
	import { BarGraph } from '@src/components/bargraph';
	import { Baritem } from '@src/components/baritem';
	import { updateData, priceData, type PriceUnit } from '@src/store';
	import { onMount, onDestroy } from 'svelte';
	let data: number[] = [1, 2, 3, 5, 8];
	let title: string = 'Hello world';

	let textNumbers: number[] = [1, 2, 3, 4, 5, 6];

	const legend: number = textNumbers.length;

	const minV: number = Math.min(...textNumbers);
	const maxV: number = Math.max(...textNumbers);

	let prices: [number, number][] = [];

	onMount(() => {
		updateData(7);
	});
</script>

<div class="root">
	<div>
		<select
			style="
		position: fixed; display:block; left: 10px; top: 10px;"
		>
			<option>7</option>
			<option>30</option>
			<option>90</option>
		</select>
		<h1
			style="
		position: fixed; display:block; left: 10px; top: 30px;"
		>
			{$priceData.length}
		</h1>
	</div>
	<div>
		<div class="header">
			<div class="name">DENOM</div>
			<div class="timestamp">TIMESTAMP &nbsp;</div>
			<div class="price">PRICE &nbsp;</div>
			<div class="price">MARKETCAP &nbsp;</div>
			<div class="price">DAYVOLUME</div>
		</div>

		<div class="table">
			{#each $priceData as price}
				<div class="item">
					<div class="name">{price.denom}&nbsp;</div>
					<div class="timestamp">{price.timestamp}&nbsp;</div>
					<div class="price">{price.price}&nbsp;</div>
					<div class="price">{price.marketCap}&nbsp;</div>
					<div class="price">{price.dayVolume}</div>
				</div>
			{/each}
		</div>
	</div>
</div>

<style lang="scss">
	.header {
		top: 15%;
		width: 100%;
		display: flex;
		background-color: pink;
		position: sticky;
	}

	.item {
		display: flex;
		//flex-wrap: wrap;
		border-bottom: solid 2px rgb(170, 170, 170);
		border-right: solid 2px rgb(170, 170, 170);
		//text-align: center;
	}

	.name {
		text-align: center;
		border-left: solid 2px rgb(170, 170, 170);
		width: 20%;
	}
	.timestamp {
		text-align: center;
		border-left: solid 2px rgb(170, 170, 170);
		width: 20%;
	}
	.price {
		text-align: center;
		border-left: solid 2px rgb(170, 170, 170);
		width: 20%;
	}
</style>
