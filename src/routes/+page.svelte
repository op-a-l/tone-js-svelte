<script lang="ts">
	//Tone.js import
	import * as Tone from 'tone';

	const synth = new Tone.Synth().toDestination();

	let audioOn = false;

	async function toggleAudio() {
		await Tone.start();
		audioOn = true;
		console.log("L'audio est prêt");
	}

	function triggerNote() {
		synth.triggerAttackRelease('A1', '8n');
	}
</script>

<button class="w-screen bg-green-500" on:click={triggerNote}>A1</button>
