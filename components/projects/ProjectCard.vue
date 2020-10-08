<template>
  <b-col md="3">
    <b-card
      img-src="https://picsum.photos/600/300/?image=25"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2"
    >
      <b-card-title>
        {{ project.name }}
      </b-card-title>
      <b-card-text>
        {{ project.desc }}
      </b-card-text>
      <b-card-text>
        <b-badge
          variant="success"
          v-for="item in project.technos"
          :key="item"
        >
          {{ item }}
        </b-badge>
      </b-card-text>
      <b-button href="#" variant="success">
        <b-icon icon="plus-circle" />
        Détails
      </b-button>
    </b-card>
  </b-col>
</template>
<script>
import { BIcon } from 'bootstrap-vue'
export default {
  components: {
    BIcon
  },
  props: {
    project: Object
  }
}
</script>
