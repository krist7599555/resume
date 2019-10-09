<template>
  <div class='steps-wrapper'>
    <h1 class="is-size-3 has-text-weight-bold is-uppercase">
      {{label}}
      <!-- <b-icon :icon='icon' size="is-large"/> -->
    </h1>
    <hr>
    <ul class="steps is-vertical">
      <slot />
    </ul>
  </div>
</template>

<script>
export default {
  props: ['label', 'icon']
}
</script>

