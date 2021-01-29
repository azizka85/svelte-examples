<script lang="ts">
	let user = {  
		loggedIn: false
	};

	function toggle() {
		user.loggedIn = !user.loggedIn
	}
</script>

<button on:click={toggle}>
{#if user.loggedIn}
	Log out
{:else}
	Log in
{/if}
</button>
