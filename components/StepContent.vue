<template>
  <li class="steps-segment">
    <span href="#" class="steps-marker"></span>
    <div class="steps-content" style='margin-left: 3rem;'>
      <slot/>
      <b-collapse v-if='!!$slots.collapse' :open="false" aria-id="contentIdForA11y1" position="is-bottom">
        <a class="showmore" slot="trigger" slot-scope="props">
          <b-icon :icon="!props.open ? 'caret-down' : 'caret-up'"></b-icon>
        </a>
        <slot name='collapse'/>
      </b-collapse>

    </div>
  </li>
</template>

<style lang="scss" scoped>
.steps-content {
  padding-bottom: 2rem !important;
}
.steps-content ul {
  list-style-type: circle;
  list-style-position: inside;
  padding-top: 5px;
  padding-left: 5px;
}

figcaption {
  text-align: center;
  font-size: 0.8rem;
  margin-top: 6px;
}

.showmore {
  width: 100%;
  display: inline-block;
  text-align: right;
}

</style>
