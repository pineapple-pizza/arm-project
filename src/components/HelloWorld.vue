<template>
  <v-container>
    <v-card
      class="mx-auto mb-2"
      max-width="344"
      outlined
      v-for="(item, i) in items"
      :key="i"
    >
      <v-list-item three-line>
        <v-list-item-content>
          <div class="overline mb-4">
            {{ $t(item.name) }}
          </div>
          <v-list-item-title>
            {{ $t(item.description) }}
          </v-list-item-title>
          <v-list-item-subtitle>
            {{ $t(item.source) }}
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    items: [
      {
        name: "news.name",
        description: "news.description",
        source: "news.source",
      },
      {
        name: "news.name",
        description: "news.description",
        source: "news.source",
      },
      {
        name: "news.name",
        description: "news.description",
        source: "news.source",
      },
    ],
  }),
};
</script>
