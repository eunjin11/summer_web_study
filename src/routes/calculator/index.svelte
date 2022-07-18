<script lang="ts">
	import { Button } from '@src/components/button';
	import { each } from 'svelte/internal';

	const textNumbers: string[] = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0'];
	const textCequal: string[] = ['C', '='];
	const textOperators: string[] = ['+', '-', '*', '/'];

	let num: number = 0;
	let sum: number = 0;
	let str: string = '';
	let oper: string = '';
	let oper2: string = '';
	let str2: string = '';
</script>

<div class="typing">
	{str}
</div>

<div class="frame">
	<!--html 문법-->

	<div class="number">
		{#each textNumbers as text}
			<Button
				{text}
				color="orange"
				onClick={(value) => {
					str2 = str2 + value;
					//num = parseInt(value);
					str = str + value;

					num = parseInt(str2);

					if (oper == '') sum = num;
					if (oper == '+') {
						sum = sum + num;
					} else if (oper == '-') {
						sum = sum - num;
					} else if (oper == '/') {
						sum = sum / num;
					} else if (oper == '*') {
						sum = sum * num;
					}
				}}
			/>
		{/each}
	</div>

	<div class="operators">
		{#each textOperators as text}
			<Button
				{text}
				color="grey"
				onClick={(value) => {
					oper = value;
					str = str + oper;
					str2 = '';
				}}
			/>
		{/each}
	</div>

	<div class="Ceqaul">
		{#each textCequal as text}
			<Button
				{text}
				color="dark-grey"
				onClick={(value) => {
					oper2 = value;
					oper = '';

					if (oper2 == 'C') {
						str = '';
						str2 = '';
						sum = 0;
					} else if (oper2 == '=') {
						str = '';
						str2 = '';
						str = str + sum;
					}
				}}
			/>
		{/each}
	</div>
</div>

<style lang="scss">
	.frame {
		width: 320px;
		height: 400px;
		display: flex;
		flex-wrap: wrap;
	}

	.typing {
		height: 80px;
		width: 320px;
	}

	.number {
		width: 240px;
		display: flex;
		flex-wrap: wrap;
	}

	.Ceqaul {
		display: flex;
		height: 80px;
		width: 160px;
		color: white;
	}
</style>
