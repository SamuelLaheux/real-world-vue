<template>
  <div>
    <h1>Create an Event, {{ user.name }}, {{ user.id }}</h1>
    <p>{{ getEventById(2) }}</p>
    <p>There are {{ catLength }} categories</p>
    <ul>
      <li v-for="(category, index) in categories" :key="index">
        {{ category }}
      </li>
    </ul>
  </div>
</template>

<script>
import { mapState, mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(['catLength', 'getEventById']),
    ...mapState(["user", "categories"])
  }
};
</script>
