<template>
  <div>
    <ul>
      <!-- <item>아이템 1</item>
      <item>아이템 2</item>
      <item>아이템 3</item>
      <item>아이템 4</item>
      <item>아이템 5</item> -->
      <item v-for="item of items" :key="item.id">
        <template v-if="item.title" v-slot:title>
          <h3>{{ item.title }}</h3>
        </template>
        <template v-if="item.content" v-slot:content>
          <hr />
          {{ item.content }}
        </template>
      </item>
      <item>
        디폴트 아이템 <button style="color:blue"> testButton </button>
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
        { id: 3, title: "아이템3" },
        { id: 4, content: "콘텐트4" }
      ],
    };
  },
};
</script>
