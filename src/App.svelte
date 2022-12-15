<script>
	let l = 15;
	let dl = 150;
	let cl = 1500;
	let ml = 15000;
	let kg = 1;
	let hg = 10;
	let g = 1000;
	let msk = 66.67;
	let tsk = 200;

	function setfromL(value) {
		l = +value;
		dl = +(10 * l).toFixed(3);
		cl = +(100 * l).toFixed(3);
		ml = +(1000 * l).toFixed(3);
		msk = +(l / 0.015).toFixed(3);
		tsk = +(l / 0.005).toFixed(3);
	}

	function setfromDl(value) {
		dl = +value;
		l = +(dl / 10).toFixed(3);
		cl = +(100 * l).toFixed(3);
		ml = +(1000 * l).toFixed(3);
		msk = +(l / 0.015).toFixed(3);
		tsk = +(l / 0.005).toFixed(3);
	}

	function setfromCl(value) {
		cl = +value;
		l = +(cl / 100).toFixed(3);
		dl = +(10 * l).toFixed(3);
		ml = +(1000 * l).toFixed(3);
		msk = +(l / 0.015).toFixed(3);
		tsk = +(l / 0.005).toFixed(3);
	}

	function setfromMl(value) {
		ml = +value;
		l = +(ml / 1000).toFixed(3);
		cl = +(100 * l).toFixed(3);
		dl = +(10 * l).toFixed(3);
		msk = +(l / 0.015).toFixed(3);
		tsk = +(l / 0.005).toFixed(3);
	}

	function setfromMsk(value) {
		msk = +value;
		l = +(msk * 0.015).toFixed(3);
		dl = +(msk * 0.15).toFixed(3);
		cl = +(msk * 1.5).toFixed(3);
		ml = +(msk * 15).toFixed(3);
		tsk = +(l / 0.005).toFixed(3);
	}

	function setfromTsk(value) {
		tsk = +value;
		l = +(tsk * 0.005).toFixed(3);
		dl = +(tsk * 0.05).toFixed(3);
		cl = +(tsk * 0.5).toFixed(3);
		ml = +(tsk * 5).toFixed(3);
		msk = +(l / 0.015).toFixed(3);
	}

	function setfromKg(value) {
		kg = +value;
		hg = +(kg * 10);
		g = +(kg * 1000);
	}

	function setfromHg(value) {
		hg = +value;
		kg = +(hg / 10);
		g = +(hg * 100);
	}

	function setfromG(value) {
		g = +value;
		kg = +(g / 1000);
		hg = +(g / 100);
	}
</script>

<div class="volym">
	<h1>Volym</h1>

	<div class="volym-form">
		<div class="liter">
			<p>Liter (l)</p>

			<input
				value={l}
				on:input={(e) => setfromL(e.target.value)}
				type="number"
			/>
		</div>

		<div class="deciliter">
			<p>Deciliter (dl)</p>

			<input
				value={dl}
				on:input={(e) => setfromDl(e.target.value)}
				type="number"
			/>
		</div>

		<div class="centiliter">
			<p>Centiliter (cl)</p>

			<input
				value={cl}
				on:input={(e) => setfromCl(e.target.value)}
				type="number"
			/>
		</div>

		<div class="milliliter">
			<p>Milliliter (ml)</p>

			<input
				value={ml}
				on:input={(e) => setfromMl(e.target.value)}
				type="number"
			/>
		</div>
		<div class="matsked">
			<p>Matsked (msk)</p>

			<input
				value={msk}
				on:input={(e) => setfromMsk(e.target.value)}
				type="number"
			/>
		</div>
		<div class="tesked">
			<p>Tesked (tsk)</p>

			<input
				value={tsk}
				on:input={(e) => setfromTsk(e.target.value)}
				type="number"
			/>
		</div>
	</div>
</div>

<div class="vikt">
	<h1>Vikt</h1>

	<div class="vikt-form">
		<div class="kilogram">
			<p>Kilogram (kg)</p>

			<input
				value={kg}
				on:input={(e) => setfromKg(e.target.value)}
				type="number"
			/>
		</div>

		<div class="hektogram">
			<p>Hektogram (hg)</p>

			<input
				value={hg}
				on:input={(e) => setfromHg(e.target.value)}
				type="number"
			/>
		</div>

		<div class="gram">
			<p>Gram (g)</p>

			<input
				value={g}
				on:input={(e) => setfromG(e.target.value)}
				type="number"
			/>
		</div>
	</div>
</div>

<style>
	h1 {
		margin: 0;
	}
	.volym {
		background-color: rgba(154, 175, 250, 0.822);
		padding: 10px;
		padding-top: 30px;
	}
	.volym-form {
		display: flex;
		gap: 16px;
		align-items: flex-end;
		flex-wrap: wrap;
		margin-left: 4px;
		margin: 0;
		padding: 6px;
	}

	.liter {
		flex-grow: 1;
		flex-basis: 160px;
	}
	.deciliter {
		flex-grow: 1;
		flex-basis: 160px;
	}
	.centiliter {
		flex-grow: 1;
		flex-basis: 160px;
	}
	.milliliter {
		flex-grow: 1;
		flex-basis: 160px;
	}
	.matsked {
		flex-grow: 1;
		flex-basis: 160px;
	}
	.tesked {
		flex-grow: 1;
		flex-basis: 160px;
	}

	.vikt {
		background-color: rgb(165, 247, 203);
		padding: 10px;
		padding-top: 20px;
	}

	.vikt-form {
		display: flex;
		gap: 16px;
		align-items: flex-end;
		flex-wrap: wrap;
		margin-left: 4px;
	}

	.kilogram {
		flex-grow: 1;
		flex-basis: 160px;
	}

	.hektogram {
		flex-grow: 1;
		flex-basis: 160px;
	}

	.gram {
		flex-grow: 1;
		flex-basis: 160px;
	}

	input {
		width: 10em;
	}
</style>
