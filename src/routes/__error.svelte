<script context="module">
	export function load({ error, status }) {
		return {
			props: {
				error,
				status
			}
		};
	}
</script>

<script>
	export let error, status;
</script>

<h1>Error: {status}</h1>
<p>{error.message}</p>
