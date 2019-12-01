<template>
  <div class="home">
    <div class="m-4">
      <h2>02 Nov 2019 - Daily Scrum</h2>
      <h4 class="text-gray-600 font-serif">for Ghiura Alexandru</h4>
    </div>
    <form class="block p-2 m-2" @submit.prevent="onSubmit">
      <div class="mb-4">
        <label class="font-mono block pb-2">
          1. What did you do
          <b>yesterday</b> ?
        </label>
        <input
          class="input block w-full"
          type="text"
          v-model="yesterday"
          placeholder="Something useful you achieved yesterday"
        />
      </div>
      <div class="mb-4">
        <label class="font-mono block pb-2">
          2. What will you do (focus)
          <b>today</b> ?
        </label>
        <input v-model="today" class="input block w-full" type="text" />
      </div>
      <div class="mb-4">
        <label class="font-mono block pb-2"
          >3. What epic are you focusing on (#code - Title) ?</label
        >
        <input
          v-model="epic"
          class="input block w-full"
          type="text"
          placeholder="#SPOT-211 - Some title"
        />
      </div>
      <div class="mb-4">
        <label class="font-mono block pb-2"
          >4. What problems are you facing?</label
        >
        <textarea
          class="input block w-full"
          rows="3"
          type="text"
          v-model="problems"
          placeholder="You can list multiple items."
        />
      </div>
      <div>
        <button class="btn">SUBMIT</button>
      </div>
    </form>
  </div>
</template>

<script lang="ts">
interface Answear {
  yesterday: string;
  today: string;
  epic: string;
  problems: string;
}

export default {
  name: "home",
  components: {},
  data(): Answear {
    return {
      yesterday: "",
      today: "",
      epic: "",
      problems: ""
    };
  },
  methods: {
    onSubmit(): void {
      console.log({ ...this.$data });
    }
  }
};
</script>
