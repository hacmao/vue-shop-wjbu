<template class="header">
    <v-app-bar
      app
      color="#ccced3"
      flat
      elevation="5"
    >
      <v-container class="py-0 fill-height">
        <img src="/cat-solid.svg" width="35px">

        <v-btn
          v-for="link in links"
          :key="link"
          text
          :href="link.path"
        >
          {{ link.name }}
        </v-btn>

        <v-spacer></v-spacer>

        <v-responsive max-width="260">
          <v-text-field
            dense
            flat
            hide-details
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive>
        <v-btn 
			elevation="2"
			outlined
		>
			Sign In
		</v-btn>
      </v-container>
    </v-app-bar>
</template>

<script>
export default {
    name: "Header",
    data: function() {
        return {
            links: [
              {
                name: "Home",
                path: "/"
              }, 
              {
                name: "Notify",
                path: "/"
              }
            ]
        }
    }
}
</script>

<style>
.header {
  padding: 10px 16px;
  position: fixed;
  top: 0;
  width: 100%
}

.v-responsive {
	margin: 1em;
}
</style>