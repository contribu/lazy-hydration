
<script>
import StopWatch from "../../components/stop-watch.vue";
import Hydrate from "lazy-hydration";

export default {
  components: {
    StopWatch,
    Hydrate
  }
};
</script>

<template>
  <div>
    <div :class="$style.banner">
      <h1>On Interaction</h1>

      <pre><code>{{`&lt;Hydrate on-interaction&gt;...&lt;/Hydrate&gt;`}}</code></pre>
    </div>

    <div :class="$style.watches">
      <Hydrate on-interaction>
        <StopWatch autoStart description="interact (focus or hover) to start" />
      </Hydrate>
      <StopWatch autoStart description="started on page mount" />
    </div>
  </div>
</template>

<style module>
.banner {
  margin: 0 auto;
  max-width: 600px;
  padding: 24px;
}

.watches {
  display: flex;
  flex-direction: row;
}
</style>