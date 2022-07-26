<script lang="ts">
	import { BarGraph } from '@src/components/bargraph';
	import { Baritem } from '@src/components/baritem';
	import { each } from 'svelte/internal';

	const textNumbers: number[] = [0.1, 0.2, 0.4, 0.7, 1.2, 1.9, 3.3, 4.8];
	const leftNumbers: number[] = [0.0, 0.5, 1.0, 1.5, 2.0, 2.5, 3.0, 3.5, 4.0, 4.5, 5.0];

	const legend: number = textNumbers.length;
	const min: number = Math.min(...textNumbers);
	const max: number = Math.max(...textNumbers);
</script>

<h1
	style="margin: 30px; text-align:center;
"
>
	Component를 이용하여 BarChart를 구현하기
</h1>
<h3
	style="margin: 30px; text-align:center;
"
>
	최소값: {min} 최대값: {max} 아이템 개수: {legend}
</h3>

<div class="frame">
	<div class="numbers" style="margin-left:-40px; margin-bottom:-5px;">
		{#each leftNumbers as item}
			<div class="numbers">{item}</div>
		{/each}
	</div>
	{#each textNumbers as item}
		<Baritem {item} data-number={item} />
	{/each}
</div>

<!--<Button {text} color="orange" onClick={(value) => {}}/>-->
<style lang="scss">
	.numbers {
		width: 30px;
		display: flex;
		flex-wrap: wrap;
		margin-top: 90%;
		flex-direction: column-reverse;
		//margin-bottom: -10px;
	}

	.frame {
		width: 700px;
		height: 500px;

		display: flex;

		align-items: flex-end;
		justify-content: space-around;
		text-align: center;
		margin: auto;

		border-bottom: solid 2px rgb(170, 170, 170);
		border-left: solid 2px rgb(170, 170, 170);

		background: repeating-linear-gradient(
			0,
			transparent,
			transparent 9.5%,

			rgba(170, 170, 170, 0.7) 10%
		);
	}
</style>
