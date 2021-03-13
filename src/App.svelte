<script>
	import { Router } from '@roxi/routify'
	import { routes } from '../.routify/routes'
	import { authStore } from './auth.js'

	// we need to queue our init till after Routify has been initialized
	setTimeout(() => window.routify.inBrowser && authStore.init())
</script>

<!-- style global>
	@import "../static/app.css";
	@import "../static/global.css";
</style -->

<style  global>
  @import "../assets/global.css";
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>

<Router {routes} />
