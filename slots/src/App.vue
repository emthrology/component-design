<template>
  <div>
    <ul>
      <!-- <item>아이템 1</item>
      <item>아이템 2</item>
      <item>아이템 3</item>
      <item>아이템 4</item>
      <item>아이템 5</item> -->
      <item v-for="item of items" :key="item.id">
        <template v-slot:title>
          {{ item.title }}
        </template>
        <template v-slot:content>
          {{ item.content }}
        </template>
      </item>
    </ul>
  </div>
</template>

<script>
import Item from "./Item.vue";

export default {
  components: {
    Item,
  },
  data() {
    return {
      items: [
        { id: 1, title: "아이템1", content: "콘텐트1" },
        { id: 2, title: "아이템2", content: "콘텐트2" },
      ],
    };
  },
};
</script>
