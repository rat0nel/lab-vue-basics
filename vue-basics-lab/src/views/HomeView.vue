<template>
  <div class="calculator">
    <input type="number" v-model="num1" />
    <input type="number" v-model="num2" />
    <p>{{ result }}</p>
    <button @click="calculate">Calculate</button>
  
  <Card
    v-for="post in posts"
    :title="post.title"
    :description="post.description"
    :key="post.id"
  /></div>
</template>

<script>
import Card from "@/components/Card.vue";

export default {
  name: "HomeView",
   components: {
       Card,
   },

  data() {
    return {
      num1: 1,
      num2: 2,
      result: null,
      posts: [
        {
          title: "Title 1",
          description: "Desciption 1",
        },
        {
          title: "Title 2",
          description: "Desciption 2",
        },
        {
          title: "Title 3",
          description: "Desciption 3",
        },
      ],
    };
  },
  methods: {
    calculate() {
      this.result = this.num1 + this.num2;
    },
  },
};
</script>
