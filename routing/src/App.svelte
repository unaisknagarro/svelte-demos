<script lang="ts">
  import { Router, Route } from 'svelte-routing'
  import Home from './pages/Home.svelte'
  import Details from './pages/Details.svelte'
</script>

<Router>
  <Route component={Home} />
  <Route path="/product/:id" let:params>
      <Details id={params.id} />
  </Route>
</Router>