<template>
  <v-container>
    <v-row>
      <v-col>
        <div class="text-body-1" style="color: #395197">
          <p>Представленные мною анекдоты делятся на две группы:</p>
          <p>
            <nuxt-link to="/entertainment/anecdotes/about_school">
              анекдоты о школе
            </nuxt-link>
            и
            <nuxt-link to="/entertainment/anecdotes/humor-in-short-pants">
              юмор в коротких штанишках
            </nuxt-link>
          </p>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Anecdotes'
}
</script>

<style scoped>

</style>
