<script lang="ts">
import Canvas from "./Canvas.svelte";
import CheckInput from "./CheckInput.svelte";
import GroupInputs from "./GroupInputs.svelte";
import Input from "./Input.svelte";
import MessageDispatcher from "./MessageDispatcher.svelte";
import MouseArea from "./MouseArea.svelte";
import NumericInputs from "./NumericInputs.svelte";
import OneClickButton from "./OneClickButton.svelte";

export let name: string;

function handleMessage(event: CustomEvent<{text: string}>) {
	alert(event.detail.text);
}

function handleAnyMessage(event: CustomEvent) {
	alert(event.detail?.time)
}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<MouseArea/>
	<OneClickButton/>
	<MessageDispatcher on:message={handleMessage} on:anyMessage={handleAnyMessage}/>
	<Input/>
	<NumericInputs/>
	<CheckInput/>
	<GroupInputs/>
	<Canvas/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;		
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
