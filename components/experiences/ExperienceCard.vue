<template>
  <div>
    <b-card>
      <b-card-title>
        {{ experience.name }}
      </b-card-title>
      <b-card-text>
        {{ experience.desc }}
      </b-card-text>
      <b-card-text>
        {{ experience.location }}
      </b-card-text>
      <b-card-text>
        {{ experience.date }}
      </b-card-text>

      <b-card-text>
        <b-badge
          v-for="item in experience.technos"
          :key="item"
          variant="secondary"
        >
          {{ item }}
        </b-badge>
      </b-card-text>
    </b-card>
  </div>
</template>
<script>
export default {
  props: {
    experience: Object
  }
}
</script>
