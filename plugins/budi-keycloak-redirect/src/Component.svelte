<script>
	import { onMount } from "svelte"
	export let id
	export let appPath
	export let userId

	onMount(() => {
		if (
			!location.href.match("builder") &&
			!location.href.match("preview")
		) {
			if (!id) throw new Error("missing id")
			if (!appPath) throw new Error("missing appPath")
			if (!userId) {
				document.cookie = `budibase:returnurl = ${appPath}; path=/`
				location.href = `/api/global/auth/default/oidc/configs/${id}`
			}
		}
	})
</script>
