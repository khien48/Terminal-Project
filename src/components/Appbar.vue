<template v-slot:append>
  
  <!-- NOTIFICATION -->

  <div class="text-center">
    <v-menu open-on-hover>
      <template v-slot:activator="{ props }">
        <v-btn
          style="margin-right: 10px"
          color="teal"
          v-bind="props"
          icon="mdi-bell"
        >
        </v-btn>
      </template>

      <v-list>
        <v-list-item v-for="(item, index) in items" :key="index">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>

  <!-- ............................. -->

  <!-- PROFILE OVERVIEW -->

  <v-list>
    <v-list-item
      style="margin-right: 10px"
      prepend-avatar="https://fthmb.tqn.com/bzCTJWqcE4bZCuV_XXuCJw6zfMo=/2121x1414/filters:fill(auto,1)/GettyImages-548929135-59f24924d088c000104ed810.jpg"
      subtitle="Faculty"
      title="Joan Reyes"
    >
      <template v-slot:append>
        <v-menu open-on-click>
          <template v-slot:activator="{ props }">
            <v-btn
              icon="mdi-menu-down"
              size="small"
              variant="text"
              v-bind="props"
            ></v-btn>
          </template>

          <v-list>
            <v-card class="mx-auto pa-2" max-width="300">

              <!-- MENU FOR PROFILE -->

              <v-list>
                <v-list-subheader>Menu</v-list-subheader>

                <v-list-item
                  color="teal"
                  v-for="(item, i) in items"
                  :key="i"
                  :value="item"
                  rounded="shaped"
                >
                  <template v-slot:prepend>
                    <v-icon :icon="item.icon"></v-icon>
                  </template>

                  <v-list-item-title v-text="item.text"></v-list-item-title>
                </v-list-item>
              </v-list>
            </v-card>
          </v-list>
        </v-menu>
      </template>
    </v-list-item>
  </v-list>

  <!-- ............................. -->
</template>

<script>
export default {
  data: () => ({
    items: [
      { text: "Profile", icon: "mdi-account" },
      { text: "Setting", icon: "mdi-cog" },
      { text: "Send Feedback", icon: "mdi-message-alert-outline" },
    ],
  }),
};
</script>
